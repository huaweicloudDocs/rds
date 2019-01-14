# AK/SK认证<a name="rds_03_0003"></a>

## 应用场景<a name="section17023744719"></a>

通过使用Access Key ID（AK）/Secret Access Key（SK）加密的方法来验证某个请求发送者身份。当您使用AK/SK认证方式完成认证鉴权时，需要通过请求签名流程获取签名并增加到业务接口请求消息头中。

>![](public_sys-resources/icon-note.gif) **说明：**   
>AK \(Access Key ID\)：访问密钥ID。与私有访问密钥关联的唯一标识符；访问密钥ID和私有访问密钥一起使用，对请求进行加密签名。  
>SK \(Secret Access Key\)：与访问密钥ID结合使用的密钥，对请求进行加密签名，可标识发送方，并防止请求被修改。  

## 调用接口步骤<a name="section10613529183317"></a>

1.  生成AK/SK。如果已生成过AK/SK，则可跳过该步骤，找到原来已下载的AK/SK文件，文件名一般为：credentials.csv。
    1.  注册并登录管理控制台。
    2.  单击用户名，在下拉列表中单击“我的凭证”。

    1.  单击“管理访问密钥”。
    2.  单击“新增访问密钥”，进入“新增访问密钥”页面。
    3.  输入当前用户的登录密码。
    4.  通过邮箱或者手机进行验证，输入对应的验证码。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >在统一身份服务中创建的用户，如果创建时未填写邮箱或者手机号，则只需校验登录密码。  

    5.  单击“确定”，下载访问密钥。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >为防止访问密钥泄露，建议您将其保存到安全的位置。  


2.  <a name="li17137133433914"></a>工程中引入API网关签名SDK。
    1.  下载API网关签名工具。

        下载地址：[https://obs.cn-north-1.myhwclouds.com/apig-sdk/ApiGateway-java-sdk.zip](https://obs.cn-north-1.myhwclouds.com/apig-sdk/ApiGateway-java-sdk.zip)。

    2.  解压下载的压缩包，得到依赖所需的jar文件。
    3.  将解压出来的jar文件添加到依赖路径中，不同的IDE添加方法不同，详细方法请参考IDE帮助文档。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >如果项目使用Maven进行依赖管理，可以不通过IDE添加依赖库，而是使用Maven本地依赖配置“java-sdk-core\*.jar”，其余jar则直接使用Maven中心仓库中的包。  


3.  对请求进行签名。

    签名方法集成在[步骤2](#li17137133433914)引入的jar文件中。发送请求前，需要对请求内容进行签名，得到的签名结果将作为http头部信息一起发送。

    以下结合demo中的post方法调用过程，介绍签名的实现。

    1.  初始化post方法。

        见“Demo.java”。post方法中传入AK/SK，请求URL以及请求Body体。签名在“accessService.access\(\)”方法中完成。

        ```
            public static void post(String ak, String sk, String requestUrl, String postbody)
                throws UnsupportedEncodingException {
        
                AccessService accessService = new AccessServiceImpl(ak, sk);
                URL url = null;
                try {
                    url = new URL(requestUrl);
                } catch (MalformedURLException e) {
                    e.printStackTrace();
                }
                InputStream content = new ByteArrayInputStream(postbody.getBytes("UTF8"));
                HttpMethodName httpMethod = HttpMethodName.POST;
                HttpResponse response;
        
                try {
                    response = accessService.access(url, content, (long) postbody.getBytes("UTF8").length, httpMethod);
                    System.out.println(convertStreamToString(response.getEntity().getContent()));
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
            }
        ```

    2.  创建用于签名的请求request，对象为SDK包中的方法：com.cloud.sdk.DefaultRequest。

        设置DefaultRequest的目标API URL、HTTPS方法、内容等信息。见“AccessServiceImpl.java”。

        ```
         public HttpResponse access(URL url, Map<String, String> headers, InputStream content, Long contentLength,
                HttpMethodName httpMethod) throws Exception {
        
                Request request = new DefaultRequest();
                try {
                    request.setEndpoint(url.toURI());
                ...
                request.setHttpMethod(httpMethod);
                if (headers != null) {
                    request.setHeaders(headers);
                }
                request.setContent(content);
                ...
        ```

    3.  调用SDK的签名方法，对Request进行签名：

        签名后，Request的“http header“中将增加签名信息如“x-sdk-date“，“Authorization“等。见“AccessServiceImpl.java”。

        ```
                ...
                Signer signer = SignerFactory.getSigner();
                signer.sign(request, new BasicCredentials(this.ak, this.sk));
                ...
        ```

    4.  发送带有签名信息的请求。

        把上步中签名产生的request转换为一个适合发送的请求，并将签名后request中的“header“信息放入新的request中。

        以“Apache HttpClient“为例，需要把“DefaultRequest“转换为“HttpRequestBase“，把签名后的“DefaultRequest“的header信息放入“HttpRequestBase“中。

        见“AccessServiceImpl.java”。

        ```
                ...
                HttpRequestBase httpRequestBase = createRequest(url, null, request.getContent(), contentLength, httpMethod);
                Map<String, String> requestHeaders = request.getHeaders();
        
                for (String key : requestHeaders.keySet()) {
                    if (key.equalsIgnoreCase(HttpHeaders.CONTENT_LENGTH.toString())) {
                        continue;
                    }
                    httpRequestBase.addHeader(key, requestHeaders.get(key));
                }
                httpRequestBase.addHeader("Content-Type", "application/json");        
                httpRequestBase.addHeader("X-Language", "en-us");
                HttpResponse response = null;
                SSLContext sslContext =
                    SSLContexts.custom().loadTrustMaterial(null, new TrustSelfSignedStrategy()).useTLS().build();
                SSLConnectionSocketFactory sslSocketFactory =
                    new SSLConnectionSocketFactory(sslContext, new AllowAllHostnameVerifier());
        
                client = HttpClients.custom().setSSLSocketFactory(sslSocketFactory).build();
        
                response = client.execute(httpRequestBase);
                ...
        ```

        示例代码展示了如何对一个请求进行签名，并通过HTTP Client发送一个HTTPS请求的过程。代码分成三个类进行演示：

        -   AccessService：抽象类，将GET/POST/PUT/DELETE归一成access方法。
        -   Demo：运行入口，模拟用户进行GET/POST/PUT/DELETE请求。
        -   AccessServiceImpl：实现access方法，具体与API网关通信的代码都在access方法中。

        各region的域名，请参考[地区和终端节点](http://developer.huaweicloud.com/endpoint)。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >1.  URI、AK、SK、HTTP METHOD是必须设置的参数。  
        >2.  可通过request.addHeader\(\)添加头信息。  

        **AccessService.java:**

        ```
        package com.cloud.apigateway.sdk.demo;
        
        import java.io.InputStream;
        import java.net.URL;
        import java.util.Map;
        
        import org.apache.http.HttpResponse;
        
        import com.cloud.sdk.http.HttpMethodName;
        
        public abstract class AccessService {
        
            protected String ak = null;
        
            protected String sk = null;
        
            public AccessService(String ak, String sk) {
                this.ak = ak;
                this.sk = sk;
            }
        
            public abstract HttpResponse access(URL url, Map<String, String> header, InputStream content, Long contentLength,
                                                HttpMethodName httpMethod) throws Exception;
        
            public HttpResponse access(URL url, Map<String, String> header, HttpMethodName httpMethod) throws Exception {
                return this.access(url, header, null, 0l, httpMethod);
            }
        
            public HttpResponse access(URL url, InputStream content, Long contentLength, HttpMethodName httpMethod)
                    throws Exception {
                return this.access(url, null, content, contentLength, httpMethod);
            }
            public HttpResponse access(URL url, HttpMethodName httpMethod) throws Exception {
                return this.access(url, null, null, 0l, httpMethod);
            }
        
            public abstract void close();
        
            public String getAk() {
                return ak;
            }
        
            public void setAk(String ak) {
                this.ak = ak;
            }
        
            public String getSk() {
                return sk;
            }
        
            public void setSk(String sk) {
                this.sk = sk;
            }
        
        }
        ```

        **AccessServiceImpl.java:**

        ```
        package com.cloud.apigateway.sdk.demo;
        
        import java.io.IOException;
        import java.io.InputStream;
        import java.net.URISyntaxException;
        import java.net.URL;
        import java.net.URLDecoder;
        import java.util.HashMap;
        import java.util.Map;
        
        import javax.net.ssl.SSLContext;
        
        import org.apache.http.Header;
        import org.apache.http.HttpHeaders;
        import org.apache.http.HttpResponse;
        import org.apache.http.client.methods.HttpDelete;
        import org.apache.http.client.methods.HttpGet;
        import org.apache.http.client.methods.HttpHead;
        import org.apache.http.client.methods.HttpPatch;
        import org.apache.http.client.methods.HttpPost;
        import org.apache.http.client.methods.HttpPut;
        import org.apache.http.client.methods.HttpRequestBase;
        import org.apache.http.conn.ssl.AllowAllHostnameVerifier;
        import org.apache.http.conn.ssl.SSLConnectionSocketFactory;
        import org.apache.http.conn.ssl.SSLContexts;
        import org.apache.http.conn.ssl.TrustSelfSignedStrategy;
        import org.apache.http.entity.InputStreamEntity;
        import org.apache.http.impl.client.CloseableHttpClient;
        import org.apache.http.impl.client.HttpClients;
        
        import com.cloud.sdk.DefaultRequest;
        import com.cloud.sdk.Request;
        import com.cloud.sdk.auth.credentials.BasicCredentials;
        import com.cloud.sdk.auth.signer.Signer;
        import com.cloud.sdk.auth.signer.SignerFactory;
        import com.cloud.sdk.http.HttpMethodName;
        
        
        public class AccessServiceImpl extends AccessService {
        
            private CloseableHttpClient client = null;
        
            public AccessServiceImpl(String ak, String sk) {
                super(ak, sk);
            }
        
            /** {@inheritDoc} */
            @Override
            public HttpResponse access(URL url, Map<String, String> headers,
                                       InputStream content, Long contentLength, HttpMethodName httpMethod)
                    throws Exception {
        
                // Make a request for signing.
                Request request = new DefaultRequest();
                try {
                    // Set the request address.
                    request.setEndpoint(url.toURI());
        
                    String urlString = url.toString();
        
                    String parameters = null;
        
                    if (urlString.contains("?")) {
                        parameters = urlString.substring(urlString.indexOf("?") + 1);
                        Map parametersmap = new HashMap<String, String>();
        
                        if (null != parameters && !"".equals(parameters)) {
                            String[] parameterarray = parameters.split("&");
        
                            for (String p : parameterarray) {
                                String key = p.split("=")[0];
                                String value = p.split("=")[1];
                                parametersmap.put(key, URLDecoder.decode(value, "UTF-8"));
                            }
                            request.setParameters(parametersmap);
                        }
                    }
        
                } catch (URISyntaxException e) {
                    // It is recommended to add logs in this place.
                    e.printStackTrace();
                }
                // Set the request method.
                request.setHttpMethod(httpMethod);
                if (headers != null) {
                    // Add request header information if required.
                    request.setHeaders(headers);
                }
                // Configure the request content.
                request.setContent(content);
        
                // Select an algorithm for request signing.
                Signer signer = SignerFactory.getSigner();
                // Sign the request, and the request will change after the signing.
                signer.sign(request, new BasicCredentials(this.ak, this.sk));
        
                // Make a request that can be sent by the HTTP client.
                HttpRequestBase httpRequestBase = createRequest(url, null,
                        request.getContent(), contentLength, httpMethod);
                Map<String, String> requestHeaders = request.getHeaders();
                // Put the header of the signed request to the new request.
                for (String key : requestHeaders.keySet()) {
                    if (key.equalsIgnoreCase(HttpHeaders.CONTENT_LENGTH.toString())) {
                        continue;
                    }
                    httpRequestBase.addHeader(key, requestHeaders.get(key));
                }
                httpRequestBase.addHeader("Content-Type", "application/json");
                httpRequestBase.addHeader("X-Language", "en-us");
                HttpResponse response = null;
                SSLContext sslContext = SSLContexts.custom()
                        .loadTrustMaterial(null, new TrustSelfSignedStrategy())
                        .useTLS().build();
                SSLConnectionSocketFactory sslSocketFactory = new SSLConnectionSocketFactory(
                        sslContext, new AllowAllHostnameVerifier());
        
                client = HttpClients.custom().setSSLSocketFactory(sslSocketFactory)
                        .build();
                // Send the request, and a response will be returned.
                response = client.execute(httpRequestBase);
                return response;
            }
        
            /**
             * Make a request that can be sent by the HTTP client.
             *
             * @param url
             *            specifies the API access path.
             * @param header
             *            specifies the header information to be added.
             * @param content
             *            specifies the body content to be sent in the API call.
             * @param contentLength
             *            specifies the length of the content. This parameter is optional.
             * @param httpMethod
             *            specifies the HTTP method to be used.
             * @return specifies the request that can be sent by an HTTP client.
             */
            private static HttpRequestBase createRequest(URL url, Header header,
                                                         InputStream content, Long contentLength, HttpMethodName httpMethod) {
        
                HttpRequestBase httpRequest;
                if (httpMethod == HttpMethodName.POST) {
                    HttpPost postMethod = new HttpPost(url.toString());
        
                    if (content != null) {
                        InputStreamEntity entity = new InputStreamEntity(content,
                                contentLength);
                        postMethod.setEntity(entity);
                    }
                    httpRequest = postMethod;
                } else if (httpMethod == HttpMethodName.PUT) {
                    HttpPut putMethod = new HttpPut(url.toString());
                    httpRequest = putMethod;
        
                    if (content != null) {
                        InputStreamEntity entity = new InputStreamEntity(content,
                                contentLength);
                        putMethod.setEntity(entity);
                    }
                } else if (httpMethod == HttpMethodName.PATCH) {
                    HttpPatch patchMethod = new HttpPatch(url.toString());
                    httpRequest = patchMethod;
        
                    if (content != null) {
                        InputStreamEntity entity = new InputStreamEntity(content,
                                contentLength);
                        patchMethod.setEntity(entity);
                    }
                } else if (httpMethod == HttpMethodName.GET) {
                    httpRequest = new HttpGet(url.toString());
                } else if (httpMethod == HttpMethodName.DELETE) {
                    httpRequest = new HttpDelete(url.toString());
                } else if (httpMethod == HttpMethodName.HEAD) {
                    httpRequest = new HttpHead(url.toString());
                } else {
                    throw new RuntimeException("Unknown HTTP method name: "
                            + httpMethod);
                }
        
                httpRequest.addHeader(header);
                return httpRequest;
            }
        
            @Override
            public void close() {
                try {
                    if (client != null) {
                        client.close();
                    }
                } catch (IOException e) {
                    // It is recommended to add logs in this place.
                    e.printStackTrace();
                }
            }
        
        }
        ```

        **Demo.java:**

        ```
        package com.cloud.apigateway.sdk.demo;
        
        import java.io.BufferedReader;
        import java.io.ByteArrayInputStream;
        import java.io.IOException;
        import java.io.InputStream;
        import java.io.InputStreamReader;
        import java.net.MalformedURLException;
        import java.net.URL;
        
        import org.apache.http.HttpResponse;
        
        import com.cloud.sdk.http.HttpMethodName;
        
        
        public class Demo {
        
            public static void main(String[] args) {
        
                //replace real AK
                String ak = "akString";
                //replace real SK
                String sk = "skString";
        
                // get method
                //replace real url. do not forget URL encoding if needed
                String url = "urlString";
                get(ak, sk, url);
        
                // post method
                //replace real url. do not forget URL encoding if needed
                String postUrl = "urlString";
                //replace real body
                String postbody = "bodyString";
                post(ak, sk, postUrl, postbody);
        
                // put method
                //replace real body
                String putbody = "bodyString";
                //replace real url. do not forget URL encoding if needed
                String putUrl = "urlString";
                put(ak, sk, putUrl, putbody);
        
                // delete method
                //replace real url. do not forget URL encoding if needed
                String deleteUrl = "urlString";
                delete(ak, sk, deleteUrl);
            }
        
            public static void put(String ak, String sk, String requestUrl,
                                   String putBody) {
        
                AccessService accessService = null;
                try {
                    accessService = new AccessServiceImpl(ak, sk);
                    URL url = new URL(requestUrl);
                    HttpMethodName httpMethod = HttpMethodName.PUT;
        
                    InputStream content = new ByteArrayInputStream(putBody.getBytes());
                    HttpResponse response = accessService.access(url, content,
                            (long) putBody.getBytes().length, httpMethod);
        
                    System.out.println(response.getStatusLine().getStatusCode());
        
        
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
        
            }
        
            public static void patch(String ak, String sk, String requestUrl,
                                     String putBody) {
        
                AccessService accessService = null;
                try {
                    accessService = new AccessServiceImpl(ak, sk);
                    URL url = new URL(requestUrl);
                    HttpMethodName httpMethod = HttpMethodName.PATCH;
                    InputStream content = new ByteArrayInputStream(putBody.getBytes());
                    HttpResponse response = accessService.access(url, content,
                            (long) putBody.getBytes().length, httpMethod);
        
                    System.out.println(convertStreamToString(response.getEntity()
                            .getContent()));
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
        
            }
        
            public static void delete(String ak, String sk, String requestUrl) {
        
                AccessService accessService = null;
        
                try {
                    accessService = new AccessServiceImpl(ak, sk);
                    URL url = new URL(requestUrl);
                    HttpMethodName httpMethod = HttpMethodName.DELETE;
        
                    HttpResponse response = accessService.access(url, httpMethod);
                    System.out.println(convertStreamToString(response.getEntity()
                            .getContent()));
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
        
            }
        
            public static void get(String ak, String sk, String requestUrl) {
        
                AccessService accessService = null;
        
                try {
                    accessService = new AccessServiceImpl(ak, sk);
                    URL url = new URL(requestUrl);
                    HttpMethodName httpMethod = HttpMethodName.GET;
                    HttpResponse response;
                    response = accessService.access(url, httpMethod);
                    System.out.println(convertStreamToString(response.getEntity()
                            .getContent()));
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
        
            }
        
            public static void post(String ak, String sk, String requestUrl,
                                    String postbody) {
        
                AccessService accessService = new AccessServiceImpl(ak, sk);
                URL url = null;
                try {
                    url = new URL(requestUrl);
                } catch (MalformedURLException e) {
                    e.printStackTrace();
                }
                InputStream content = new ByteArrayInputStream(postbody.getBytes());
                HttpMethodName httpMethod = HttpMethodName.POST;
                HttpResponse response;
        
                try {
                    response = accessService.access(url, content,
                            (long) postbody.getBytes().length, httpMethod);
                    System.out.println(convertStreamToString(response.getEntity()
                            .getContent()));
                } catch (Exception e) {
                    e.printStackTrace();
                } finally {
                    accessService.close();
                }
            }
        
            private static String convertStreamToString(InputStream is) {
                BufferedReader reader = new BufferedReader(new InputStreamReader(is));
                StringBuilder sb = new StringBuilder();
        
                String line = null;
                try {
                    while ((line = reader.readLine()) != null) {
                        sb.append(line + "\n");
                    }
                } catch (IOException e) {
                    e.printStackTrace();
                } finally {
                    try {
                        is.close();
                    } catch (IOException e) {
                        e.printStackTrace();
                    }
                }
        
                return sb.toString();
            }
        
        }
        ```



