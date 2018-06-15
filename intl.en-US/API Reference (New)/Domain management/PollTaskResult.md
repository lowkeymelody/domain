# PollTaskResult {#concept_gyj_pyk_c2b .concept}

The PollTaskResult API obtains a task details list of the completed tasks of a domain name \(including successful tasks and failed tasks that reach the retry limit\).  This API must be used with [AcknowledgeTaskResult](intl.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md#) to confirm task results.  After task results are confirmed, the corresponding task records cannot be queried by using this API.

## Request parameters {#section_zw1_rpl_c2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|PageNum|Integer|Yes|1|Page number.|
|PageSize|Integer|Yes|20|Page size.|
|DomainName|String|No|test.com|Domain name.|
|InstanceId |String|No|S20181T0WLI85212| Instance ID.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|TaskNo|String|No|75addb07-28a3-450e-b5ec-test|Task number.|
|TaskResultStatus|Integer|No|2|The task result type, with the following enumerated values: 2: Success. 3: Failed.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_ovn_cql_c2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|E879DC07-38EE-4408-9F33-73B30CD965CD|Unique request ID.|
|TotalItemNum|Integer|10|Total number of entries.|
|CurrentPageNum|Integer|1| Current page number.|
|TotalPageNum|Integer|10|Total number of pages.|
|PageSize|Integer|1|Page size.|
|PrePage|Boolean|false|Whether the previous page exists.|
|NextPage|Boolean|false| Whether the next page exists.|
|Data|[TaskDetail](#table_v4j_inf_b2b)|[TaskDetail](#table_v4j_inf_b2b)|Task details list.|

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|TaskNo|String|b95bc334-f7d8-4f39-8a62-4c4302a243d8|Task number.|
|TaskDetailNo|String|15fee9d10d514bada66bd08c5723c583|Task details number.|
|TaskType|String|CHG\_DNS|Task type.|
|InstanceId|String|S201817141000000|Domain name instance ID.|
|DomainName|String|test.com|Domain name.|
|TaskStatus|String|EXECUTE\_SUCCESS|Task status. Possible values:-   WAITING\_EXECUTE: Awaiting execution
-   EXECUTING: Execution in progress
-   EXECUTE\_SUCCESS: Execution successful
-   EXECUTE\_FAILURE: Execution failed

|
|UpdateTime|String|2018-03-26 15:22:18|Execution time of the last task details operation.|
|CreateTime|String|2018-03-26 15:08:20|Task creation time.|
|TryCount|Integer|0|Number of task details operation retries.|
|ErrorMsg|String|The operation is successful.|Task execution error message.|
|Taskstatuscode|Integer|2| Task status code. Possible values: Possible values:

 -   0 : Awaiting execution
-   1: Execution in progress
-   2: Execution successful
-   3: Execution failed

 |
|TaskResult|String|test|Task result.|
|TaskTypeDescription|String|Modify DNS|Task type description. Change the Lang parameter to change the language used in this field.|

## Examples {#section_of5_377_b2b .section}

**Request parameters**

```
/? Action=PollTaskResult
&PageNum=1
&PageSize=20
&DomainName=test.com
&InstanceId=S20181T0WLI85212
&TaskNo=75addb07-28a3-450e-b5ec-test
&TaskResultStatus=2
&TaskType=1
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <PollTaskResultResponse>
      <Data>
        <TaskDetail>
          <TryCount>0</TryCount>
          <TaskDetailNo>15fee9d10d514bada66bd08c5723c583</TaskDetailNo>
          <TaskNo>b95bc334-f7d8-4f39-8a62-4c4302a243d8</TaskNo>
          <CreateTime>2018-03-26 15:08:20</CreateTime>
          <InstanceId>S201817141000000</InstanceId>
          <UpdateTime>2018-03-26 15:22:18</UpdateTime>
          <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
          <DomainName>test.com</DomainName>
          <TaskTypeDescription>DNS Modification</TaskTypeDescription>
          <TaskStatusCode>2</TaskStatusCode>
          <ErrorMsg>The operation is successful.</ErrorMsg>
          <TaskType>CHG_DNS</TaskType>
        </TaskDetail>
      </Data>
      <TotalItemNum>10</TotalItemNum>
      <PageSize>1</PageSize>
      <CurrentPageNum>1</CurrentPageNum>
      <RequestId>C2CB6161-7971-4EB6-BC16-92A2BA3816D9</RequestId>
      <TotalPageNum>10</TotalPageNum>
    </PollTaskResultResponse>
    ```

-   JSON format

    ```
    {
        "CurrentPageNum":1,
        "Data":{
            "TaskDetail":[{
                "CreateTime":"2018-03-26 15:08:20",
                "DomainName":"test.com",
                "ErrorMsg":"The operation is successful.",
                "InstanceId":"S201817141000000",
                "TaskDetailNo":"15fee9d10d514bada66bd08c5723c583",
                "TaskNo":"b95bc334-f7d8-4f39-8a62-4c4302a243d8",
                "TaskStatus":"EXECUTE_SUCCESS",
                "TaskStatusCode":2,
                "TaskType":"CHG_DNS",
                "TaskTypeDescription":"DNS Modification",
                "TryCount":0,
                "UpdateTime":"2018-03-26 15:22:18"
            }]
        },
        "PageSize":1,
        "RequestId":"E879DC07-38EE-4408-9F33-73B30CD965CD",
        "TotalItemNum":10,
        "TotalPageNum":10
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>3D864CDF-026E-45FE-99C8-B31D0E6A775A</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingPageSize</Code>
      <Message>PageSize is mandatory for this action.</Message>
      <Recommend><![ CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingPageSize&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"MissingPageSize",
        "HostId":"domain.aliyuncs.com",
        "Message":"PageSize is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingPageSize&source=PopGw",
        "RequestId":"85A308D1-F383-4552-B9E7-8D312218D434"
    }
    ```


## Error codes {#section_nwb_377_b2b .section}

[See the error codes of the product](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

