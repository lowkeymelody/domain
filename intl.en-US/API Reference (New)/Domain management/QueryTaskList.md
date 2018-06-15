# QueryTaskList {#concept_ic1_wyk_c2b .concept}

The QueryTaskList API queries the list of domain name tasks under the current account and returns the results by page.

## Request parameters {#section_w3j_zsm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The API name, a required parameter. Set this parameter to QueryTaskList.|
|PageNum|Integer|Yes|Page number.|
|PageSize|Integer|Yes|Page size.|
|BeginCreateTime|Long|No|Start time of the period in which the domain name tasks are queried, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|EndCreateTime|Long|No|End time of the period in which the domain name tasks are queried, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|

## Response parameters {#section_npt_ctm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TotalItemNum|Integer|Total number of tasks.|
|CurrentPageNum|Integer|Current page number.|
|Totalpagenum|Integer|Total number of pages.|
|PageSize|Integer|Page size.|
|PrePage|Boolean|Whether the previous page exists.|
|NextPage|Boolean|Whether the next page exists.|
|Data|[Taskinfotype](#table_dhm_gtm_c2b)|Task list.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type, which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT: Modify the administrator information.
-   UPDATE\_BILLING\_CONTACT: Modify the payers information.
-   UPDATE\_TECH\_CONTACT: Modify the technician information.
-   SET\_UPDATE\_PROHIBITED: Set the domain name security lock.
-   SET\_TRANSFER\_PROHIBITED : Set the domain name transfer lock.
-   ORDER\_ACTIVATE: Create a registration order.
-   ORDER\_RENEW: Create a renewal order.
-   ORDER\_REDEEM: Create a redemption order.
-   CREATE\_DNSHOST: Create a DNS host.
-   UPDATE\_DNSHOST: Update a DNS host.
-   SYNC\_DNSHOST: Synchronize a DNS host.

|
|Integer|TaskNum|Number of domain names in the task.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   COMPLETE: The has been executed.

|
|String|TaskStatusCode|Task status code. which has the following values:-   1: The task is waiting for execution.
-   2: The task is being executed.
-   3: The has been executed.

|
|String|CreateTime|Task creation time.|
|String|Clientip|IP address of the user who submits the task.|
|String|TaskNo|Task ID.|
|String|TaskTypeDescription|Description of the task type.|

## Error codes {#section_izl_ptm_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_lsg_stm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryTaskList
&PageNum=1
&PageSize=2
&<Public request parameter>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryTaskListResponse>
        <Data>
            <TaskInfo>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>8b1cd755-4928-4b02-adee-e5d41d7b1939</TaskNo>
                <CreateTime>Dec 26,2017 11:00:54</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>1</TaskNum>
                <TaskType>CREATE_DNSHOST</TaskType>
            </TaskInfo>
            <TaskInfo>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>b0069db5-db21-4e57-842a-260c370a37e2</TaskNo>
                <CreateTime>Dec 26,2017 11:00:54</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>2</TaskNum>
                <TaskType>CHG_DNS</TaskType>
            </TaskInfo>
        </Data>
        <TotalItemNum>43</TotalItemNum>
        <PageSize>2</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>8D7D294A-8E99-481F-B64C-017EFC793059</RequestId>
        <TotalPageNum>22</TotalPageNum>
    </QueryTaskListResponse>
    ```

-   JSON format

    ```
    {
      "CurrentPageNum": 1,
      "Data": {
        "TaskInfo": [
          {
            "Clientip": "127.0.0.1",
            "CreateTime": "Dec 26,2017 11:00:54",
            "TaskNo": "8b1cd755-4928-4b02-adee-e5d41d7b1939",
            "TaskNum": 1,
            "TaskStatus": "COMPLETE",
            "TaskType": "CREATE_DNSHOST"
          },
          {
            "Clientip": "127.0.0.1",
            "CreateTime": "Dec 26,2017 11:00:54",
            "TaskNo": "b0069db5-db21-4e57-842a-260c370a37e2",
            "TaskNum": 2,
            "TaskStatus": "COMPLETE",
            "TaskType": "CHG_DNS"
          }
        ]
      },
      "PageSize": 2,
      "RequestId": "85C735DC-872F-423B-A728-C20C2924D3C6",
      "TotalItemNum": 43,
      "TotalPageNum": 22
    }
    ```


