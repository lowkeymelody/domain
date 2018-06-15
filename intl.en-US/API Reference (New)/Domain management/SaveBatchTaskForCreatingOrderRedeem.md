# SaveBatchTaskForCreatingOrderRedeem {#concept_p44_1zk_c2b .concept}

The SaveBatchTaskForCreatingOrderRedeem API submits bulk domain name redemption tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_zmv_kcn_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveBatchTaskForCreatingOrderRedeem.|
|OrderRedeemParam|[OrderRedeemParamType](#table_zxj_pcn_c2b)|Yes| List of subtasks.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|DomainName|String|Yes|Domain name.|
|CurrentExpirationDate|Long|Yes|Current expiration time of the domain name, expressed by the number of milliseconds between the expiration time and the UTC time 00:00 on January 1, 1970.|

## Response parameters {#section_yfp_1dn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_fs1_2dn_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_csc_hdn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveBatchTaskForCreatingOrderRedeem
&OrderRedeemParam. 1. DomainName=test1.com
&OrderRedeemParam. 1. CurrentExpirationDate=000000
&OrderRedeemParam. 2. DomainName=test2.com
&OrderRedeemParam. 2. CurrentExpirationDate=000000
&OrderRedeemParam. 3. DomainName=test3.com
&OrderRedeemParam. 3. CurrentExpirationDate=000000
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForCreatingOrderRedeemResponse>
        <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
        <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
    </SaveBatchTaskForCreatingOrderRedeemResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
      "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
    }
    ```


