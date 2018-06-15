# SaveSingleTaskForTransferProhibitionLock {#concept_ff5_mxr_b2b .concept}

The SaveSingleTaskForTransferProhibitionLock API submits a transfer prohibition lock task. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_ltc_5xr_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForTransferProhibitionLock.|
|DomainName|String|Yes|Domain name.|
|Status|Boolean|Yes|Whether the lock is enabled. The value true indicates that the lock is enabled, and the value false indicates that the lock is disabled.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_fk4_tyr_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier|
|TaskNo|String|Task ID.|

## Error codes {#section_ggp_wyr_b2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples { .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveSingleTaskForTransferProhibitionLock
&DomainName=test1.com
&Status=false
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForTransferProhibitionLockResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveSingleTaskForTransferProhibitionLockResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


