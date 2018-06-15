# SaveSingleTaskForDomainNameProxyService {#concept_yb2_3ds_b2b .concept}

The SaveSingleTaskForDomainNameProxyService API submits a task of the domain name privacy protection service. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_hcj_qds_b2b .section}

For more information about public request parameters, see  [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForDomainNameProxyService.|
|DomainName|string|Yes|Domain name.|
|Status|Boolean|Yes|Whether the service is enabled. The value true indicates that the service is enabled, and the value false indicates that the service is disabled.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_i5y_5ds_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_mn5_yds_b2b .section}

|Error code|Description| HTTP status code| Semantics|
|:---------|:----------|:----------------|:---------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_xwq_d2s_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForDomainNameProxyService
&DomainName=test1.com
&Status=false
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForDomainNameProxyServiceResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveSingleTaskForDomainNameProxyServiceResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


