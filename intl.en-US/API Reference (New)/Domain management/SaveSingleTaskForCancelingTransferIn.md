# SaveSingleTaskForCancelingTransferIn {#concept_ehk_3zk_c2b .concept}

The SaveSingleTaskForCancelingTransferIn API submits tasks to cancel domain name transfer to Alibaba Cloud Domains. You can use the [QueryTaskDetailList](intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_wnj_zqn_c2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|DomainName|String|Yes|test.com|Domain name.|
|Lang|String|No|en|Language of the error message returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|UserClientIp|String|No|127.0.0.1|User IP address.|

## Response parameters {#section_fdl_drn_c2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The unique request ID.|
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|The task ID.|

## Examples {#section_of5_404_b2b .section}

**Request example**

```
/? Action=SaveSingleTaskForCancelingTransferIn
&DomainName=test.com
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <SaveSingleTaskForCancelingTransferInResponse>
      <TaskNo>3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054</TaskNo>
      <RequestId>EEB28AA7-6051-4E71-B2CC-DAAFB2DF6BCA</RequestId>
    </SaveSingleTaskForCancelingTransferInResponse>e>
    ```

-   JSON format

    ```
    {
        "RequestId":"492D1868-1384-4219-8F8B-7EB44534A72A",
        "TaskNo":"939b6918-be3b-4c4f-b949-93553da52dca"
    }
    ```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>4149E915-CD99-4C77-9D6D-58A3E58E8135</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>TaskIsBeingProcessed</Code>
      <Message>An operation is being processed. Please try again later.</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"TaskIsBeingProcessed",
        "HostId":"domain.aliyuncs.com",
        "Message":"An operation is being processed. Please try again later.",
        "RequestId":"CF7F1EC6-9BE0-4B96-968A-4982EE813647"
    }
    ```


