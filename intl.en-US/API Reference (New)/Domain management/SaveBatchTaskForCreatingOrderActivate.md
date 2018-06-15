# SaveBatchTaskForCreatingOrderActivate {#concept_yjw_zyk_c2b .concept}

The SaveBatchTaskForCreatingOrderActivate API submits bulk domain name registration tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_zvk_k1n_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveBatchTaskForCreatingOrderActivate.|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|
|OrderActivateParam|[OrderActivateParamType](#table_ftr_s1n_c2b)|Yes|List of subtasks.|

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|DomainName|String|Yes|Domain name.|
|SubscriptionDuration|Integer|No|Purchase duration, in years. The default purchase duration is one year.|
|RegistrantProfileId|Long|Yes|ID of the domain name information template.|
|EnableDomainProxy|Boolean|No|Whether to enable the Domain Name Proxy Service. The default value is True.|
|PermitPremiumActivation|Boolean|No|Whether to enable registration of premium domain names. The default value is False.|
|AliyunDns|Boolean|No|Whether to use Alibaba Cloud DNS. The default value is True. When using a non-Alibaba Cloud DNS, first check that this DNS is valid, or else this can cause registration to fail.|
|Dns1|String|When using Alibaba Cloud DNS, you do not need to enter this parameter. When using a non-Alibaba Cloud DNS, you must enter this parameter.|Custom DNS 1.|
|Dns2|String|When using Alibaba Cloud DNS, you do not need to enter this parameter. When using a non-Alibaba Cloud DNS, you must enter this parameter.|Custom DNS 2.|
|Country|String|You do not need to enter this parameter when using an information template to register a domain name.|Country code, such as CN.|
|RegistrantOrganization|String|You do not need to enter this parameter when using an information template to register a domain name.|Name of the domain name registrant.|
|RegistrantName|String|You do not need to enter this parameter when using an information template to register a domain name.|The domain name contact person.|
|Province|String|You do not need to enter this parameter when using an information template to register a domain name.|The province.|
|City|String|You do not need to enter this parameter when using an information template to register a domain name.|The city.|
|Address|String|You do not need to enter this parameter when using an information template to register a domain name.|The address.|
|PostalCode|String|You do not need to enter this parameter when using an information template to register a domain name.|The postal code.|
|TelArea|String|You do not need to enter this parameter when using an information template to register a domain name.|The country telephone code, such as 86 for China.|
|Telephone|String|You do not need to enter this parameter when using an information template to register a domain name.|The telephone number.|
|TelExt|String|You do not need to enter this parameter when using an information template to register a domain name.|The telephone extension number.|
|RegistrantType|String|You do not need to enter this parameter when using an information template to register a domain name.|Type of the domain name registrant,  with the following enumerated values: 1: individual; 2: enterprise or organization.|
|Email|String|You do not need to enter this parameter when using an information template to register a domain name.|The email address.|

## Response parameters {#section_mck_nbn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_o4b_qbn_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_c5f_sbn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveBatchTaskForCreatingOrderActivate
&OrderActivateParam. 1. DomainName=test.com
&OrderActivateParam. 1. PermitPremiumActivation=true
&OrderActivateParam. 1. RegistrantProfileId=000000
&OrderActivateParam. 1. SubscriptionDuration=1
&OrderActivateParam. 2. DomainName=alibabacloud.com
&OrderActivateParam. 2. EnableDomainProxy=true
&OrderActivateParam. 2. PermitPremiumActivation=false
&OrderActivateParam. 2. RegistrantProfileId=000000
&OrderActivateParam. 2. SubscriptionDuration=1
&OrderActivateParam. 3. DomainName=aliyun.com
&OrderActivateParam. 3. EnableDomainProxy=false
&OrderActivateParam. 3. PermitPremiumActivation=false
&OrderActivateParam. 3. RegistrantProfileId=000000
&OrderActivateParam. 3. SubscriptionDuration=1
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForCreatingOrderActivateResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveBatchTaskForCreatingOrderActivateResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


