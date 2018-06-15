# SaveSingleTaskForCreatingOrderRedeem {#concept_tl1_jsp_b2b .concept}

The SaveSingleTaskForCreatingOrderRedeem API submits a domain name redemption task. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_irp_dwn_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForCreatingOrderRedeem.|
|DomainName|String|Yes|Domain name.|
|CurrentExpirationDate|Long|Yes| Current expiration time of the domain name, expressed by the number of milliseconds between the expiration time and the UTC time 00:00 on January 1, 1970.|
|Lang|String|No| Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_wdq_fwn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_vwy_lwn_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|An action is being processed for the domain name. Try again later.|

## Examples {#section_ebr_pwn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForCreatingOrderRedeem
&CurrentExpirationDate=0000
&DomainName=test.com
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForCreatingOrderRedeemResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveSingleTaskForCreatingOrderRedeemResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


