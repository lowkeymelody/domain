# SaveSingleTaskForSynchronizingDnsHost {#concept_jtb_nzr_b2b .concept}

The SaveSingleTaskForSynchronizingDnsHost API submits a DNS host synchronization task. This API can be used to handle problems of missing and inconsistent DNS hosts. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_pgv_rzr_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForSynchronizingDnsHost.|
|InstanceId|String|Yes| Instance ID. You can query it by using [QueryDomainList](intl.en-US/API Reference (New)/Domain management/QueryDomainList.md#) API.|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Return parameters { .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|The unique request ID.|
|TaskNo|String| Task ID.|

## Error codes { .section}

|Error code|Description|HTTP status code |Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400| Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|An action is being processed for the domain name. Try again later.|

## Examples {#section_vxj_j1s_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveSingleTaskForSynchronizingDnsHost
&InstanceId=ST2017120814571100001303
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForSynchronizingDnsHostResponse>
    <TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
    <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
    </SaveSingleTaskForSynchronizingDnsHostResponse>
    ```

-   JSON format

    ```
    {
      "requestId": "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
      "taskNo": "e9b8e8b4-7334-4548-9cec-c30b6891f292"
    }
    ```


