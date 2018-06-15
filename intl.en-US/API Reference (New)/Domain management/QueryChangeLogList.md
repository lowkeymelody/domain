# QueryChangeLogList {#concept_ptg_qyk_c2b .concept}

The QueryChangeLogList API queries operation logs under the current account and returns the results by page.

## Request parameters {#section_b1f_xrl_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryChangeLogList.|
|PageNum|Integer|Yes|Page number. The minimum value is 1.|
|PageSize|Integer|Yes|Page size. The value ranges from 1 to 100.|
|StartDate|Long|No|Start time of the period in which the operation logs are queried, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970.|
|EndDate|Long|No|End time of the period in which the operation logs are queried, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970.|
|DomainName|String|No|Domain name of which the operation logs are queried.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_tlk_1sl_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TotalItemNum|Integer|The total number of records.|
|CurrentPageNum|Integer|The current page number.|
|TotalPageNum|Integer|Total number of pages.|
|PageSize|Integer|The page size.|
|PrePage|Boolean|Whether the previous page exists.|
|NextPage|Boolean|Whether the next page exists.|
|ResultLimit|Boolean|If the number of pages is not limited, the server end can process at most 1,000 records during query. If the number of results exceeds 1,000 and ResultLimit is set to true, you are required to narrow down the time range and query again. Alternatively, set ResultLimit to false.|
|Data|[ChangeLogType](#table_u4w_fsl_c2b)|List of operation logs|

|Parameter|Type|Description|
|:--------|:---|:----------|
|DomainName|String|Domain name.|
|Result|String|Operation result.|
|Operation|String|Operation action.|
|OperationIPAddress|String|Operation IP address.|
|Details|String|Details.|
|Time|String| Operation time, in UTC format. For example, 2017-12-25 12:00:00. The specific format is determined by the input parameter Lang.|

## Error codes {#section_lvw_ksl_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_wll_2tl_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryChangeLogList
&PageNum=1
&PageSize=1
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryChangeLogListResponse>
        <Data>
            <ChangeLog>
                <Result>Failed</Result>
                <Operation>DNS modification</Operation>
                <Time>2017-12-26 12:00:00</Time>
                <Details>dns1;dns2 -> dns3;dns4</Details>
                <DomainName>test1.com</DomainName>
                <OperationIPAddress>127.0.0.1</OperationIPAddress>
            </ChangeLog>
        </Data>
        <TotalItemNum>1000</TotalItemNum>
        <PageSize>1</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>2DEDFF32-7827-46B1-BE90-3DB8ABD91A58</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1000</TotalPageNum>
        <ResultLimit>true</ResultLimit>
        <NextPage>true</NextPage>
    </QueryChangeLogListResponse>
    ```

-   JSON format

    ```
    {
      "currentPageNum": 1,
      "data": [
        {
          "Details": "dns1; dns2-> dns3; dns4 ",
          "domainName": "test1.com",
          "operation": "DNS modification",
          "operationIPAddress": "127.0.0.1",
          "result": "Failed",
          "time": "2017-12-26 12:00:00"
        }
      ],
      "nextPage": true,
      "pageSize": 1,
      "prePage": false,
      "requestId": "0B83F967-7135-49A3-B249-ABC14CBA6B8B",
      "resultLimit": true,
      "totalItemNum": 1000,
      "totalPageNum": 1000
    }
    ```


