# Signature {#concept_t5d_35b_b2b .concept}

DNS performs identity authentication on each access request. Therefore, both HTTP requests and HTTPS requests must contain signature information. The service performs symmetric encryption by using the AccessKeyID and AccessKeySecret to authenticate the request sender.

The AccessKeyID and AccessKeySecret are officially issued to you by Alibaba Cloud. \(You can apply for and manage them on the Alibaba Cloud website.\) The AccessKeyID indicates your identity. The AccessKeySecret is the key used to encrypt a signature string and to verify the signature string on the server. It must be kept strictly confidential and only available to you and Alibaba Cloud.

## Procedure {#section_bfp_dxb_b2b .section}

Follow these steps to sign the access request:

1.  Construct the Canonicalized Query String by using the request parameters.
    1.  Sort the parameters. Sort the request parameters alphabetically by parameter name. \(The request parameters include the “public request parameters” and the custom parameters for the API, but do not include the Signature parameter mentioned in the “public request parameters”.\)

        **Note:** When a request is submitted by using the GET method, these parameters are in the parameter section of the request URI. The section in the URI follows a question mark \(?\) and connected by an ampersand \(&\).

    2.  Encode the parameters. Perform URL encoding for names and values of sorted request parameters by using the UTF-8 character set. The encoding rules are as follows:

        -   Uppercase letters \(A–Z\), lowercase letters \(a–z\), numbers \(0–9\), hyphens \(-\), underscores \(\_\), periods \(.\), and tildes \(~\) are not encoded.
        -   Other characters are encoded in  `%XY` format, with XY representing the characters’ ASCII code  in hexadecimal notation. For example, the English double quotes \(“\) are encoded as `%22`.
        -   Extended UTF-8 characters are encoded in `%XY%ZA…` format.
        -   It must be noted that the English space is encoded as `%20`, rather than the plus sign \(+\).
        **Note:** 

        This encoding method is similar to the `application/x-www-form-urlencoded` MIME-type encoding algorithm \(for example, java.net.URLEncoder of Java\), but is different from it. If this encoding method is used, encode parameters by following the standard library, replace the plus signs \(+\) in the encoded strings with `%20`, the asterisks \(\*\) with `%2A`, and change `%7E` back to the tilde \(~\) to conform to the preceding encoding rules. This algorithm can be achieved by using the `percentEncode` method as follows:

        ```
        private static final String ENCODING = "UTF-8";
        private static String percentEncode(String value) throws UnsupportedEncodingException {
        return value ! = null ? URLEncoder.encode(value, ENCODING).replace("+", "%20").replace("*", "%2A").replace("%7E", "~") : null;
        }
        ```

    3.  Connect the encoded parameter names and values with the English equals sign \(=\).
    4.  Sort the parameter name and value pairs connected by equal signs in alphabetical order, and connect them with & to produce the Canonicalized Query String.
2.  Use the Canonicalized Query String to construct the string to be signed according to the following rules:

    ```
    StringToSign=
     HTTPMethod + “&” +
     percentEncode(“/”) + ”&” +
     percentEncode(CanonicalizedQueryString)
    ```

    Where,

    -   HTTPMethod indicates the HTTP method used for request submission, for example, GET.
    -   percentEncode\(/\) indicates the encoded value for the character \(/\) according to the URL encoding rules described in 1.b, namely `%2F`.
    -   percentEncode\(CanonicalizedQueryString\) indicates the encoded string of the Canonicalized Query String constructed in step 1, produced by following the URL encoding rules described in 1.b.
3.  Calculate the HMAC value of the `StringToSign` string based on the definition of [RFC 2104](http://www.ietf.org/rfc/rfc2104.txt) .

    **Note:** When the signature is calculated, the key is the `AccessKeySecret` held by the user plus the \(&\) character \(ASCII:38\), and the SHA1 hashing algorithm is used.

4.  According to Base64 encoding rules, encode the preceding HMAC value into a string to obtain the signature value.
5.  Add the signature value to the request parameters as the `Signature` parameter to sign the request.

    **Note:** When the obtained signature value is submitted to the Domain server as the final request parameter value, the value is URL encoded like other parameters according to [RFC3986](http://tools.ietf.org/html/rfc3986) rules.


## Example {#section_cll_5xb_b2b .section}

Take checkDomain as an example. If the AccessKeyID is testid and the AccessKeySecret is testsecret, the request URL before signing is as follows:

```
http://domain-intl.aliyuncs.com/
? TimeStamp=2017-12-26T06%3A04%3A54Z
&Format=JSON
&AccessKeyId=testid
&Action=CheckDomain
&SignatureMethod=HMAC-SHA1
&SignatureNonce=5033a7d9-dfeb-417d-9fdf-13459fe90c1a
&Version=2017-12-18
&SignatureVersion=1.0`
```

The calculated StringToSign is as follows:

```
GET&%2F&AccessKeyId%3Dtestid&Action%3DCheckDomain&Format%3DJSON&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3D5033a7d9-dfeb-417d-9fdf-13459fe90c1a&SignatureVersion%3D1.0&TimeStamp%3D2016-05-19T09%253A06%253A05Z&Version%3D2016-05-11
```

The value of AccessKeySecret is testsecret. Therefore, the key used for HMAC calculation is testsecret&. The calculated signature value is as follows:

```
WXkgFH4ymmnCjSUM65f6I1n7%2FUs=
```

Add the signature value to the URL request as the Signature parameter. The following URL is obtained:

```
http://domain-intl.aliyuncs.com/
? Format=JSON
&AccessKeyId=testid
&Action=CheckDomain
&SignatureMethod=HMAC-SHA1
&RegionId=cn-hangzhou
&DomainName=test.com
&SignatureNonce=b2d61eac-ecb7-453b-98bc-726871a7a310
&SignatureVersion=1.0
&Version=2017-12-18
&Signature=3WrgmEE%2BW1XqUY%2FFyS2GRohBbZA%3D
&Timestamp=2017-12-26T06%3A04%3A54Z
```

