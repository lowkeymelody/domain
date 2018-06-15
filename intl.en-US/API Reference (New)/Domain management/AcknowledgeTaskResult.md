# AcknowledgeTaskResult {#concept_bl2_2qy_b2b .concept}

TheAcknowledgeTaskResult API confirms detailed task results. After the task result is confirmed, you cannot query that task by calling [PollTaskResult](intl.en-US/API Reference (New)/Domain management/PollTaskResult.md#).

## Request parameters {#section_shn_szk_c2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|TaskDetailNo.N|RepeatList|Yes|2659c29493e94416b297a7691340ccc4|Task details number.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_hqz_11l_c2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|D6CB3623-4726-4947-AC2B-2C6E673B447C|The unique request ID.|
|Result|Integer|1|Number of items successfully confirmed.|

## Examples {#section_of5_371_b2b .section}

**Request example**

```
/? Action=AcknowledgeTaskResult
&TaskDetailNo. 1=2659c29493e94416b297a7691340ccc4
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <AcknowledgeTaskResultResponse>
      <Result>2</Result>
      <RequestId>25DE4410-3E4D-493E-A5E2-927DB738CCEB</RequestId>
    </AcknowledgeTaskResultResponse>
    ```

-   JSON format

    ```
    {
        "RequestId":"270F04F2-6086-4B54-A86B-A1956F231CEC",
        "Result":2
    }
    ```


**Exception response example**

-   XML format

    ```
    <Error>
      <RequestId>3A598F91-51B9-4027-B516-BB2BE3E3352D</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingTaskDetailNo</Code>
      <Message>TaskDetailNo is mandatory for this action.</Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingTaskDetailNo&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"MissingTaskDetailNo",
        "HostId":"domain.aliyuncs.com",
        "Message": "taskdetailno is mandatory for this action .",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingTaskDetailNo&source=PopGw",
        "RequestId":"37FCCA3D-5BD7-436D-A1EC-3F2E08F0E71E"
    }
    ```


## Error code {#section_nwb_371_b2b .section}

[See error codes of this product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

