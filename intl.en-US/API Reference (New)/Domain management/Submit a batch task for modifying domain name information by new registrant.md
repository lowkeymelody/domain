# Submit a batch task for modifying domain name information by new registrant {#concept_dwb_gzk_c2b .concept}

The SaveBatchTaskForUpdatingContactInfoByNewContact API submits a batch task for modifying domain name information by new registrant. You can use the [QueryTaskDetailList](reseller.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md#) API to query the task execution result.

## Request parameters {#section_zwz_yln_c2b .section}

For more information about public request parameters, see [Public parameters](reseller.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Name|Parameters|Required|Description|
|:---|:---------|:-------|:----------|
|Action|String|Yes|The name of API. Set this parameter to SaveBatchTaskForUpdatingContactInfoByNewContact.|
|DomainName|[DomainListType](#table_fvy_dmn_c2b)|Yes|Domain name list.|
|ContactType|String|Yes|Contact type. Optional values: -   registrant
-   admin
-   billing
-   tech

|
|TransferOutProhibited|Boolean|Optional|Whether to add a transfer out prohibition. This parameter takes effect only when ContactType is set to registrant, and indicates whether the domain name can be transferred 60 days after the registrant modifies the domain name. The default value is false, that is, transfer is allowed.|
|Lang|String|No|Language of the error message returned by the API. Optional values: zh \(Chinese\),en \(English\). The default value is en.|
|RegistrantName|String|Yes|Contact name.|
|RegistrantOrganization|String|Yes|Registrant’s organization.|
|Province|String|Yes|Province.|
|City|String|Yes|City. |
|Address|String|Yes|The specific address.|
|Country|String|Yes|Country code, such as CN or US.|
|Email|String|Yes|Email address.|
|PostalCode|String|Yes|Postal code.|
|TelArea|String|Yes|Country dialing code.|
|Telephone|String|Yes|Phone number.|
|TelExt|String|Yes|Extension number.|

|Name|Type|Description|
|:---|:---|:----------|
|DomainName|String|Domain Name.|

## Response parameters {#section_gyt_mmn_c2b .section}

|Name |Type|Required|
|:----|:---|:-------|
|RequestId|String|Unique request identifier.|
|TaskNo|String|Task ID.|

## Error codes {#section_jxz_4mn_c2b .section}

|Error code|Description| HTTP status code| Description|
|:---------|:----------|:----------------|:-----------|
|ParameterIllegal|Parameter illegal.|400|You used an illegal parameter.|
|NetworkIOError|Network I/O Error.|400|A network I/O exception occurs.|
|DomainNotExist|The domain name does not exist.|400|The domain name does not exist.|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|There is an ongoing operation for the domain name. Try again later.|

## Examples {#section_hvy_rmn_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveBatchTaskForUpdatingContactInfoByNewContact
&Address=Rd. xitucheng
&City=Bei jing
&Country=CN
&Email=test@test.com
&PostalCode=10000
&Province=Bei jing
&RegistrantName=zhang san
&RegistrantOrganization=zhang san
&RegistrantType=2
&TelArea=86
&Telephone=13800000000
&TelExt=01
&DomainName. 1=alibabacloud.com
&DomainName. 2=aliyun.com
&ContactType=registrant
&AddTransferLock=true
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveBatchTaskForUpdatingContactInfoByNewContactResponse>
        <TaskNo>880f1579-be51-4dd3-a69d-test</TaskNo>
        <RequestId>EDC28FEC-6BE0-4583-95BC-test</RequestId>
    </SaveBatchTaskForUpdatingContactInfoByNewContactResponse>
    ```

-   JSON format

    ```
    {
      "requestId": "464AF466-CA8E-43A8-B61D-test",
      "taskNo": "65de2165-ca09-491f-9fe0-test"
    }
    ```


