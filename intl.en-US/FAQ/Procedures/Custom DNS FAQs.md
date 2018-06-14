# Custom DNS FAQs {#concept_gp2_2sd_b2b .concept}

-   [What is a custom DNS?](#section_rbt_xsd_b2b)
-   [What does a server name consist of?](#section_sbt_xsd_b2b)
-   [How many DNSs can be created at most?](#section_tbt_xsd_b2b)
-   [Is IPv6 supported?](#section_ubt_xsd_b2b)
-   [How many IP addresses are supported at most?](#section_vbt_xsd_b2b)
-   [Can a server name be changed or deleted?](#section_wbt_xsd_b2b)
-   [Can an IP address be changed or deleted?](#section_xbt_xsd_b2b)
-   [What else do I do after a DNS is created successfully?](#section_ybt_xsd_b2b)
-   [Does a server become effective immediately after being created?](#section_act_xsd_b2b)

## What is a custom DNS? {#section_rbt_xsd_b2b .section}

A custom DNS is created by you using an existing domain name to provide resolution services. Professional background is required to create such a server. What else do Otherwise, we recommend that you directly use DNS resolution services of a domain name provider.

## What does a server name consist of? {#section_sbt_xsd_b2b .section}

A valid DNS name must consist of letters \(a-z, case-insensitive\), numbers \(0-9\), period \(.\), and dash \(-\), and be limited to 80 characters. A DNS name cannot start or end with the period or dash.  Spaces and special characters are not allowed.

We recommend that you use dns or ns in a server name. For example, dns1.yourdomain.com / dns2.yourdomain.com.

## How many DNSs can be created at most? {#section_tbt_xsd_b2b .section}

A maximum of 13 DNS names can be created, as specified by the Registry.

## Is IPv6 supported? {#section_ubt_xsd_b2b .section}

Yes.

## How many IP addresses are supported at most? {#section_vbt_xsd_b2b .section}

A minimum of one and a maximum of 13 IP addresses can be added for a DNS, as specified by the Registry.

## Can a server name be changed or deleted? {#section_wbt_xsd_b2b .section}

No. Take extra caution when you create it.

## Can an IP address be changed or deleted? {#section_xbt_xsd_b2b .section}

Yes. But at least one IP address must be retained.

## What else do I do after a DNS is created successfully? {#section_ybt_xsd_b2b .section}

Before or after a DNS name is created, you must add a corresponding A record to the current DNS. Only after such operation will a created DNS become effective.

For example, you want to create a DNS “ns1.a.com” using the domain name “a.com”. \(Suppose the IP address is 1.1.1.1\).

-   If the domain name "a.com” uses Alibaba Cloud DNS ns1.hichina.com/ns2.ahichina.com,

    before or after the DNS ns1.a.com is created, you must add an A record of “ns1.a.com” to Alibaba Cloud DNS to point to the created IP address \(1.1.1.1\).

-   If the created DNS “ns1.a.com” is used to resolve the current domain name “a.com”, you must add an A record to the server for “ns1.a.com”  \(Suppose the IP address is 1.1.1.1\).


## Does a server become effective immediately after being created? {#section_act_xsd_b2b .section}

Generally it becomes effective within a few minutes after being created.

