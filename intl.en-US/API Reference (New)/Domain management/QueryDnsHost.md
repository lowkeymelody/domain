# QueryDnsHost {#concept_xwb_wjq_b2b .concept}

QueryDnsHost: queries the DNS host.

## Request parameters {#section_kn5_xdm_c2b .section}

For more information about public request parameters, see [Public parameters](intl.en-US/API Reference (New)/Calling method/Public parameters.md#).

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|API of the action, system required parameter. Set this parameter to QueryDnsHost.|
|InstanceId|String|Yes|Instance ID.Instance ID can be queried by calling [QueryDomainList](intl.en-US/API Reference (New)/Domain management/QueryDomainList.md#).

|
|Lang|String|No|Language of the error message returned from the API. The enumerated values include zh \(Chinese\) and en \(English\).  The default value is en.|

## Response parameters {#section_s3t_g2m_c2b .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|Unique request identifier|
|DnsHostList|[DnsHostType](#table_gjw_k2m_c2b)|DNS host information.|

|Parameter|Type|Description|
|:--------|:---|:----------|
|DnsName|String|Domain name.|
|IpList|IpListType|IP address list.|

## Error codes {#section_gy3_r2m_c2b .section}

|Error code|Description| HTTP status code|Meaning|
|:---------|:----------|:----------------|:------|
|ParameterIllegal|Parameter illegal.|400|Parameter error.|
|Networkioerror|Network IO Error.|400|Network I/O exception.|

## Examples {#section_lxh_52m_c2b .section}

**Request example**

```
http://domain-intl.aliyuncs.com/?Action=QueryDnsHost
&InstanceId=ST2017120814571100001303
&<Public request parameters>
```

**Response example**

-   XML format

    ```
    <? xml version='1.0' encoding='UTF-8'? >
    <QueryDnsHostResponse>
        <DnsHostList>
            <DnsHost>
                <DnsName>ns3</DnsName>
                <IpList>
                    <ip>185.27.134.201</ip>
                    <ip>218.83.159.236</ip>
                </IpList>
            </DnsHost>
        </DnsHostList>
        <RequestId>18A313DD-3AF3-40AA-84F9-56BA45DC511F</RequestId>
    </QueryDnsHostResponse>
    ```

-   JSON format

    ```
    {
      "dnsHostList": [
        {
          "dnsName": "ns3",
          "ipList": [
            "185.27.134.201",
            "218.83.159.236"
          ]
        }
      ],
      "requestId": "6A973B69-7B5F-4959-AA89-ED4010541D20"
    }
    ```


