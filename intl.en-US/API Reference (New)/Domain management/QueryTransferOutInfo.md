# QueryTransferOutInfo {#concept_my3_yyk_c2b .concept}

The QueryTransferOutInfo API queries outbound domain name transfer information.

## Request parameters {#section_c3t_cym_c2b .section}

|Parameters|Type|Required|Sample value|Description|
|:---------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh\(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_iv5_391_c2b .section}

|Parameters|Type|Sample value|Description|
|:---------|:---|:-----------|:----------|
|RequestId|String|BBEC5A50-DFDF-482E-8343-B4EB0105E055|The unique request ID.|
|Status|Integer|8|Transfer status, with the following enumerated values:-   1: Verify mobile phone.
-   2: Verify email.
-   3: Obtained transfer authorization code.
-   4: Transfer in progress \(received registry transfer request\).
-   5: Transfer successful.
-   8: Transfer failed.

|
|Email|String|test@test.com|Address to which the transfer authorization code email is sent.|
|TransferAuthorizationCodeSendDate|String|2018-04-13 19:57:56|Transfer authorization code retrieval time.|
|ExpirationDate|String|2018-04-13 19:57:56|Time when the obtained transfer authorization code expires.|
|PendingRequestDate|String|2018-04-13 19:57:56|Time when the registry transfer out request was received.|
|ResultCode|String|clientRejected|Code indicating the reason the transfer failed.|
|ResultMsg|String|Transfer out rejected|Description of the reason the transfer failed.|

## Examples {#section_of5_391_b2b .section}

**Request example**

```
/? Action=QueryTransferOutInfo
&DomainName=test.com
&<Public request parameter>
```

**Normal return example**

-   XML format

    ```
    <QueryTransferOutInfoResponse>
      <Status>3</Status>
      <RequestId>6F23B2C0-0355-4685-BB39-342956C5118B</RequestId>
      <TransferAuthorizationCodeSendDate>2018-03-29 19:57:56</TransferAuthorizationCodeSendDate>
      <ExpirationDate>2018-04-13 19:57:56</ExpirationDate>
    </QueryTransferOutInfoResponse>
    ```

-   JSON format

    ```
    {
        "ExpirationDate":"2018-04-13 19:57:56",
        "RequestId":"BBEC5A50-DFDF-482E-8343-B4EB0105E055",
        "Status":3,
        "TransferAuthorizationCodeSendDate":"2018-03-29 19:57:56"
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>8A7F0039-FB78-47B3-82F2-3FFEFC878A89</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>DomainNotExist</Code>
      <Message>The domain name does not exist.</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"DomainNotExist",
        "HostId":"domain.aliyuncs.com",
        "Message":"The domain name does not exist.",
        "RequestId":"DF5F9400-374F-4C25-9D2C-6FB928D00E50"
    }
    ```


## Error code {#section_nwb_391_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

