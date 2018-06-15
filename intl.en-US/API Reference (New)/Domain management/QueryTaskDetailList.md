# QueryTaskDetailList {#concept_ozl_5yk_c2b .concept}

The QueryTaskDetailList API queries the details list of the specified domain name task and returns the results by page.

## Request parameters {#section_y33_p4m_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryTaskDetailList.|
|PageNum|Integer|Yes|Page number.|
|PageSize|Integer|Yes|Page size.|
|TaskNo|String|Yes|Task ID.|
|TaskStatus|Integer|Optional|Task status. The enumerated values include: 0: The task is waiting to be executed. 1 : The task is being executed. 2: The task is successfully executed. 3: The task fails to be executed.|
|DomainName|String|Optional|Domain name.|
|InstanceId|String|Optional|Domain name instance ID.|

## Response parameters {#section_j34_jpm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier|
|TotalItemNum|Integer|Total number of details items|
|CurrentPageNum|Integer|Current page number.|
|TotalPageNum|Integer|Total number of pages.|
|PageSize|Integer|Page size.|
|PrePage|Boolean|Whether the previous page exists.|
|NextPage|Boolean|Whether the next page exists.|
|Data|[TaskDetailType](#table_jrf_qpm_c2b)|Task list.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type, which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT: Modify the administrator information.
-   UPDATE\_BILLING\_CONTACT: Modify the payers information.
-   UPDATE\_TECH\_CONTACT: Modify the technician information.
-   SET\_UPDATE\_PROHIBITED: Set the domain name security lock.
-   SET\_TRANSFER\_PROHIBITED: Set the domain name transfer lock.
-   ORDER\_ACTIVATE: Create a registration order.
-   ORDER\_RENEW: Create a renewal order.
-   ORDER\_REDEEM: Create a redemption order.
-   CREATE\_DNSHOST: Create a DNS host.
-   UPDATE\_DNSHOST: Update a DNS host.
-   SYNC\_DNSHOST: Synchronize DNS host information.

|
|String|DomainName|Domain name.|
|String|InstanceId|Domain name instance ID.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   EXECUTE\_SUCCESS: The task has been successfully executed.
-   EXECUTE\_FAILURE: The task failed to be executed.

|
|String|TaskStatusCode|Task status code. which has the following values:-   0: The task is waiting for execution.
-   1: The task is being executed.
-   2: The task has been successfully executed.
-   3: The task failed to be executed.

|
|String|CreateTime|Task creation time.|
|String|UpdateTime|Last execution time to obtain task details.|
|Integer|TryCount|Number of retries to obtain task details.|
|String|TaskNo|Task ID.|
|String|TaskDetailNo|Task details ID.|
|String|ErrorMsg|Task execution failure message.|
|String|TaskTypeDescription|Description of the task type.|
|String|TaskResult|Task execution results.|

## Error codes {#section_wcy_5pm_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_s2x_wpm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryTaskDetailList
&PageSize=1
&PageNum=1
&TaskNo=75addb07-28a3-450e-b5ec-9f98b9d07ea3
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryTaskDetailListResponse>
        <Data>
            <TaskDetail>
                <TryCount>0</TryCount>
                <TaskDetailNo>75addb07-28a3-450e-b5ec-test</TaskDetailNo>
                <TaskNo>60d6e201-8ee5-47ab-8fdc-test</TaskNo>
                <CreateTime>2018-01-25 20:46:57</CreateTime>
                <InstanceId>S20179H1BBI9test</InstanceId>
                <UpdateTime>2018-01-25 20:47:01</UpdateTime>
                <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
                <DomainName>test.com</DomainName>
                <TaskStatusCode>2</TaskStatusCode>
                <ErrorMsg>The operation is successful.</ErrorMsg>
                <TaskType>ORDER_RENEW</TaskType>
            </TaskDetail>
        </Data>
        <TotalItemNum>1</TotalItemNum>
        <PageSize>2</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>6A2320E4-D870-49C9-A6DC-test</RequestId>
        <TotalPageNum>1</TotalPageNum>
    </QueryTaskDetailListResponse>
    ```

-   JSON format

    ```
    {
      "currentPageNum": 1,
      "data": [
        {
          "createTime": "2018-01-25 20:46:57",
          "domainName": "test.com",
          "errorMsg": "The operation is successful.",
          "instanceId": "S20179H1BBI9test",
          "taskDetailNo": "d2402d834c9e4db880d375173e786738",
          "taskNo": "75addb07-28a3-450e-b5ec-test",
          "taskStatus": "EXECUTE_SUCCESS",
          "taskStatusCode": 2,
          "taskType": "ORDER_RENEW",
          "tryCount": 0,
          "updateTime": "2018-01-25 20:47:01"
        }
      ],
      "pageSize": 2,
      "requestId": "A0D9EC32-E365-414F-A9B4-test",
      "totalItemNum": 1,
      "totalPageNum": 1
    }
    ```


