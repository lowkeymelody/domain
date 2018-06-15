# SaveSingleTaskForCreatingOrderActivate {#concept_twq_kzk_c2b .concept}

The SaveSingleTaskForCreatingOrderActivate API submits domain name registration tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_q5w_1vn_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes| The API name, a required parameter. Set this parameter to SaveSingleTaskForCreatingOrderActivate.|
|DomainName|String|Yes|Domain name.|
|SubscriptionDuration|Integer|No|Purchase duration, in years. The default purchase duration is one year.|
|RegistrantProfileId|Long|No|ID of the domain name information template.|
|EnableDomainProxy|Boolean|No|Whether to enable the Domain Name Proxy Service. The default value is true.|
|PermitPremiumActivation|Boolean|No| Whether to enable registration of premium domain names. The default value is false.|
|Lang|String|No| Language of the error message returned from the API, which has the following enumerated values: zh \(Chinese\) and en  \(English\). The default value is en.|
|AliyunDns|Boolean|No|Whether to use Alibaba Cloud DNS. The default value is true. When using a non-Alibaba Cloud DNS, first check that this DNS is valid, or else this can cause registration to fail.|
|Dns1|String|When using Alibaba Cloud DNS, you do not need to enter this parameter. When using a non-Alibaba Cloud DNS, you must enter this parameter.|Custom DNS 1.|
|Dns2|String|When using Alibaba Cloud DNS, you do not need to enter this parameter. When using a non-Alibaba Cloud DNS, you must enter this parameter.|Custom DNS 2.|
|Country|String|You do not need to enter this parameter when using an information template to register a domain name.|Country code, such as CN.|
|RegistrantOrganization|String|You do not need to enter this parameter when using an information template to register a domain name.|Name of the domain name registrant.|
|RegistrantName|String|You do not need to enter this parameter when using an information template to register a domain name.|The domain name contact person.|
|Province|String| You do not need to enter this parameter when using an information template to register a domain name.|The province.|
|City|String|You do not need to enter this parameter when using an information template to register a domain name.|The city.|
|Address|String| You do not need to enter this parameter when using an information template to register a domain name.|The street address.|
|Postalcode|String|You do not need to enter this parameter when using an information template to register a domain name.|The postal code.|
|TelArea|String|You do not need to enter this parameter when using an information template to register a domain name.|The country telephone code, such as 86 for China.|
|Telephone|String|You do not need to enter this parameter when using an information template to register a domain name.|The telephone number.|
|TelExt|String|You do not need to enter this parameter when using an information template to register a domain name.|The telephone extension number.|
|RegistrantType|String|You do not need to enter this parameter when using an information template to register a domain name.|Type of the domain name registrant, with the enumerated values: 1 individual; 2: enterprise or organization|
|Email|String|You do not need to enter this parameter when using an information template to register a domain name.|The email address.|

## Response parameters {#section_bnh_mvn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_anc_pvn_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|An action is being processed for the domain name. Try again later.|

## Examples {#section_vvv_svn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForCreatingOrderActivate
&RegistrantProfileId=123
&DomainName=test.com
&<Public request parameter>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForCreatingOrderActivateResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveSingleTaskForCreatingOrderActivateResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
            
    ```


