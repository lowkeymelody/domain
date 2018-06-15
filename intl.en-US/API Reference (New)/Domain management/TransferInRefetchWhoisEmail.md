# TransferInRefetchWhoisEmail {#concept_dy3_prp_b2b .concept}

TransferInRefetchWhoisEmail: During email verification for a domain name transfer, the system automatically crawls WHOIS emails if the registrant’s email on WHOIS is incorrect or cannot be obtained.

## Request parameters {#section_ymj_42r_b2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_ksw_pjr_b2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The unique request ID.|

## Examples {#section_of5_qbr_b2b .section}

**Request example**

```
/? Action=TransferInRefetchWhoisEmail
&DomainName=test.com
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <TransferInRefetchWhoisEmailResponse>
      <RequestId>9625281F-1176-4F57-ACBB-3AEF6E407AFE</RequestId>
    </TransferInRefetchWhoisEmailResponse>
    ```

-   JSON format

    ```
    {
        "RequestId":"C01181CC-D03C-465F-B89F-C78B721567D0"
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>7618A307-69AD-4CC4-BC44-A898DB4FD9F4</RequestId>
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
        "RequestId":"B94591C4-3F8F-4EDB-BE09-DEBC8837D513"
    }
    ```


## Error code {#section_nwb_44cr_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

