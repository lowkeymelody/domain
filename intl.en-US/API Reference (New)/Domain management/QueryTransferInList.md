# QueryTransferInList {#concept_ikn_xyk_c2b .concept}

QueryTransferInList: queries the list of inbound domain name transfers.

## Request parameters {#section_ymr_1wm_c2b .section}

|Parameters|Type|Required|Sample value|Description|
|:---------|:---|:-------|:-----------|:----------|
|PageNum|Integer|Yes|1|Page number.|
|PageSize|Integer|Yes|20|Page size.|
|DomainName|String|No|test.com|Domain name, prefix match.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en  \(English\). The default value is en.|
|SimpleTransferInStatus|String|No|INIT|Transfer status, with the following enumerated values:-   INIT Transfer submitted.
-   AUTHORIZATION Transfer authorization \(email verification\).
-   NAME\_VERIFICATION Name verification.
-   PASSWORD\_VERIFICATION Transfer authorization code verification.
-   PENDING Transfer in progress.
-   SUCCESS Transfer successful.
-   FAIL Transfer failed.

|
|SubmissionEndDate|Long|No|1514428524669|Transfer submission start time.|
|Submissionary startdate|Long|No|1514428524669|Transfer submission end time.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_qbh_fwm_c2b .section}

|Parameters|Type|Sample value|Description|
|:---------|:---|:-----------|:----------|
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The unique request ID.|
|TotalItemNum|Integer|40|Total number of entries.|
|CurrentPageNum|Integer|1|Current page number.|
|TotalPageNum|Integer|2|Total number of pages.|
|PageSize|Integer|20|Page size.|
|PrePage|Boolean|false|Whether the previous page exists.|
|NextPage|Boolean|true|Whether the next page exists.|
|Data|TransferInInfo|TransferInInfo|Inbound domain name transfer information list.|

|Parameters|Type|Sample value|Description|
|:---------|:---|:-----------|:----------|
| SubmissionDate|String|2018-03-28 00:41:42|Transfer request submission time.|
|  ModificationDate|String|2018-03-28 00:41:42|Transfer information update time.|
|  UserId|String|123456|User ID.|
|  InstanceId|String|S20181T0WLI85212|Instance ID.|
|The domain domainname|String|test.com|Domain name.|
| Status|Integer|11|Detailed domain name transfer status, with the following enumerated values:-   10 Initial status.
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
|  SimpleTransferInStatus|String|FAIL|Transfer status, with the following enumerated values:-   INIT Transfer submitted.
-   AUTHORIZATION Transfer authorization \(email verification\).
-   NAME\_VERIFICATION Name verification.
-   PASSWORD\_VERIFICATION Transfer authorization code verification.
-   PENDING Transfer in progress.
-   SUCCESS Transfer successful.
-   FAIL Transfer failed.

|
|  ResultCode|String|clientCancelled|The failure code returned when a transfer fails, with the following enumerated values:-   clientCancelled You cancelled this transfer.
-   clientRejected The original domain name registrar rejected the transfer \(or you rejected the operation at the original registrar\).
-   serverCancelled The registry cancelled the transfer.
-   transferProhibited The domain name status does not permit a transfer.
-   transferExpired You did not complete the transfer within the effective period.
-   nameVerificationFailed The domain name did not pass name verification.
-   transferSubmitted Another user has already submitted a domain name transfer.

|
| ResultDate|String|2018-03-28 00:41:42|Time of transfer success or failure.|
|  ResultMsg|String|You have cancelled this domain name transfer|The transfer description returned when a transfer fails.|
|  TransferAuthorizationCodeSubmissionDate|String|2018-03-28 00:41:42|Transfer authorization code submission time.|
|  NeedMailCheck|Boolean|true|Whether email verification is required.|
|  Email|String|test@test.com|The address to which the domain name transfer confirmation email is sent.|
|  WhoisMailStatus|Boolean|true|Whether the domain name registrant’s email is crawled by WHOIS. When this field is false for an authorized domain name transfer \(email verification\), it indicates that the registrant’s email is not crawled by WHOIS and must be manually entered.|
|  ExpirationDate|String|2018-03-28 00:41:42|Domain name transfer expiration time.|
|  ProgressBarType|Integer|0|The transfer progress bar type, with the following enumerated values:-   0 Requires both email verification and name verification.
-   1 Requires email verification, but not name verification.
-   2 Requires name verification, but not email verification.
-   3 Does not require email verification or name verification.

|
| SubmissionDateLong|Long|1514428524669|Transfer request submission timestamp.|
| ModificationDateLong|Long|1514428524669|Transfer information update timestamp.|
|  ResultDateLong|Long|1514428524669|Timestamp of transfer success or failure.|
|  ExpirationDateLong|Long|1514428524669|Domain name transfer expiration timestamp.|
|  TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|Transfer authorization code submission timestamp.|

## Examples {#section_of5_390_b2b .section}

**Request example**

```
/? Action=QueryTransferInList
&PageNum=1
&PageSize=20
&DomainName=test.com
&SimpleTransferInStatus=INIT
&SubmissionEndDate=1514428524669
&SubmissionStartDate=1514428524669
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <QueryTransferInListResponse>
      <Data>
        <TransferInInfo>
          <Status>31</Status>
          <Email>te****st@alibaba-inc.com</Email>
          <ResultMsg>TransferInFailureReason.null</ResultMsg>
          <SimpleTransferInStatus>PASSWORD_VERIFICATION</SimpleTransferInStatus>
          <InstanceId>S20182G180111111</InstanceId>
          <ModificationDate>2018-03-29 16:31:02</ModificationDate>
          <DomainName>test.com</DomainName>
          <WhoisMailStatus>true</WhoisMailStatus>
          <UserId>123456</UserId>
          <ProgressBarType>0</ProgressBarType>
          <ExpirationDate>2018-04-13 15:51:01</ExpirationDate>
          <NeedMailCheck>true</NeedMailCheck>
          <SubmissionDate>2018-03-29 15:51:01</SubmissionDate>
        </TransferInInfo>
        <TransferInInfo>
          <InstanceId>S20182G151111111</InstanceId>
          <WhoisMailStatus>true</WhoisMailStatus>
          <UserId>123456</UserId>
          <ResultDate>2018-03-29 15:47:37</ResultDate>
          <ExpirationDate>2018-04-13 14:57:11</ExpirationDate>
          <NeedMailCheck>true</NeedMailCheck>
          <Status>50</Status>
          <Email>b****i4@test.com</Email>
          <SimpleTransferInStatus>FAIL</SimpleTransferInStatus>
          <ResultMsg>You have canceled this domain name transfer in.</ResultMsg>
          <ModificationDate>2018-03-29 15:47:37</ModificationDate>
          <ResultCode>clientCancelled</ResultCode>
          <DomainName>btest.com</DomainName>
          <ProgressBarType>0</ProgressBarType>
          <SubmissionDate>2018-03-29 14:57:11</SubmissionDate>
        </TransferInInfo>
      </Data>
      <TotalItemNum>87</TotalItemNum>
      <PageSize>2</PageSize>
      <CurrentPageNum>1</CurrentPageNum>
      <RequestId>041FEBFE-966C-452E-A21D-38FBE520B93D</RequestId>
      <PrePage>false</PrePage>
      <TotalPageNum>44</TotalPageNum>
      <NextPage>true</NextPage>
    </QueryTransferInListResponse>
    ```

-   JSON format

    ```
    {
        "CurrentPageNum":1,
        "Data":{
            "TransferInInfo":[
                {
                    "DomainName":"test.com",
                    "Email":"te****st@alibaba-inc.com",
                    "ExpirationDate":"2018-04-13 15:51:01",
                    "InstanceId":"S20182G180111111",
                    "ModificationDate":"2018-03-29 15:59:02",
                    "NeedMailCheck":true,
                    "ProgressBarType":0,
                    "ResultMsg":"TransferInFailureReason.null",
                    "SimpleTransferInStatus":"PASSWORD_VERIFICATION",
                    "Status":31,
                    "SubmissionDate":"2018-03-29 15:51:01",
                    "UserId":"123456",
                    "WhoisMailStatus":true
                },
                {
                    "DomainName":"btest.com",
                    "Email":"b****i4@test.com",
                    "ExpirationDate":"2018-04-13 14:57:11",
                    "InstanceId":"S20182G15000000",
                    "ModificationDate":"2018-03-29 15:47:37",
                    "NeedMailCheck":true,
                    "ProgressBarType":0,
                    "ResultCode":"clientCancelled",
                    "ResultDate":"2018-03-29 15:47:37",
                    "ResultMsg":"You have canceled this domain name transfer in.",
                    "SimpleTransferInStatus":"FAIL",
                    "Status":50,
                    "SubmissionDate":"2018-03-29 14:57:11",
                    "UserId":"123456",
                    "WhoisMailStatus":true
                }
            ]
        },
        "NextPage":true,
        "PageSize":2,
        "PrePage":false,
        "RequestId":"CC71762B-0A20-4D3A-AD74-C225DB8DBEAE",
        "TotalItemNum":87,
        "TotalPageNum":44
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>773FF621-FAF1-40C4-93F6-800AD2AEEF75</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingPageNum</Code>
      <Message>PageNum is mandatory for this action.</Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingPageNum&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"MissingPageNum",
        "HostId":"domain.aliyuncs.com",
        "Message":"PageNum is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingPageNum&source=PopGw",
        "RequestId":"1489D619-4051-4CA0-92DD-B57A89E125D2"
    }
    ```


## Error code {#section_nwb_390_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

