# TransferInCheckMailToken {#concept_qbg_rrp_b2b .concept}

The TransferInCheckMailToken API provides the token in the registrant verification email for domain name transfer in.

## Request parameters {#section_fhn_4lr_b2b .section}

|Parameter|Type| Required|Sample value|Description|
|:--------|:---|:--------|:-----------|:----------|
|Token|String|Yes|3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054|Token received in the email.|
|Lang|String|No|en|Language of the information returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_gbh_slr_b2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|Unique request ID.|
|SuccessList|String|test.com|List of successfully verified domain names.|
|FailList|String|test.com|List domain names that failed verification.|

## Examples {#section_of5_423_b2b .section}

**Request example**

```
/? Action=TransferInCheckMailToken
&Token=3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054
&<Public request parameter>
```

**Sample of a normal response**

-   XML format

    ```
    <TransferInCheckMailTokenResponse>
      <FailList/>
      <RequestId>C99AA313-4A94-4896-915B-4D4043C063DA</RequestId>
      <SuccessList>
        <SuccessDomain>test.com</SuccessDomain>
      </SuccessList>
    </TransferInCheckMailTokenResponse>
    ```

-   JSON format

    ```
    {
        "FailList":{
            "FailDomain":[]
        },
        "RequestId":"3E5677B5-6F55-4518-9A55-A9CE57313C9D",
        "SuccessList":{
            "SuccessDomain":["test.com"]
        }
    }
    ```


**Sample of an abnormal response**

-   XML format

    ```
    <Error>
      <RequestId>0F260AD0-67BD-44EC-AB95-F50FD0F25D16</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>TokenFailed</Code>
      <Message>Invalid email link, please get a new verification email</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"TokenFailed",
        "HostId":"domain.aliyuncs.com",
        "Message": "invalid email link, please get a new verification email ",
        "RequestId":"EA123BFB-2D07-4AB6-B6E5-28F4D64D6BD4"
    }
    ```


## Error code {#section_nwb_4423_b2b .section}

[See the error codes of the product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

