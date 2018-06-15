# CheckTransferInFeasibility {#concept_srq_nyk_c2b .concept}

CheckTransferInFeasibility: verifies that the domain name can be transferred in.

## Request parameters {#section_dbg_3nl_c2b .section}

|Parameters|Type|Required|Sample value|Description|
|:---------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|TransferAuthorizationCode|String|No|test|Transfer authorization code.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_q2n_lnl_c2b .section}

|Parameters|Type|Sample value|Description|
|:---------|:---|:-----------|:----------|
|RequestId|String|FC0D6B89-2353-4D64-BD80-6606A7DBD7C1|The unique request ID.|
|CanTransfer|Boolean|false|Whether the domain name can be transferred in.|
|Code|String|CheckTransferResult.DomainTransferProhibited|Error code returned when the domain name cannot be transferred in.|
|Message|String|This domain name is in transfer prohibited status, so it cannot be transferred. You can contact your original registrar to change its status.|Description of the error that does not allow the domain name transfer.|
|ProductId|String|2a|Product ID.|

## Examples {#section_of5_373_b2b .section}

**Request example**

```
/? Action=CheckTransferInFeasibility
&DomainName=test.com
&TransferAuthorizationCode=test
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <CheckTransferInFeasibilityResponse>
      <RequestId>60D2283F-36EA-46D4-A38D-15B5A2C455E3</RequestId>
      <CanTransfer>true</CanTransfer>
      <ProductId>2a</ProductId>
    </CheckTransferInFeasibilityResponse>
    ```

-   JSON format

    ```
    {
        "CanTransfer":true,
        "ProductId":"2a",
        "RequestId":"CE82EB4C-882D-430B-A908-E0BECFC35025"
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>390373FE-12C8-40F2-A906-AEEB5525CE54</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingDomainName</Code>
      <Message>DomainName is mandatory for this action.</Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingDomainName&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code": "missingdomainname ",
        "HostId":"domain.aliyuncs.com",
        "Message":"DomainName is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingDomainName&source=PopGw",
        "RequestId":"F931CD4D-9EF6-4DDC-AFBD-A1C026B97133"
    }
    ```


## Error codes {#section_nwb_373_b2b .section}

[See error codes of this product.](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

