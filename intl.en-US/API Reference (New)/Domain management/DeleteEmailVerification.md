# DeleteEmailVerification {#concept_ur1_mjq_b2b .concept}

The DeleteEmailVerification API deletes verified email addresses. After a verified email address is deleted, it must be verified again.

## Request parameters {#section_jtz_h4l_c2b .section}

For more information about public request parameters, see [public parameters](reseller.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes| API of the action, system required parameter. Set this parameter to DeleteEmailVerification.|
|Email|String|Yes|Email address. Use commas \(,\) to separate multiple email addresses.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en  \(English\). The default value is en.|

## Response parameters {#section_oyr_m4l_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|SuccessList|[SendResultType](#table_l15_q4l_c2b)|Delete the successful list.|
|FailList|[SendResultType](#table_l15_q4l_c2b)|Delete the failure list.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|Email|String|Email address to be verified.|
|Code|String|Return code.|
|Message|String|Response message.|

## Error codes {#section_ecg_v4l_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|Networkioerror|Network IO Error.|400|Network I/O exception.|

## Examples {#section_bhn_bpl_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=DeleteEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <DeleteEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>test1@aliyun.com</Email>
                <Message>Parameter error</Message>
                <Code>ParameterIllegall</Code>
            </SendResult>
            <SendResult>
                <Email>test2@aliyun.com</Email>
                <Message>Parameter error</Message>
                <Code>ParameterIllegall</Code>
            </SendResult>
        </FailList>
        <RequestId>7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE</RequestId>
        <SuccessList/>
    </DeleteEmailVerificationResponse>
    ```

-   JSON format

    ```
    {
      "failList": [
        {
          "code": "ParameterIllegall",
          "email": "test1@aliyun.com",
          "message": "Parameter error"
        }
      ],
      "requestId": "B862F011-5E61-4302-88BD-A4EAA5326140",
      "successList": [
        {
          "email": "test2@aliyun.com"
        }
      ]
    }
    ```


