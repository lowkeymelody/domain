# QueryDomainByInstanceId {#concept_xl3_qqy_b2b .concept}

The QueryDomainByInstanceId API queries the basic information about a domain name by the domain name ID.

## Request parameters {#section_yll_kfm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryDomainByInstanceId.|
|InstanceId|String|Yes|Domain name instance ID.|

## Response parameters {#section_yz3_nfm_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier.|
|UserId|String|Alibaba Cloud user ID.|
|DomainName|String|Domain name.|
|InstanceId|String|Domain name instance ID.|
|RegistrationDate|String|Registration time.|
|ExpirationDate|String|Expiration time.|
|RegistrantOrganization|String|Owner of the domain name.|
|RegistrantName|String|Contact.|
|Email|String|Email address of the domain name owner.|
|EmailVerificationClientHold|Boolean|Whether it is in clientHold status.|
|Emailverificationstatus|Boolean|Whether the email address is verified. The enumerated values include: 0 : The email address fails to be verified. 1 : The email address is verified.|
|UpdateProhibitionLock|String|Domain name security lock status. The enumerated values include: NONE\_SETTING : Not set. OPEN: Enabled. CLOSE : Disabled.|
|TransferProhibitionLock|String|Domain name transfer lock status. The enumerated values include: NONE\_SETTING : Not set. OPEN: Enabled. CLOSE : Disabled.|
|DomainNameProxyService|Boolean|Whether the privacy protection service is enabled.|
|Premium|Boolean|Whether it is a premium domain name.|
|DnsList|[DnsListType](#table_m3n_xfm_c2b)|DNS list.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|dns|String|DNS information.|

## Examples {#section_kzj_kgm_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryDomainByInstanceId
&InstanceId=S201312050017225
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryDomainByInstanceIdResponse>
        <DomainNameProxyService>false</DomainNameProxyService>
        <InstanceId>S201312050000000</InstanceId>
        <RegistrationDate>2013-12-06 00:00:00</RegistrationDate>
        <Email>test@aliyun.com</Email>
        <UserId>1344371</UserId>
        <RegistrantName>sadf sdf</RegistrantName>
        <ExpirationDate>2016-12-06 00:00:00</ExpirationDate>
        <DomainName>fds234sdf.net</DomainName>
        <UpdateProhibitionLock>NONE_SETTING</UpdateProhibitionLock>
        <DnsList>
            <Dns>dns19.hichina.com</Dns>
            <Dns>dns20.hichina.com</Dns>
        </DnsList>
        <TransferProhibitionLock>CLOSE</TransferProhibitionLock>
        <RegistrantOrganization>safd</RegistrantOrganization>
    </QueryDomainByInstanceIdResponse>
    ```

-   JSON format

    ```
    {
      "DomainNameProxyService": false,
      "InstanceId": "S201312050000000",
      "RegistrationDate": "2013-12-06 00:00:00",
      "Email": "test@aliyun.com",
      "UserId": "1344371",
      "RegistrantName": "sadf sdf",
      "ExpirationDate": "2016-12-06 00:00:00",
      "DomainName": "fds234sdf.net",
      "UpdateProhibitionLock": "NONE_SETTING",
      "DnsList": {
        "Dns": [
          "dns19.hichina.com",
          "dns20.hichina.com"
        ]
      },
      "TransferProhibitionLock": "CLOSE",
      "RegistrantOrganization": "safd"
    }
    ```


