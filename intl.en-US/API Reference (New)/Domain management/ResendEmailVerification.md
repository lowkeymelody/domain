# ResendEmailVerification {#concept_dhd_zyk_c2b .concept}

ResendEmailVerification: resends verification emails.

## Request parameters {#section_dbr_dzm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The API name, a required parameter. Set this parameter to ResendEmailVerification.|
|Email|String|Yes|Email address. Use commas \(,\) to separate multiple email addresses.|
|Lang|String|No|Language of the information returned from the API, which has the following enumerated values: zh\(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_zp1_3zm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|SuccessList|[SendResultType](#table_ltc_lzm_c2b)|Success list.|
|FailList|SendResultType|Failure list.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|Email|String|Email address to be verified.|
|Code|String|Return code.|
|Message|String|Response message.|

## Error codes {#section_n1h_rzm_c2b .section}

|Error code|Description| HTTP status code|Meaning|
|:---------|:----------|----------------:|:------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_mdg_tzm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=ResendEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<Public request parameter>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <ResendEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>test1@aliyun.com</Email>
                <Message>The maximum number of attempts allowed to send the email verification link is exceeded.</Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
            <SendResult>
                <Email>test2@aliyun.com</Email>
                <Message>The maximum number of attempts allowed to send the email verification link is exceeded.</Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
        </FailList>
        <RequestId>0EA54E99-DB48-4CE3-A099-6ED8E451B8AC</RequestId>
        <SuccessList/>
    </ResendEmailVerificationResponse>
    ```

-   JSON format

    ```
    {
      "failList": [
        {
          "code": "SendTokenQuotaExceeded",
          "email": "test1@aliyun.com",
          "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
        },
        {
          "code": "ParameterIllegall",
          "email": "test2@aliyun.com",
          "message": "Parameter error"
        }
      ],
      "requestId": "8D93B5EC-09D5-43C3-A5ED-AFBC6A98DDDF",
      "successList": []
    }
    ```


