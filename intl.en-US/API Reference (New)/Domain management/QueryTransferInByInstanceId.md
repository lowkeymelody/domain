# QueryTransferInByInstanceId {#concept_b3t_wyk_c2b .concept}

QueryTransferInByInstanceId: queries domain name transfer information by instance ID.

## Request parameters {#section_ahd_f5m_c2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|InstanceId|字符串|Yes|S20181T0WLI85212|Instance ID.|
|Lang|字符串|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|字符串|No|127.0.0.1|User IP address.|

## Response parameters {#section_ahr_j5m_c2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|字符串|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The unique request ID.|
|SubmissionDate|字符串|2018-03-28 00:41:42|Transfer request submission time.|
|ModificationDate|字符串|2018-03-28 00:41:42|Transfer information update time.|
|UserId|字符串|123456|User ID.|
|InstanceId|字符串|S20181T0WLI85212|Instance ID.|
|DomainName|字符串|test.com|Domain name.|
|Status|Integer|11|Detailed domain name transfer status, with the following enumerated values:-   10 Initial status.
-   11 Email verification token link sent.
-   19 Token link verification successful.
-   20 Submitted for name verification.
-   21 Name verification failed.
-   29 Name verification successful.
-   31 Incorrect transfer authorization code.
-   39 Transfer submission successful.
-   50 Transfer cancelled by customer.
-   51 Transfer failed.
-   52 Transfer expired.
-   59 Transfer successful.

|
|SimpleTransferInStatus|字符串|SUCCESS|Transfer status, with the following enumerated values:-   INIT Transfer submitted.
-   AUTHORIZATION Transfer authorization \(email verification\).
-   NAME\_VERIFICATION Name verification.
-   PASSWORD\_VERIFICATION Transfer authorization code verification.
-   PENDING Transfer in progress.
-   SUCCESS Transfer successful.
-   FAIL Transfer failed.

|
|ResultCode|字符串|clientCancelled|The failure code returned when a transfer fails, with the following enumerated values:-   clientCancelled You cancelled this transfer.
-   clientRejected The original domain name registrar rejected the transfer \(or you rejected the operation at the original registrar\).
-   serverCancelled The registry cancelled the transfer.
-   transferProhibited The domain name status does not permit a transfer.
-   transferExpired You did not complete the transfer within the effective period.
-   nameVerificationFailed The domain name did not pass name verification.
-   transferSubmitted Another user has already submitted a domain name transfer.

|
|ResultDate|字符串|2018-03-28 00:41:42|Time of transfer success or failure.|
|ResultMsg|字符串|You have cancelled this domain name transfer|The transfer description returned when a transfer fails.|
|TransferAuthorizationCodeSubmissionDate|字符串|2018-03-28 00:41:42|Transfer authorization code submission time.|
|NeedMailCheck|Boolean|true|Whether email verification is required.|
|Email|字符串|test@test.com|The address to which the domain name transfer confirmation email is sent.|
|WhoisMailStatus|Boolean|true|Whether the domain name registrant’s email is crawled by WHOIS. If this field is false for an authorized domain name transfer \(email verification\), it indicates that the registrant’s email is not crawled by WHOIS and must be manually entered.|
|ExpirationDate|字符串|2018-03-28 00:41:42|Domain name transfer expiration time.|
|ProgressBarType|Integer|0|The transfer progress bar type, with the following enumerated values:-   0 Requires both email verification and name verification.
-   1 Requires email verification, but not name verification.
-   2 Requires name verification, but not email verification.
-   3 Does not require email verification or name verification.

|
|SubmissionDateLong|Long|1514428524669|Transfer request submission timestamp.|
|ModificationDateLong|Long|1514428524669|Transfer information update timestamp.|
|Resultdatelong|Long|1514428524669|Timestamp of transfer success or failure.|
|ExpirationDateLong|Long|1514428524669|Domain name transfer expiration timestamp.|
|TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|Transfer authorization code submission timestamp.|

## Examples {#section_of5_389_b2b .section}

**Request example**

```
/? Action=QueryTransferInByInstanceId
&InstanceId=S20181T0WLI85212
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <QueryTransferInByInstanceIdResponse>
      <InstanceId>S20182F0RED000000</InstanceId>
      <WhoisMailStatus>true</WhoisMailStatus>
      <UserId>123456</UserId>
      <ResultDate>2018-03-28 09:54:39</ResultDate>
      <ExpirationDate>2018-04-12 09:51:53</ExpirationDate>
      <NeedMailCheck>true</NeedMailCheck>
      <Status>50</Status>
      <Email/>
      <SimpleTransferInStatus>FAIL</SimpleTransferInStatus>
      <ResultMsg>You have canceled this domain name transfer in.</ResultMsg>
      <RequestId>0D6108ED-7BB3-4898-83D0-44883DE0D3E7</RequestId>
      <ModificationDate>2018-03-28 09:54:39</ModificationDate>
      <ResultCode>clientCancelled</ResultCode>
      <DomainName>test.com</DomainName>
      <ProgressBarType>0</ProgressBarType>
      <SubmissionDate>2018-03-28 09:51:53</SubmissionDate>
    </QueryTransferInByInstanceIdResponse>
    ```

-   JSON format

    ```
    {
        "DomainName":"test.com",
        "Email":"",
        "ExpirationDate":"2018-04-12 09:51:53",
        "InstanceId":"S20182F0RED000000",
        "ModificationDate":"2018-03-28 09:54:39",
        "NeedMailCheck":true,
        "ProgressBarType":0,
        "RequestId":"B3E437A1-4947-4E4F-B9E2-9781AB1C8134",
        "ResultCode":"clientCancelled",
        "ResultDate":"2018-03-28 09:54:39",
        "ResultMsg":"You have canceled this domain name transfer in.",
        "SimpleTransferInStatus":"FAIL",
        "Status":50,
        "SubmissionDate":"2018-03-28 09:51:53",
        "UserId":"123456",
        "WhoisMailStatus":true
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>41187FF2-262D-4414-8AD2-7B85D74E1385</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingInstanceId</Code>
      <Message>InstanceId is mandatory for this action.</Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingInstanceId&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"MissingInstanceId",
        "HostId":"domain.aliyuncs.com",
        "Message":"InstanceId is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingInstanceId&source=PopGw",
        "RequestId":"05973664-CD29-4CF5-8060-FAC3E2CE0D87"
    }
    ```


## Error code {#section_nwb_389_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

