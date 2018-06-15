# Request structure {#concept_if4_g5b_b2b .concept}

## Service address {#section_ofb_kvb_b2b .section}

The domain name API service access address is `domain-intl.aliyuncs.com`.

## Communication protocols {#section_xls_qvb_b2b .section}

The system supports request communication through HTTP or HTTPS. HTTPS is recommended for higher security.

## Request methods {#section_qjj_svb_b2b .section}

The system allows you to send HTTP GET or POST requests. HTTP GET requires request parameters to be included in the request URL.

## Request parameters {#section_m2p_tvb_b2b .section}

For each request, the operation to be executed must be specified by using the Action parameter \(for example, CheckDomain\). Each operation must contain the public request parameters and the specific request parameters of the specified operation.

-   When the GET method is used, the request parameters must be included in the request URL.
-   When the POST method is used, the request parameters are placed in HEAD.

This guide uses the GET method in all examples.

## Character encoding {#section_fm2_vvb_b2b .section}

Requests and returned results are both encoded by using the UTF-8 character set.

