# QueryDomainList {#concept_pky_ryk_c2b .concept}

The QueryDomainList queries the list of domain names under the current account and returns the results by page.

## Request parameters {#section_zcp_r3m_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryDomainList.|
|PageNum|Integer|Yes|Page number.|
|PageSize|Integer|Yes|Page size.|
|Orderkeytype|String|No|Sorting field. The enumerated values include: RegistrationDate Sort the domain names by registration time; ExpirationDate Sort the domain names by expiration time. If this parameter is not set, domain names are sorted by storage time by default.|
|OrderByType|String|No|Sorting order. The enumerated values include: ASC ascending order. DESC descending order. If this parameter is not set, the default value DESC is used.|
|StartRegistratonDate|Long|No|Start time of the period in which domain names are registered, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|EndRegistrationDate|Long|No|End time of the period in which domain names are registered, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|StartExpirationDate|Long|No|Start time of the period in which domain names expire, expressed by the number of milliseconds between the start time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|EndExpirationDate|Long|No|End time of the period in which domain names expire, expressed by the number of milliseconds between the end time and the UTC time 00:00 on January 1, 1970. Currently, only query by day is supported.|
|Lang|String|No|Language of the information returned from the API. The enumerated values include: zh \(Chinese\) and en \(English\). If this parameter is not set, the default value en is used.|
|DomainName|String|No|Domain name search.|
|ProductDomainType|String|No|Domain name type. The enumerated values include: New gTLD; gTLD; ccTLD.|
|QueryType|String|No|Query list type. The enumerated values include: 1: Domain names that urgently need renewal. 2 : Domain names that urgently need redemption.|

## Response parameters {#section_dfj_djm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier|
|TotalItemNum|Integer|Total number of domain names.|
|CurrentPageNum|Integer|The current page number.|
|TotalPageNum|Integer|Total number of pages.|
|PageSize|Integer|Page size.|
|PrePage|Boolean|Whether the previous page exists.|
|NextPage|Boolean|Whether the next page exists.|
|Data|[Domaininfotype](#table_kt3_3jm_c2b)|Domain name list|

|Parameter|Type|Description|
|:--------|:---|:----------|
|DomainName|String|Domain name.|
|InstanceId|String|Instance ID.|
|RegistrationDate|String|Domain name registration time.|
|RegistrationDateLong|Long|Domain name registration time, expressed by the number of milliseconds between the registration time and the UTC time 00:00 on January 1, 1970.|
|ExpirationDate|String|Domain name expiration time.|
|ExpirationDateLong|Long|Domain name expiration time, expressed by the number of milliseconds between the expiration time and the UTC time 00:00 on January 1, 1970.|
|DomainStatus|String|Domain name status. The enumerated values include: 1: Renewal badly needed. 2 : Redemption badly need. 3: Normal.|
|DomainType|String|Domain name type. The enumerated values include New gTLD;gTLD; ccTLD.|
|Premium|Boolean|Whether it is a premium domain name.|
|ProductId|String|Product ID.|

## Error codes {#section_upg_rjm_c2b .section}

|Error code|Description| HTTP status code|Semantics|
|:---------|:----------|:----------------|:--------|
|ParameterIllegal|Parameter illegal.|400|Parameter error|
|NetworkIOError|Network IO Error.|400|Network I/O exception.|

## Examples {#section_vts_wjm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryDomainList
&PageNum=1&PageSize=10
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryDomainListResponse>
        <Data>
            <Domain>
                <ExpirationDate>Nov 02,2019 04:00:45</expirationDate>
                <InstanceId>ST20151102120031118</SaleId>
                <RegistrationDate>Nov 02,2017 04:00:45</registrationDate>
                <DomainName>test.com</DomainName>
                <DomainType>gTLD</domainType>
            </Domain>
        </Data>
        <TotalItemNum>1</TotalItemNum>
        <PageSize>5</PageSize>
        <CurrentPageNum>0</CurrentPageNum>
        <RequestId>B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E</RequestId>
        <PrePage>false</PrePage>
        <TotalPageNum>1</TotalPageNum>
        <NextPage>false</NextPage>
    </QueryDomainListResponse>
    ```

-   JSON format

    ```
    {
      "Data": {
        "Domain": [
          {
            "ExpirationDate": "Nov 02,2019 04:00:45",
            "InstanceId": "ST2015110212003800001928",
            "RegistrationDate": "Nov 02,2017 04:00:45",
            "DomainName": "fds234sdf.net",
            "DomainType": "gTLD"
          }
        ]
      },
      "TotalItemNum": 1,
      "PageSize": 5,
      "CurrentPageNum": 0,
      "RequestId": "77F90DA6-89AB-4074-80F3-E595CB57DF98",
      "PrePage": false,
      "TotalPageNum": 1,
      "NextPage": false
    }
    ```


