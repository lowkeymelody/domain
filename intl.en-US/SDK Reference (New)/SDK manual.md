# SDK manual {#concept_hlx_jsw_b2b .concept}

Currently, Alibaba Cloud provides SDKs in four languages: Java, Python, PHP, and C\#. The following links provide the download, installation, and usage guide for each language:

-   Java
-   Python
-   PHP
-   C\#

If you want SDKs in other languages, select a third-party SDK service.

## Quick start {#section_fzb_ptw_b2b .section}

**Java**

The following example describes how to install and use the Java SDK:

1.  On the Alibaba Cloud official website, create and manage your AccessKey.
2.  Install the SDK by using Maven.
    1.  Add the Maven library.

        ```
        <repositories>
             <repository>
                 <id>sonatype-nexus-staging</id>
                 name>Sonatype Nexus Staging</name>
                 <url>https://oss.sonatype.org/service/local/staging/deploy/maven2/</url>
                 <releases>
                     <enabled>true</enabled>
                 </releases>
                 <snapshots>
                     <enabled>true</enabled>
                 </snapshots>
             </repository>
        </repositories>
        ```

    2.  Add the JAR package dependency.

        ```
        <dependency>
         <groupId>com.aliyun</groupId>
         <artifactId>aliyun-java-sdk-domain-intl</artifactId>
             <version>1.0.0</version>
        </dependency>
        <dependency>
         <groupId>com.aliyun</groupId>
         <artifactId>aliyun-java-sdk-core</artifactId>
             <version>3.5.0</version>
        </dependency>
        ```

    3.  Sample code. The following example submits bulk domain name registration tasks:

        ```
        import java.util.ArrayList;
        import com.aliyuncs.DefaultAcsClient;
        import com.aliyuncs.IAcsClient;
        import com.aliyuncs.domain_intl.model.v20171218. SaveBatchTaskForCreatingOrderActivateRequest;
        import com.aliyuncs.domain_intl.model.v20171218. SaveBatchTaskForCreatingOrderActivateRequest.OrderActivateParam;
        import com.aliyuncs.domain_intl.model.v20171218. SaveBatchTaskForCreatingOrderActivateResponse;
        import com.aliyuncs.exceptions.ClientException;
        import com.aliyuncs.exceptions.ServerException;
        import com.aliyuncs.profile.DefaultProfile;
        import com.aliyuncs.profile.IClientProfile;
        public class DomainSdkDemo {
            private static IAcsClient client = null;
            //Initialize the client.
            static {
                String regionId = "ap-southeast-1"; //Use the region value such as "ap-southeast-1" for the domain name SDK.
                String accessKeyId = ""; // your accessKey
                String accessKeySecret = "";// your accessSecret
                IClientProfile profile = DefaultProfile.getProfile(regionId, accessKeyId, accessKeySecret);
                // If the error message "Can not find endpoint to access" is returned, add the following code:
                // DefaultProfile.addEndpoint("ap-southeast-1", "ap-southeast-1", "Domain-intl", "domain-intl.aliyuncs.com");
                client = new DefaultAcsClient(profile);
            }
            public static void main(String[] args) {
                //Initialize the request.
                SaveBatchTaskForCreatingOrderActivateRequest request = new SaveBatchTaskForCreatingOrderActivateRequest();
                // request.setProtocol(ProtocolType.HTTPS); //Specify the access protocol.
                // request.setAcceptFormat(FormatType.JSON); //Specify the return format of the API.
                // request.setMethod(MethodType.POST); //Specify the request method.
                ArrayList<OrderActivateParam> list = new ArrayList<OrderActivateParam>();
                OrderActivateParam orderActivateParam = new OrderActivateParam();
                orderActivateParam.setDomainName("yourdomain.com");
                orderActivateParam.setRegistrantProfileId(0L);
                orderActivateParam.setEnableDomainProxy(false);
                orderActivateParam.setSubscriptionDuration(1);
                orderActivateParam.setPermitPremiumActivation(false);
                list.add(orderActivateParam);
                request.setOrderActivateParams(list);
                //Call the API and resolve the result.
                try {
                    //IAcsClient provides two types of result returning. One is to call the doAction method to obtain the original API call result, that is, return the result of the HttpResponse type. The sample code is as follows:
                    //HttpResponse httpResponse = client.doAction(describeCdnServiceRequest);
                    //System.out.println(httpResponse.getUrl());
                    //System.out.println(new String(httpResponse.getContent()));
                    //Another is to call the getAcsResponse method to obtain the deserialized object. The sample code is as follows:
                    SaveBatchTaskForCreatingOrderActivateResponse response = client.getAcsResponse(request);
                    System.out.println(response.getTaskNo());
                } catch (ServerException e) {
                    e.printStackTrace();
                } catch (ClientException e) {
                    e.printStackTrace();
                }
            }
        }
        ```


