# QueryContactInfo {#concept_akb_ryk_c2b .concept}

The QueryContactInfo API queries the domain name contact information.

## Request parameters {#section_hcg_rtl_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryContactInfo.|
|DomainName|String|Yes|Domain name.|
|ContactType|String|Yes|Contact type. The optional values include: registrant owner of the domain name\), tech \(technician\), admin \(administrator\), and billing \(payer\).|

## Response parameters {#section_gk5_5tl_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|CreateDate|String|Creation time.|
|RegistrantName|String|Contact name.|
|RegistrantOrganization|String|Owner name.|
|Province|String|Province|
|City|String|City|
|Address|String|Specific address.|
|Country|String|Country code, such as CN or US.|
|Email|String|Mailbox.|
|PostalCode|String|Zip code.|
|TelArea|String|Country dialing code.|
|Telephone|String|Phone number.|
|TelExt|String|Extension number.|

## Error codes {#section_rxh_ddm_c2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_hb5_gdm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryContactInfo
&DomainName=fds234sdf.net&ContactType=admin
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryContactInfoResponse>
        <CreateDate>2013-12-06 00:00:00</CreateDate>
        <Address>Ou Wo E Ou </Address>
        <TelExt></TelExt>
        <City>Bei Jing Shi</City>
        <Telephone>13000000000</Telephone>
        <Country>CN</Country>
        <TelArea>86</TelArea>
        <Province>Bei Jing</Province>
        <PostalCode>111111</PostalCode>
        <Email>13000000000@aliyun.com</Email>
        <RequestId>DBBEFD6C-86F2-4C68-930A-21F8668BB6E8</RequestId>
        <RegistrantName>li Yun</RegistrantName>
        <RegistrantOrganization>Li Yun</RegistrantOrganization>
    </QueryContactInfoResponse>
    ```

-   JSON format

    ```
    {
      "CreateDate": "2013-12-06 00:00:00",
      "Address": "Ou Wo E Ou ",
      "TelExt": "",
      "City": "Bei Jing Shi",
      "Telephone": "1300000000",
      "Country": "CN",
      "TelArea": "86",
      "Province": "Bei Jing",
      "PostalCode": "111111",
      "Email": "1300000000@aliyun.com",
      "RequestId": "77B19432-82FF-4D25-82F9-CF83E19516F7",
      "RegistrantName": "li Yun",
      "RegistrantOrganization": "Li Yun"
    }
    ```


