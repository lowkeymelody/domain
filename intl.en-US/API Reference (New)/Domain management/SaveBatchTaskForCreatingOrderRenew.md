# SaveBatchTaskForCreatingOrderRenew {#concept_vs3_bzk_c2b .concept}

The SaveBatchTaskForCreatingOrderRenew API submits bulk domain name renewal tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_sdm_12n_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveBatchTaskForCreatingOrderRenew.|
|OrderRenewParam|[OrderRenewParamType](#table_fnv_g2n_c2b)|Yes|List of subtasks.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en  \(English\). The default value is en.|

|Parameter|Type|Required?|Description|
|:--------|:---|:--------|:----------|
|DomainName|String|Yes|Domain name.|
|CurrentExpirationDate|Long|Yes|Current expiration time of the domain name, expressed by the number of milliseconds between the expiration time and the UTC time 00:00 on January 1, 1970.|
|SubscriptionDuration|Integer|Yes|Renewal period, in years.|

## Response parameters {#section_h1f_n2n_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_q4b_q2n_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network Io error.|400|Network I/O exception.|

## Examples {#section_tql_s2n_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveBatchTaskForCreatingOrderRenew
&OrderRenewParam. 1. DomainName=test1.com
&OrderRenewParam. 1. SubscriptionDuration=1
&OrderRenewParam. 1. CurrentExpirationDate=0000
&OrderRenewParam. 2. DomainName=test2.com
&OrderRenewParam. 2. SubscriptionDuration=2
&OrderRenewParam. 2. CurrentExpirationDate=0000
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForCreatingOrderRenewResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveBatchTaskForCreatingOrderRenewResponse>
    ```

-   JSON format

    ```
    {
      "requestId": "9DFBA504-3C59-427D-907D-B6C61F2A3A27",
      "taskNo": "2daff10d-c284-4b98-a6f4-796148116b2b"
    }
    ```


