# VerifyEmail {#concept_yhk_mrp_b2b .concept}

The VerifyEmail API verifies the email token.

## Request parameters {#section_cbr_jtq_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to VerifyEmail.|
|Token|String|Yes|Token received in the email.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_szd_stq_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|

## Error codes {#section_itv_5tq_b2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_jmz_wtq_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=VerifyEmail
&Email=test@aliyun.com
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <VerifyEmailResponse>
        <RequestId>FD3AD289-83EE-4E32-803A-CF1B3A8EEE64</RequestId>
    </VerifyEmailResponse>
    ```

-   JSON format

    ```
    {
        "requestId":"6ED795BD-192E-4921-B8E5-1BCA6F71186C"
    }
    ```


