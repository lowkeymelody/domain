# TransferInReenterTransferAuthorizationCode {#concept_w33_qrp_b2b .concept}

The TransferInReenterTransferAuthorizationCode API re-enters the authorization code for a domain name transfer.

## Request parameters {#section_m4v_3kr_b2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|TransferAuthorizationCode|String|Yes|testCode|The transfer authorization code.|
|Lang|String|No|en| Language of the information returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_ufg_tkr_b2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The unique request ID.|

## Examples {#section_of5_424_b2b .section}

**Request example**

```
/? Action=TransferInReenterTransferAuthorizationCode
&DomainName=test.com
&TransferAuthorizationCode=testCode
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <TransferInReenterTransferAuthorizationCodeResponse>
      <RequestId>A8734DAA-56BB-4181-825E-8EE1F0C85DF4</RequestId>
    </TransferInReenterTransferAuthorizationCodeResponse>
    ```

-   JSON format

    ```
    {
        "RequestId":"F7C42D02-2FBE-475A-85A2-872865926EDC"
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>F367C925-88F9-4297-A604-0ACDD1E8D5D4</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>DomainTransferPendingNotExist</Code>
      <Message>The domain name is not currently being transferred in.</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"DomainTransferPendingNotExist",
        "HostId":"domain.aliyuncs.com",
        "Message":"The domain name is not currently being transferred in.",
        "RequestId":"20E291F8-A08C-4999-93B8-5C16B8F49B87"
    }
    ```


## Error code {#section_nwb_424_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

