# QueryTaskDetailHistory {#concept_gfr_tyk_c2b .concept}

The QueryTaskDetailHistory API queries the task details list for the specified domain name and returns the results by page.

## Request parameters {#section_frj_dmm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The API name, a required parameter. Set this parameter to QueryTaskDetailHistory.|
|PageSize|Integer|Yes|Page size.|
|TaskNo|String|Yes|Task ID.|
|TaskStatus|Integer|Optional|Task status, which has the following enumerated values: 0: The task is waiting to be executed. 1 : The task is being executed. 2: The task was successfully executed. 3: The task failed to be executed.|
|DomainName|String|Optional|Domain name.|
|InstanceId|String|Optional|Domain name instance ID.|
|Domainnamecursor|String|Optional|Domain name cursor .|
|TaskDetailNoCursor|String|Optional|Task details cursor.|

## Response parameters {#section_qkp_3mm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|PageSize|Integer|Page size.|
|CurrentPageCursor|[TaskDetailHistoryCurrentPageCursorType](#table_h14_nmm_c2b)|Current page cursor.|
|NextPageCursor|[TaskDetailHistoryNextPageCursorType](#table_x2j_vmm_c2b)|Next page cursor.|
|PrePageCursor|[TaskDetailHistoryPrePageCursorType](#table_e25_2nm_c2b)|Previous page cursor.|
|Objects|[TaskDetailHistoryType](#table_qrs_pnm_c2b)|Task details.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type， which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT : Modify the administrator information.
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
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE : The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   EXECUTE\_SUCCESS: The task has been successfully executed.
-   EXECUTE\_FAILURE: The task failed to be executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   0: awaiting execution.
-   1: execution in progress.
-   2: execution successful.
-   3: execution failed.

|
|String|CreateTime|Task creation time.|
|String|UpdateTime|Last execution time to obtain task details.|
|Integer|TryCount|Number of retries to obtain task details.|
|String|TaskNo|Task ID.|
|String|TaskDetailNo|Task details ID.|
|String|ErrorMsg|Task execution failure message.|
|String|TaskTypeDescription|Description of the task type.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type， which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT : Modify the administrator information.
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
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE : The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   EXECUTE\_SUCCESS: The task has been successfully executed.
-   EXECUTE\_FAILURE: The task failed to be executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   0: awaiting execution.
-   1: execution in progress.
-   2: execution successful.
-   3: execution failed.

|
|String|CreateTime|Task creation time.|
|String|UpdateTime|Last execution time to obtain task details.|
|Integer|TryCount|Number of retries to obtain task details.|
|String|TaskNo|Task ID.|
|String|TaskDetailNo|Task details ID.|
|String|ErrorMsg|Task execution failure message.|
|String|TaskTypeDescription|Description of the task type.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type， which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT : Modify the administrator information.
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
|String|TaskStatus|The task status code, which has the following values:-   WAITING\_EXECUTE : The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   EXECUTE\_SUCCESS: The task has been successfully executed.
-   EXECUTE\_FAILURE: The task failed to be executed.

|
|String|TaskStatusCode|The task status code, which has the following values:-   0: awaiting execution.
-   1: execution in progress.
-   2: execution successful.
-   3: execution failed.

|
|String|CreateTime|Task creation time.|
|String|UpdateTime|Last execution time to obtain task details.|
|Integer|TryCount|Number of retries to obtain task details.|
|String|TaskNo|Task ID.|
|String|TaskDetailNo|Task details ID.|
|String|ErrorMsg|Task execution failure message.|
|String|TaskTypeDescription|Description of the task type.|

|Type|Parameter|Description|
|:---|:--------|:----------|
|String|TaskType|Task type， which has the following enumerated values:-   CHG\_HOLDER: Modify the registrant’s information.
-   CHG\_DNS: Modify DNS information.
-   SET\_WHOIS\_PROTECT: Set privacy protection.
-   UPDATE\_ADMIN\_CONTACT : Modify the administrator information.
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
|String|TaskStatus|Task status, which has the following values:-   WAITING\_EXECUTE : The task is waiting for execution.
-   EXECUTING: The task is being executed.
-   EXECUTE\_SUCCESS: The task has been successfully executed.
-   EXECUTE\_FAILURE: The task failed to be executed.

|
|String|TaskStatusCode|The task status code, which has the following values: which has the following values:-   0: awaiting execution.
-   1: execution in progress.
-   2: execution successful.
-   3: execution failed.

|
|String|CreateTime|Task creation time.|
|String|UpdateTime|Last execution time to obtain task details.|
|Integer|TryCount|Number of retries to obtain task details.|
|String|TaskNo|Task ID.|
|String|TaskDetailNo|Task details ID.|
|String|ErrorMsg|Task execution failure message.|
|String|TaskTypeDescription|Description of the task type.|

## Error codes {#section_jwg_xnm_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_r31_24m_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryTaskDetailHistory
&PageSize=1
&PageNum=1
&TaskNo=75addb07-28a3-450e-b5ec-test
&<Public request parameter>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryTaskDetailHistoryResponse>
        <PageSize>2</PageSize>
        <RequestId>548CAE74-88F8-402F-8C12-97E747389C51</RequestId>
    </QueryTaskDetailHistoryResponse>
    ```

-   JSON format

    ```
    {
      "currentPageCursor": {},
      "nextPageCursor": {},
      "objects": [],
      "pageSize": 2,
      "prePageCursor": {},
      "requestId": "CCE5DABB-48DF-403C-A7A1-A8F8B4F530CA"
    }
    ```


