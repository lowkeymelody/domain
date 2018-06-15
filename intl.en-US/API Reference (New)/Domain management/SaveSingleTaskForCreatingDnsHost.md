# SaveSingleTaskForCreatingDnsHost {#concept_lny_jzk_c2b .concept}

The SaveSingleTaskForCreatingDnsHost API submits a task of creating a DNS host. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_tlq_vtn_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForCreatingDnsHost.|
|InstanceId|String|Yes|Instance ID. You can query it by calling [QueryDomainList](intl.en-US/API Reference (New)/Domain management/QueryDomainList.md#).|
|DnsName|String|Yes|For example: dns1 ".|
|Ips|[IpListType](#table_nfd_d5n_c2b)|Yes|IP address list.|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|ip|String|IP address.|

## Response parameters {#section_wbh_f5n_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_kdd_k5n_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|An action is being processed for the domain name. Try again later.|

## Examples {#section_ff5_n5n_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveSingleTaskForCreatingDnsHost
&DnsName=ns3
&Ip. 2=185.27.134.201
&Ip. 1=218.83.159.236
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForCreatingDnsHostResponse>
    <TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
    <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
    </SaveSingleTaskForCreatingDnsHostResponse>
    ```

-   JSON format

    ```
    {
      "requestId": "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
      "taskNo": "e9b8e8b4-7334-4548-9cec-c30b6891f292"
    }
    ```


