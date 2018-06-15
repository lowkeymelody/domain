# SaveBatchTaskForModifyingDomainDns {#concept_cwr_dzk_c2b .concept}

The SaveBatchTaskForModifyingDomainDns API submits bulk DNS modification tasks. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_dq5_t3n_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveBatchTaskForModifyingDomainDns.|
|DomainName|[DomainListType](#table_otg_v3n_c2b)|Yes|Domain name list.|
|AliyunDns|Boolean|Yes|Whether to change the domain name to Alibaba Cloud DNS.|
|DomainNameServer|[DnsListType](#table_x31_y3n_c2b)|No|DNS list \(required if AliyunDns is set to false\).|
|Lang|String|No| Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\).  The default value is en.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|DomainName|String|Domain name.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|DNS|String|DNS information.|

## Response parameters {#section_xhw_fjn_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_nwj_3jn_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_dfv_jjn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/
? Action=SaveBatchTaskForModifyingDomainDns
&AliyunDns=false
&DomainName. 1=test1.com
&DomainName. 2=test2.com
&DomainNameServer. 1=ns1.test.com
&DomainNameServer. 2=ns2.test.com
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForModifyingDomainDnsResponse>
    <TaskNo>35fb2fb7-d4d6-4478-9408-22cb63696b86</TaskNo>
    <RequestId>6A862A8A-E7AB-4C4E-8946-A74122D9CC4B</RequestId></SaveBatchTaskForModifyingDomainDnsResponse>
    ```

-   JSON format

    ```
    {
      "requestId": "689C17B3-6AE0-45FB-8E41-4491A02C9999",
      "taskNo": "fce12087-6c9f-4dcd-92df-d3829b7f19bc"
    }
    ```


