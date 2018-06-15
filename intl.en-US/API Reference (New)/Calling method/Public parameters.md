# Public parameters {#concept_vbz_4jb_b2b .concept}

## Public request parameters {#section_v5c_s5b_b2b .section}

Public request parameters are the request parameters used in each API.

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Format|String|No|Type of value returned. JSON and XML are supported. The default type is XML.|
|Version|String|Yes|API version number, in the `YYYY-MM-DD` format. The current version number is `2018-01-29`.|
|AccessKeyId|String|Yes| Your Key ID issued by Alibaba Cloud for access to the service.|
|Signature|String|Yes|Signature result string. For more information about the signature calculation method, see [Signature](intl.en-US/API Reference (New)/Calling method/Signature.md#).|
|SignatureMethod|String|Yes|Signature method. HMAC-SHA1 is currently supported.|
|Timestamp|String|Yes|Time stamp of a request. The date format follows the ISO 8601 standard and uses UTC time. The format is `YYYY-MM-DDThh:mm:ssZ`. For example: `2018-01-29T12:00:00Z` \(12:00:00 on January 29, 2018 UTC\).|
|SignatureVersion|String|Yes|Signature algorithm version. The current version is 1.0.|
|SignatureNonce|String|Yes|A unique random number, used to prevent replay attacks. Different random numbers must be used for different requests.|

**Example**

```
https://domain-intl.aliyuncs.com/
? Format=xml
&Version=2017-12-18    
&Signature=Pc5WB8gokVn0xfeu%2FZV%2BiNM1dgI%3D     
&SignatureMethod=HMAC-SHA1    
&SignatureNonce=15215528852396   
&SignatureVersion=1.0   
&AccessKeyId=key-test   
&Timestamp=2017-12-25T12:00:00Z   
…
```

## Public response parameters {#section_wpb_y5b_b2b .section}

The system returns a unique identification code \(RequestId\) each time you send a request to call an API, no matter the call is successful or not.

**Example**

XML format

```
<? xml version="1.0" encoding="UTF-8"? > 
<!—Result root node-->
<API name+Response>
    <!—Returned request tag-->
    <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
    <!—Returned results-->
</API name+Response>
```

JSON format

```
{
    "RequestId": "4C467B38-3910-447D-87BC-AC049166F216"
    /* Returned results */
}
```

