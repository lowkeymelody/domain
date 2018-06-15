# QueryTaskInfoHistory {#concept_s5f_vyk_c2b .concept}

The QueryTaskInfoHistory API queries the list of historical domain name tasks under the current account and returns the results by page.

## Request parameters {#section_gdr_yqm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The API name, a system required parameter. Set this parameter to QueryTaskInfoHistory.|
|PageSize|Integer|Yes|Page size.|
|BeginCreateTime|Long|No|Start time of the period in which the domain name tasks are queried by creation date, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|EndCreateTime|Long|No|End time of the period in which the domain name tasks are queried by creation date, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|CreateTimeCursor|String|No|Creation date cursor.|
|TaskNoCursor|String|No|Task cursor. When you turn pages, this is task number in the corresponding page cursor.|

## Response parameters {#section_wb5_crm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|PageSize|Integer|Page size.|
|CurrentPageCursor|[TaskInfoHistoryCurrentPageCursorType](#table_v3m_prm_c2b)|Current page cursor.|
|NextPageCursor|[TaskInfoHistoryNextPageCursorType](#table_a1s_srm_c2b)|Next page cursor.|
|PrePageCursor|[TaskInfoHistoryPrePageCursorType](#table_t4m_xrm_c2b)|Previous page cursor.|
|Objects|[TaskInfoHistoryType](#table_nzd_bsm_c2b)|Task information.|

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
-   UPDATE\_REGISTRANT\_CONTACT: Modify the registration contact.
-   DELETE\_DOMAIN: Delete domain name.
-   SYNC\_DNSHOST: Synchronize DNS host information.

|
|Integer|TaskNum|Number of domain names in the task.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   COMPLETE: The has been executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   1: awaiting execution.
-   2: execution in progress.
-   3: execution complete.

|
|String|CreateTime|Task creation time.|
|String|CreateTimeLong|Task creation time.|
|String|Clientip|IP address of the user who submits the task.|
|String|TaskNo|Task ID.|
|String|TaskTypeDescription|Description of the task type.|

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
-   UPDATE\_REGISTRANT\_CONTACT: Modify the registration contact.
-   DELETE\_DOMAIN: Delete domain name.
-   SYNC\_DNSHOST: Synchronize DNS host information.

|
|Integer|TaskNum|Number of domain names in the task.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   COMPLETE: The has been executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   1: awaiting execution.
-   2: execution in progress.
-   3: execution complete.

|
|String|CreateTime|Task creation time.|
|String|CreateTimeLong|Task creation time.|
|String|Clientip|IP address of the user who submits the task.|
|String|TaskNo|Task ID.|
|String|TaskTypeDescription|Description of the task type.|

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
-   UPDATE\_REGISTRANT\_CONTACT: Modify the registration contact.
-   DELETE\_DOMAIN: Delete domain name.
-   SYNC\_DNSHOST: Synchronize DNS host information.

|
|Integer|TaskNum|Number of domain names in the task.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   COMPLETE: The has been executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   1: awaiting execution.
-   2: execution in progress.
-   3: execution complete.

|
|String|CreateTime|Task creation time.|
|String|CreateTimeLong|Task creation time.|
|String|Clientip|IP address of the user who submits the task.|
|String|TaskNo|Task ID.|
|String|TaskTypeDescription|Description of the task type.|

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
-   UPDATE\_REGISTRANT\_CONTACT: Modify the registration contact.
-   DELETE\_DOMAIN: Delete domain name.
-   SYNC\_DNSHOST: Synchronize DNS host information.

|
|Integer|TaskNum|Number of domain names in the task.|
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE: The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   COMPLETE: The has been executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   1: awaiting execution.
-   2: execution in progress.
-   3: execution complete.

|
|String|CreateTime|Task creation time.|
|String|CreateTimeLong|Task creation time.|
|String|Clientip|IP address of the user who submits the task.|
|String|TaskNo|Task ID.|
|String|TaskTypeDescription|Description of the task type.|

## Error codes {#section_ytj_3sm_c2b .section}

|Error code|Description| HTTP status code| Description|
|:---------|:----------|:----------------|:-----------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_vxg_lsm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryTaskInfoHistory
&PageSize=2
&<Public request parameter>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryTaskInfoHistoryResponse>
        <Objects>
            <TaskInfoHistory>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
                <CreateTime>2017-11-01 17:22:51</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>1</TaskNum>
                <TaskStatusCode>3</TaskStatusCode>
                <TaskType>CHG_DNS</TaskType>
                <CreateTimeLong>1509528171000</CreateTimeLong>
            </TaskInfoHistory>
            <TaskInfoHistory>
                <Clientip>127.0.0.1</Clientip>
                <TaskNo>f9baa3d5-33b9-4c81-8847-test</TaskNo>
                <CreateTime>2017-11-01 17:19:47</CreateTime>
                <TaskStatus>COMPLETE</TaskStatus>
                <TaskNum>15</TaskNum>
                <TaskStatusCode>3</TaskStatusCode>
                <TaskType>CHG_DNS</TaskType>
                <CreateTimeLong>1509527987000</CreateTimeLong>
            </TaskInfoHistory>
        </Objects>
        <PageSize>2</PageSize>
        <NextPageCursor>
            <TaskNo>8f112aa1-98be-48c3-82f8-test</TaskNo>
            <CreateTime>2017-10-27 13:07:07</CreateTime>
            <CreateTimeLong>1509080827000</CreateTimeLong>
        </NextPageCursor>
        <RequestId>EB3FCCBA-CA1F-4D31-9F34-test</RequestId>
        <CurrentPageCursor>
            <Clientip>127.0.0.1</Clientip>
            <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
            <CreateTime>2017-11-01 17:22:51</CreateTime>
            <TaskStatus>COMPLETE</TaskStatus>
            <TaskNum>1</TaskNum>
            <TaskStatusCode>3</TaskStatusCode>
            <TaskType>CHG_DNS</TaskType>
            <CreateTimeLong>1509528171000</CreateTimeLong>
        </CurrentPageCursor>
    </QueryTaskInfoHistoryResponse>
    ```

-   JSON format

    ```
    {
      "currentPageCursor": {
        "clientip": "127.0.0.1",
        "createTime": "2017-11-01 17:22:51",
        "createTimeLong": 1509528171000,
        "taskNo": "aa634d3f-927e-4d17-9d2c-test",
        "taskNum": 1,
        "taskStatus": "COMPLETE",
        "taskStatusCode": 3,
        "taskType": "CHG_DNS"
      },
      "nextPageCursor": {
        "createTime": "2017-10-27 13:07:07",
        "createTimeLong": 1509080827000,
        "taskNo": "8f112aa1-98be-48c3-82f8-test"
      },
      "objects": [
        {
          "clientip": "127.0.0.1",
          "createTime": "2017-11-01 17:22:51",
          "createTimeLong": 1509528171000,
          "taskNo": "aa634d3f-927e-4d17-9d2c-test",
          "taskNum": 1,
          "taskStatus": "COMPLETE",
          "taskStatusCode": 3,
          "taskType": "CHG_DNS"
        },
        {
          "clientip": "127.0.0.1",
          "createTime": "2017-11-01 17:19:47",
          "createTimeLong": 1509527987000,
          "taskNo": "f9baa3d5-33b9-4c81-8847-test",
          "taskNum": 15,
          "taskStatus": "COMPLETE",
          "taskStatusCode": 3,
          "taskType": "CHG_DNS"
        }
      ],
      "pageSize": 2,
      "prePageCursor": {},
      "requestId": "6EB5D9B8-AD99-4423-9D02-test"
    }
    ```


