# SaveBatchTaskForTransferProhibitionLock {#concept_odl_2zk_c2b .concept}

The SaveBatchTaskForTransferProhibitionLock API submits bulk transfer prohibition lock tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_o1c_yjn_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveBatchTaskForTransferProhibitionLock.|
|DomainName|[DomainNameListType](#table_bs1_ckn_c2b)|Yes|Domain name list.|
|Status|Boolean|Yes| Whether the service is enabled. The value true indicates that the service is enabled, and the value false indicates that the service is disabled.|
|Lang|String|No| Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\).  The default value is en.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|domainName|String|Domain name.|

## Response parameters {#section_an4_2kn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_ly4_jkn_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_f1h_3kn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveBatchTaskForTransferProhibitionLock
&DomainName. 1=test1.com
&DomainName. 2=test2.com
&DomainName. 3=test3.com
&Status=false
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForTransferProhibitionLockResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveBatchTaskForTransferProhibitionLockResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


