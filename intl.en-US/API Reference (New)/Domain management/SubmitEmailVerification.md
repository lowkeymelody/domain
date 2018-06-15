# SubmitEmailVerification {#concept_s3f_2mr_b2b .concept}

According to the ICANN policies and regulations, the email address of a domain name owner must be verified. The SubmitEmailVerification API submits email address verification task.

## Request parameters {#section_wy4_pmr_b2b .section}

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SubmitEmailVerification.|
|Email|String|Yes|Email address. Use commas \(,\) to separate multiple email addresses.|
|SendIfExist|Boolean|Yes|Whether to repeatedly send the verification email if the verification record already exists|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_u1p_wmr_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|SuccessList|[SendResultType](#table_ecg_2nr_b2b)|The success list is sent.|
|FailList|[SendResultType](#table_ecg_2nr_b2b)|The failure list is sent.|
|ExistList|[SendResultType](#table_ecg_2nr_b2b)|A list already exists.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|Email|String|Email address to be verified.|
|Code|String|Return code.|
|Message|String| Response message.|

## Error codes {#section_tmt_ynr_b2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network Io error.|400|Network I/O exception.|

## Examples {#section_lpr_34r_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SubmitEmailVerification
&InstanceId=ST2017120814571100001303
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SubmitEmailVerificationResponse>
        <FailList>
            <SendResult>
                <Email>aaa@test.com</Email>
                <Message>The maximum number of attempts allowed to send the email
                    verification link is exceeded.
                </Message>
                <Code>SendTokenQuotaExceeded</Code>
            </SendResult>
        </FailList>
        <RequestId>E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D</RequestId>
        <ExistList />
        <SuccessList>
            <SendResult>
                <Email>ccc@test.com</Email>
                <Message />
                <Code />
            </SendResult>
            <SendResult>
                <Email>ddd@test.com</Email>
                <Message />
                <Code />
            </SendResult>
        </SuccessList>
    </SubmitEmailVerificationResponse>
    ```

-   JSON format

    ```
    {
      "existList": [
        {
          "email": "aaa@test.com"
        }
      ],
      "failList": [
        {
          "code": "SendTokenQuotaExceeded",
          "email": "bbb@test.com",
          "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
        }
      ],
      "requestId": "2EF65AFD-A2C4-48D3-B326-ACB52B5A6771",
      "successList": [
        {
          "email": "ccc@test.com"
        },
        {
          "email": "ddd@test.com"
        }
      ]
    }
    ```


