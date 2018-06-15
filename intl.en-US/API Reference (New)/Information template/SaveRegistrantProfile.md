# SaveRegistrantProfile {#concept_dsm_tbc_b2b .concept}

Create or save a domain registrant information template.

## Request parameters {#section_v4h_whc_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action. System required parameter. SaveRegistrantProfile.|
|RegistrantProfileId|Long|Required in template update and empty in template creation.|ID of the domain name information template.|
|Telephone|String|Required in template update and empty in template creation.|Phone number.|
|DefaultRegistrantProfile|Boolean|Required in template update and empty in template creation.|Whether it is the default template.|
|Country|String|Required in template update and empty in template creation.|Country code, such as CN or US.|
|Province|String|Required in template update and empty in template creation.| Province.|
|TelArea|String|Required in template update and empty in template creation.|Country dialing code.|
|City|String|Required in template update and empty in template creation.|City. |
|PostalCode|String|Required in template update and empty in template creation.| Zip code.|
|Email|String|Required in template update and empty in template creation.|Email address.|
|Address|String|Required in template update and empty in template creation.|Specific address。|
|RegistrantName|String|Required in template update and empty in template creation.|Contact name.|
|RegistrantOrganization|String|Required in template update and empty in template creation.| Owner name.|
|TelExt|String|No| Extension number|

## Response parameters { .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|RegistrantProfileId|Long|ID of the contact information template.|

## Error codes { .section}

|Error code|Description|HTTP status code|Meaning|
|:---------|:----------|:---------------|:------|
|ParameterIllegal|Parameter illegal.|400|Parameter error|
|NetworkIOError|Network IO Error.|400|Network I/O exception|

## Examples {#section_tpq_m3c_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=SaveRegistrantProfile
&DefaultRegistrantProfile=false
&Email=a%40a.com
&Address=test+a
&Telephone=18800000000
&PostalCode=000000
&City=testc
&Province=test+p
&RegistrantName=test+rn
&Country=CN
&RegistrantOrganization=test+ro
&TelArea=86
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <SaveRegistrantProfileResponse>
        <RegistrantProfileId>3600000</RegistrantProfileId>
        <RequestId>D09B153B-294D-42F1-BB61-F1C72136DFD3</RequestId>
    </SaveRegistrantProfileResponse>
    ```

-   JSON format

    ```
    {
      "RegistrantProfileId": "3696573",
      "RequestId": "ECB708B9-A82E-45D7-A230-58231E532A57"
    }
    ```


