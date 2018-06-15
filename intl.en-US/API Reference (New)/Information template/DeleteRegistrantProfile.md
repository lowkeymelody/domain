# DeleteRegistrantProfile {#concept_wcr_vyb_b2b .concept}

The DeleteRegistrantProfile API deletes the specified domain name information templates.

## Request parameters {#section_g5r_1zb_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to DeleteRegistrantProfile.|
|RegistrantProfileId|Long|Yes|ID of the domain name information template.|

**Response parameters**

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|Unique request identifier.|

**Error codes**

|Error code|Description| HTTP status code| Semantics|
|:---------|:----------|:----------------|:---------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|
|ContactTemplateNotExist|ContactTemplateNotExist|400|The contact information template does not exist.|

## Examples {#section_l4n_kzb_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=DeleteRegistrantProfile
&RegistrantProfileId=3600000
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <DeleteRegistrantProfileResponse>
        <RequestId>C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8</RequestId>
    </DeleteRegistrantProfileResponse>
    ```

-   JSON format

    ```
    {
      "RequestId": "0B22A572-0A57-4510-B233-4620D5DE33FE"
    }
    ```


