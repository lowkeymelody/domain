# Domain transfer FAQs {#concept_twj_bpd_b2b .concept}

-   [How long does it take to transfer a domain name to Alibaba CLoud?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_kqg_zpd_b2b)
-   [What is the registrar information of Alibaba Cloud?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_mqg_zpd_b2b)
-   [How long can I keep the transfer key unused?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_nqg_zpd_b2b)
-   [How to smoothly transfer a domain name that is in use to Alibaba Cloud?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_oqg_zpd_b2b)
-   [What can I do if the current domain registrar does not allow domain transfer out?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_qqg_zpd_b2b)
-   [What should I do if I receive the message “The domain name is in Transfer Prohibited status, and cannot be transferred”?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_rqg_zpd_b2b)
-   [What should I do if I receive the message “Sorry. Your domain transfer key is incorrect”?](reseller.en-US/FAQ/Registration and Verification Issues/Domain transfer FAQs.md#section_tqg_zpd_b2b)

## How long does it take to transfer a domain name to Alibaba CLoud? {#section_kqg_zpd_b2b .section}

Typically this depends on your current domain registrar. You must have their approval to proceed with the transfer process. 5-7 days is the standard given to registrars by ICANN.

## What is the registrar information of Alibaba Cloud? {#section_mqg_zpd_b2b .section}

When you transfer a domain name from another registrar to Alibaba Cloud, the current registrar will require you to provide the registrar information of Alibaba Cloud. This information is as follows:

Full name: Alibaba Cloud Computing Co., Ltd. \(former HiChina\)

Contact: 95187-1

## How long can I keep the transfer key unused? {#section_nqg_zpd_b2b .section}

Domain transfer key is valid within 15 days. After obtaining the transfer key, you must complete transfer process at the new registrar as soon as possible. If the transfer key expires, you have to apply for a new transfer key.

## How to smoothly transfer a domain name that is in use to Alibaba Cloud? {#section_oqg_zpd_b2b .section}

When you plan to transfer a domain name you are using \(such as a domain name for a website or mailbox\) to Alibaba Cloud, follow these steps to smooth the transfer process:

1.  Configure DNS settings for your domain name in the Alibaba Cloud DNS console.
2.  Go to your current registrar, and modify the DNS server of your domain name to ns1.alidns.com and ns2.alidns.com. Submit the transfer application.

Make sure that the DNS resolution records you add at Alibaba Cloud DNS are in sync with that at the previous DNS provider within 48 hours after you change the DNS server.

For more information, see [transfer domain name to Alibaba Cloud](../../../../reseller.en-US/User Guide/Domain name transfer/Transfer your domain name to Alibaba Cloud.md#).

## What can I do if the current domain registrar does not allow domain transfer out? {#section_qqg_zpd_b2b .section}

If your current registrar restricts or rejects domain transfer out, you can file a complaint at:

[Contacting ICANN Regarding Contractual Compliance Complaint](http://reports.internic.net/cgi/registrars/problem-report.cgi?spm=a2c4g.11186623.2.21.VgStC5&file=problem-report.cgi)

.

## What should I do if I receive the message “The domain name is in Transfer Prohibited status, and cannot be transferred”? {#section_rqg_zpd_b2b .section}

This is because the domain name is in the Transfer Prohibited status. You can contact your current registrar to remove this status.

You can go to the Alibaba Cloud WHOIS search page to view the domain status.

## What should I do if I receive the message “Sorry. Your domain transfer key is incorrect”? {#section_tqg_zpd_b2b .section}

This is because the domain transfer key is incorrect.  You must request a new domain transfer key from your current registrar.

For more information, see [obtain a domain transfer key](../../../../reseller.en-US/User Guide/Domain name transfer/Conditions and procedures to get an authorization code.md#).

**Note:** 

-   Do not add any space when entering the transfer key. We recommend that you enter the key manually.
-   The transfer key contains special characters. You must enter the complete transfer key provided by your current registrar. Note that the ending parenthesis may be a part of the key.
-   You must contact your current registrar to obtain the transfer key. Alibaba Cloud cannot do it on your behalf.
-   Alibaba Cloud cannot manually verify the transfer key. You can only wait for the system to verify the key. If you have entered the incorrect key multiple times, you can contact your current registrar to confirm the transfer key.

