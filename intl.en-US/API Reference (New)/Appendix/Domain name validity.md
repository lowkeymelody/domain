# Domain name validity {#concept_mhb_dmq_b2b .concept}

A valid domain name is subject to the following limits:

-   Domain names are case-insensitive and do not distinguish between simplified and traditional Chinese characters.

-   A valid domain name must contain 1–63 characters \(excluding the suffix\).

-   A valid English domain name consists of lowercase letters \(a–z\), numbers \(0–9\), and hyphens \(-\). But a hyphen is not allowed in the string head, tail, and the third and fourth character positions.

-   A valid Chinese domain name must contain at least one Chinese character \(simplified or traditional\) in addition to the valid English characters. The length of a Chinese domain name is measured in punycode after conversion.

-   Request parameters starting with “xn—“ \(punycode\) are not supported. You must use a Chinese domain name as the request parameter.


