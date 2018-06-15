# TransferInResendMailToken {#concept_zg3_4rp_b2b .concept}

The TransferInResendMailToken API resends the verification email for a domain name transfer.

## Request parameters {#section_pmj_xcr_b2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|Lang|String|No|en|Language of the information returned by the API, which has the following enumerated values: zh \(Chinese\) and en  \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_z3r_ddr_b2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The unique request ID.|

## Examples {#section_of5_qbr_b2b .section}

**Request example**

```
/? Action=TransferInResendMailToken
&DomainName=test.com
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <TransferInResendMailTokenResponse>
      <RequestId>3E5DAABD-DED4-4624-A776-D04303F24C9A</RequestId>
    </TransferInResendMailTokenResponse>
    ```

-   JSON format

    ```
    { "RequestId":"F7C42D02-2FBE-475A-85A2-872865926EDC"}
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>9B895799-50AC-4ADD-86B9-028A8DBCDE5C</RequestId>
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
        "RequestId":"2B74BA5F-B3EB-403C-B682-7AE6C7F97F6F"
    }
    ```


## Error code {#section_nwb_jcr_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

