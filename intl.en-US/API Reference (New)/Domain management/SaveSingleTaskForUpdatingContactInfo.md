# SaveSingleTaskForUpdatingContactInfo {#concept_enl_j5r_b2b .concept}

The SaveSingleTaskForUpdatingContactInfo API submits a task of modifying the domain name information. You can use the QueryTaskDetailList API to query the task execution result.

## Request parameters {#section_fd3_gvr_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to SaveSingleTaskForUpdatingContactInfo.|
|InstanceId|String|Optional|Domain name instance ID.|
|DomainName|String|Yes|Domain name.|
|RegistrantProfileId|Long|Yes|Information template ID.|
|ContactType|String|Yes|Contact type. The enumerated values include registrant, admin, billing, tech.|
|AddTransferLock|Boolean|Optional|Whether to add transfer prohibition. This parameter takes effect only when ContactType is set to registrant, and indicates whether the domain name can be transferred 60 days after the owner modifies the domain name. The value of the parameter defaults to false, that is, transfer is allowed.|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\). The default value is en.|

## Response parameters {#section_kx5_nvr_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_hdm_rvr_b2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|DomainNotExist|The domain name does not exist.|400|The domain name does not exist.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400| An action is being processed for the domain name. Try again later.|

## Examples {#section_evc_wvr_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForUpdatingContactInfo
&RegistrantProfileId=1
&DomainName=test.com
&ContactType=registrant
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveSingleTaskForUpdatingContactInfoResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveSingleTaskForUpdatingContactInfoResponse>
    ```

-   JSON format

    ```
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


