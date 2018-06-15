# QueryRegistrantProfiles {#concept_l4w_rzb_b2b .concept}

The QueryRegistrantProfiles API queries domain name information templates under the current account.

## Request parameters {#section_dxl_j1c_b2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action. System required parameter. Set it to QueryRegistrantProfiles.|
|RegistrantOrganization|String|No|Name of the domain name owner.|
|RegistrantProfileId|Long|No|Contact template ID.|
|DefaultRegistrantProfile|Boolean|No|Whether it is the default template.|
|PageNum|Integer|No|Page number.|
|PageSize|Integer|No|Number of records on each page.|

## Response parameters {#section_nxv_w1c_b2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|TotalItemNum|Integer|Total number of records.|
|CurrentPageNum|Integer| Current page number.|
|TotalPageNum|Integer|Total number of pages.|
|PageSize|Integer| Number of records on each page.|
|PrePage|Boolean| Whether the previous page exists.|
|NextPage|Boolean|Whether the next page exists.|
|RegistrantProfile|[Registrantprofiletype](intl.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md#table_s4s_tmq_b2b)|List of domain name information templates. See the following table: RegistrantProfileType.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|RegistrantProfileId|Long|ID of the domain name information template.|
|CreateTime|String|Creation time.|
|UpdateTime|String|Update time.|
|Telephone|String|Phone number.|
|DefaultRegistrantProfile|Boolean|Whether it is the default template.|
|Country|String| Country code, such as CN or US.|
|province|String|Province.|
|TelArea|String|Country dialing code.|
|City|String| City.|
|PostalCode|String| Zip code.|
|Email|String|Email|
|Address|String|Specific address.|
|RegistrantName|String|Contact name.|
|RegistrantOrganization|String| Owner name.|
|TelExt|String|Extension number.|
|EmailVerificationStatus|Integer|Email address verification status. Values: 0:not verified, 1:verified|

**Error codes**

|Error code|Description|HTTP status code|Meaning|
|----------|-----------|----------------|-------|
|ParameterIllegal|Parameter illegal.|400| Parameter error.|
|NetworkIOError|Network IO Error.|400|Network I/O exception|

## Examples {#section_vgl_jbc_b2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryRegistrantProfiles
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryRegistrantProfilesResponse>
        <TotalItemNum>11</TotalItemNum>
        <PageSize>2</PageSize>
        <CurrentPageNum>1</CurrentPageNum>
        <RequestId>1200F9CE-0000-4C5F-86C2-F8CF3828670D</RequestId>
        <PrePage>false</PrePage>
        <RegistrantProfiles>
            <RegistrantProfile>
                <Telephone>11119999</Telephone>
                <DefaultRegistrantProfile>true</DefaultRegistrantProfile>
                <EmailVerificationStatus>0</EmailVerificationStatus>
                <UpdateTime>Dec 25,2017 03:21:59</UpdateTime>
                <Country>US</Country>
                <Province>qa</Province>
                <TelArea>010</TelArea>
                <City>us</City>
                <RegistrantProfileId>5170612</RegistrantProfileId>
                <PostalCode>010101</PostalCode>
                <Email>xxx@xxx.com</Email>
                <CreateTime>Dec 25,2017 03:20:30</CreateTime>
                <Address>aqqqq</Address>
                <RegistrantName>pop</RegistrantName>
                <RegistrantOrganization>popus-x</RegistrantOrganization>
            </RegistrantProfile>
            <RegistrantProfile>
                <Telephone>15600000000</Telephone>
                <DefaultRegistrantProfile>false</DefaultRegistrantProfile>
                <EmailVerificationStatus>0</EmailVerificationStatus>
                <UpdateTime>Nov 22,2017 09:20:40</UpdateTime>
                <Country>MO</Country>
                <Province>Beijing</Province>
                <TelArea>853</TelArea>
                <City>Beijing</City>
                <RegistrantProfileId>5049715</RegistrantProfileId>
                <PostalCode>100086</PostalCode>
                <Email>abctest@xx.com</Email>
                <CreateTime>Nov 22,2017 09:20:40</CreateTime>
                <Address>Chaoyang District</Address>
                <RegistrantName>lk</RegistrantName>
                <RegistrantOrganization>lk</RegistrantOrganization>
            </RegistrantProfile>
        </RegistrantProfiles>
        <TotalPageNum>6</TotalPageNum>
        <NextPage>true</NextPage>
    </QueryRegistrantProfilesResponse>
    ```

-   JSON  format

    ```
    {
      "CurrentPageNum": 1,
      "NextPage": true,
      "PageSize": 2,
      "PrePage": false,
      "RegistrantProfiles": {
        "RegistrantProfile": [
          {
            "Address": "aqqqq",
            "City": "us",
            "Country": "US",
            "CreateTime": "Dec 25,2017 03:20:30",
            "DefaultRegistrantProfile": true,
            "Email": "a@xxx.com",
            "EmailVerificationStatus": 0,
            "PostalCode": "010101",
            "Province": "qa",
            "RegistrantName": "x",
            "RegistrantOrganization": "xxx",
            "RegistrantProfileId": 5170612,
            "TelArea": "010",
            "Telephone": "11119999",
            "UpdateTime": "Dec 25,2017 03:21:59"
          },
          {
            "Address": "xx District",
            "City": "Beijing",
            "Country": "MO",
            "CreateTime": "Nov 22,2017 09:20:40",
            "DefaultRegistrantProfile": false,
            "Email": "abctest@xxx.com",
            "EmailVerificationStatus": 0,
            "PostalCode": "100086",
            "Province": "Beijing",
            "RegistrantName": "lk",
            "RegistrantOrganization": "lk",
            "RegistrantProfileId": 5049715,
            "TelArea": "853",
            "Telephone": "15600000000",
            "UpdateTime": "Nov 22,2017 09:20:40"
          }
        ]
      },
      "RequestId": "8843D641-7520-4399-9FCC-BFB90C068E6F",
      "TotalItemNum": 11,
      "TotalPageNum": 6
    }
    ```


