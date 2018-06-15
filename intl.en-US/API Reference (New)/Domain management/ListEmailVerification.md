# ListEmailVerification {#concept_k4m_njq_b2b .concept}

ListEmailVerification: queries the list of email address verification tasks under the current account and returns the results by page.

## Request parameters {#section_bl4_fll_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to ListEmailVerification.|
|PageNum|Integer|Yes| Page number.|
|PageSize|Integer|Yes|The page size.|
|BeginCreateTime|Long|No|Start time of the period in which the email addresses are verified, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|EndCreateTime|Long|No|End time of the period in which the email addresses are verified, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|Email|String|No|Email address to be verified.|
|VerificationStatus|Integer|No|Verification status. The enumerated values include: 0: waiting for verification; 1: successfully verified.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters { .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TotalItemNum|Integer|Total number of domain names.|
|CurrentPageNum|Integer|Current page number.|
|TotalPageNum|Integer|Total number of pages.|
|PageSize|Integer|The page size.|
|PrePage|Boolean|Whether the previous page exists|
|NextPage|Boolean|Whether the next page exists.|
|Data|[Emailverificationtype](#table_tsy_4ll_c2b)|List of email address verification tasks.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|GmtCreate|String|Creation time.|
|GmtModified|String|Update time.|
|Email|String|Email address to be verified.|
|UserId|String| User ID.|
|EmailVerificationNo|String| Email address verification ID.|
|TokenSendTime|String|Time to send the email address verification token.|
|VerificationStatus|Integer|Email address verification status. The enumerated values include: 0: Waiting for verification; 1: Successfully verified.|
|VerificationTime|String|Email address verification time.|
|SendIp|String|IP address that sends the verification email.|
|ConfirmIp|String|IP address used to confirm email address verification.|

## Error codes { .section}

|Error code|Description| HTTP status code|Meaning|
|:---------|:----------|:----------------|:------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_sff_1ml_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=ListEmailVerification
&PageNum=1
&PageSize=1
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <ListEmailVerificationResponse>
        <Data>
            <EmailVerification>
                <ConfirmIp>127.0.0.1</ConfirmIp>
                <TokenSendTime>Dec 25,2017 03:38:46</TokenSendTime>
                <Email>test1@aliyun.com</Email>
                <VerificationStatus>1</VerificationStatus>
                <SendIp>127.0.0.1</SendIp>
                <VerificationTime>Dec 25,2017 03:41:11</VerificationTime>
                <EmailVerificationNo>00000a21fd374da99d9c95b48500000</EmailVerificationNo>
                <UserId>0000</UserId>
                <GmtCreate>Dec 25,2017 03:38:46</GmtCreate>
                <GmtModified>Dec 25,2017 03:41:11</GmtModified>
            </EmailVerification>
            <EmailVerification>
                <ConfirmIp>127.0.0.1</ConfirmIp>
                <TokenSendTime>Dec 25,2017 03:35:22</TokenSendTime>
                <Email>test2@aliyun.com</Email>
                <VerificationStatus>1</VerificationStatus>
                <SendIp>127.0.0.1</SendIp>
                <VerificationTime>Dec 25,2017 03:36:57</VerificationTime>
                <EmailVerificationNo>0000021fd374da99d9c95b48500000</EmailVerificationNo>
                <UserId>0000</UserId>
                <GmtCreate>Dec 25,2017 03:32:40</GmtCreate>
                <GmtModified>Dec 25,2017 03:36:57</GmtModified>
            </EmailVerification>
        </Data>
        <TotalItemNum>2</TotalItemNum>
        <PageSize>500</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>4BF41EC0-C147-4F88-8B3D-D569AF5C3E8B</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1</TotalPageNum>
        <NextPage>false</NextPage>
    </ListEmailVerificationResponse>
    ```

-   JSON format

    ```
    {
      "currentPageNum": 1,
      "data": [
        {
          "confirmIp": "127.0.0.1",
          "email": "test1@aliyun.com",
          "emailVerificationNo": "00000a21fd374da99d9c95b48500000",
          "gmtCreate": "Dec 25,2017 03:38:46",
          "gmtModified": "Dec 25,2017 03:41:11",
          "sendIp": "127.0.0.1",
          "tokenSendTime": "Dec 25,2017 03:38:46",
          "userId": "0000",
          "verificationStatus": 1,
          "verificationTime": "Dec 25,2017 03:41:11"
        },
        {
          "confirmIp": "127.0.0.1",
          "email": "test2@aliyun.com",
          "emailVerificationNo": "0000021fd374da99d9c95b48500000",
          "gmtCreate": "Dec 25,2017 03:32:40",
          "gmtModified": "Dec 25,2017 03:36:57",
          "sendIp": "127.0.0.1",
          "tokenSendTime": "Dec 25,2017 03:35:22",
          "userId": "0000",
          "verificationStatus": 1,
          "verificationTime": "Dec 25,2017 03:36:57"
        }
      ],
      "nextPage": false,
      "pageSize": 500,
      "prePage": false,
      "requestId": "09D3DA75-B3B5-480B-9100-92DC43919B46",
      "totalItemNum": 2,
      "totalPageNum": 1
    }
    ```


