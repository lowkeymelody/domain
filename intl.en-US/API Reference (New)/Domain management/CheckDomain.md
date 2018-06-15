# CheckDomain {#concept_nds_myk_c2b .concept}

The CheckDomain API checks whether the domain name can be registered according to the input parameters. To determine the domain name validity, see [Domain name validity](intl.en-US/API Reference (New)/Appendix/Domain name validity.md#).

## Request parameters {#section_nmf_ybl_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to CheckDomain.|
|DomainName|String|Yes|Domain name.|

## Response parameters { .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|DomainName|String|Domain name to be queried.|
|Avail|Integer|Whether the domain name can be registered. The optional values are as follows: 1: Yes. 2: Pending. 0: No. -1 : Abnormal. -2: No. -3: Blacklist.|
|Premium|Boolean|Whether it is a premium domain name. The optional values are as follows:true \(yes\) andfalse \(no\).|

## Error codes {#section_ap3_ycl_c2b .section}

For general errors to all APIs, see the [Error code table](intl.en-US/API Reference (New)/Appendix/Error code table.md#).

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|Failed|Query failed.|400|The query failed.|
|QueryRegistryFailed|Query registry failed.|400|Failed to query the registry.|
|Busy|Server is busy, please try again later.|400|The system is busy.|
|InvaildParameter|The parameter is invaild.|400| The parameter is invalid.|

## Examples {#section_gpk_cdl_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=CheckDomain
&DomainName=abc.com
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <CheckDomain>
        <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
        <DomainName>abc.com</DomainName>
        <Avail>0</Avail>
        <Premium>false</Premium>
    </CheckDomain>
    ```

-   JSON format Examples

    ```
    {
        "RequestId": "BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1",
        "DomainName": "abc.com",
        "Avail": 0,
        "Premium": false
    }
    ```


