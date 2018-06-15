# VerifyContactField {#concept_phf_nrp_b2b .concept}

The VerifyContactField API verifies domain name contact information.

## Request parameters {#section_g1j_n5q_b2b .section}

|Parameter|Type|Required|Sample value|Description|
|:--------|:---|:-------|:-----------|:----------|
|Address|String|No|Rd. xitucheng|Address.|
|City|String|No|Bei jing|City.|
|Country|String|No|CN|Country code, such as CN or US.|
|Email|String|No|test@test.com|Email.|
|Lang|String|No|en|Language of the information returned by the API, which has the following enumerated values: zh \(Chinese\) and en \(English\). The default value is en.|
|PostalCode|String|No|10000|Postal code.|
|Province|String|No|Bei jing|Province.|
|RegistrantName|String|No|zhang san|Contact name.|
|RegistrantOrganization|String|No|zhang san|Registrant’s name.|
|RegistrantType|String|No|1|Registrant type, with the following enumerated values: 1 : Individual. 2: Enterprise.|
|TelArea|String|No|86|Country dialing code.|
|TelExt|String|No|01|Extension number.|
|Telephone|string|No|13800000000|Phone number.|
|UserClientIp|String|No|127.0.0.1|User IP address.|
|ZhAddress|String|No|西土城路|Chinese address.|
|Zhcity|string|No|Beijing|Chinese city.|
|ZhProvince|String|No|北京|Chinese province.|
|ZhRegistrantName|String|No|张三|Chinese contact name.|
|ZhRegistrantOrganization|String|No|张三|Chinese registrant’s name.|

## Response parameters {#section_u3g_bvq_b2b .section}

|Parameter|Type|Sample value|Description|
|:--------|:---|:-----------|:----------|
|RequestId|String|ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6|The unique request ID.|

## Examples {#section_uc2_21r_b2b .section}

**Request example**

```
/? Action=VerifyContactField
&Address=Rd. xitucheng
&City=Bei jing
&Country=CN
&Email=test@test.com
&PostalCode=10000
&Province=Bei jing
&RegistrantName=zhang san
&RegistrantOrganization=zhang san
&RegistrantType=1
&TelArea=86
&Telephone=13800000000
&TelExt=01
&<Public request parameter>
```

**Normal response example**

-   XML format

    ```
    <VerifyContactFieldResponse>
      <RequestId>30EEA1A7-3C86-471B-BFD8-5AF13CBE0CD3</RequestId>
    </VerifyContactFieldResponse>
    ```

-   JSON format

```
{
    "RequestId":"ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6"
}
```


**Abnormal response example**

-   XML format

    ```
    <Error>
      <RequestId>EA6A415C-01CE-480E-82D1-BE90AF0DC8A8</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>ParameterIllegall</Code>
      <Message>Incorrect format. Make sure that the city is correct</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "Code":"ParameterIllegall",
        "HostId":"domain.aliyuncs.com",
        "Message":"Format error, make sure the city is correct",
        "RequestId":"FCC08834-C2D3-4F2E-BE58-45E96A64298C"
    }
    ```


