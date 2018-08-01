# Domain API authentication rules {#concept_d3r_f2d_n2b .concept}

This document describes domain API authentication rules.

Sub-accounts are subject to authorization rules when accessing master account resources through the domain API.

When a sub-account requests access to domain resources of the master account by using the domain APIs, the domain backend checks authentication in RAM to ensure that the resource owner has authorized the sub-account to do so.

Based on the resources involved and the definition of API, each domain API determines resources whose permissions need to be checked accordingly. The following table describes the authentication rules for each API:

|API|Authorization action|Authorization resource|
|:--|:-------------------|:---------------------|
|[SaveSingleTaskForUpdatingContactInfo](https://help.aliyun.com/document_detail/69378.html)|domain:DomainInfoModification|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForUpdatingContactInfo](https://help.aliyun.com/document_detail/67721.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](https://help.aliyun.com/document_detail/67720.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[TransferInReenterTransferAuthorizationCode](https://help.aliyun.com/document_detail/69385.html)|domain:DomainTransferInOperation|acs:cdn:\*:$accountid:domain/$domainName|
|[TransferInRefetchWhoisEmail](https://help.aliyun.com/document_detail/69386.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[TransferInResendMailToken](https://help.aliyun.com/document_detail/69384.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForCancelingTransferIn](https://help.aliyun.com/document_detail/69374.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForCancelingTransferOut](https://help.aliyun.com/document_detail/69373.html)|domain:DomainTransferOutOperation|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](https://help.aliyun.com/document_detail/69368.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForModifyingDnsHost](https://help.aliyun.com/document_detail/69376.html)|domain:DnsHostModification|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForCreatingDnsHost](https://help.aliyun.com/document_detail/69367.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForSynchronizingDnsHost](https://help.aliyun.com/document_detail/69375.html)|acs:cdn:\*:$accountid:domain/$domainName|
|SaveSingleTaskForDeletingDnsHost|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForModifyingDomainDns](https://help.aliyun.com/document_detail/67722.html)|domain:DnsModification|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForTransferProhibitionLock](https://help.aliyun.com/document_detail/69370.html)|domain:SecuritySetting|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForTransferProhibitionLock](https://help.aliyun.com/document_detail/67718.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveSingleTaskForUpdateProhibitionLock](https://help.aliyun.com/document_detail/69369.html)|acs:cdn:\*:$accountid:domain/$domainName|
|[SaveBatchTaskForUpdateProhibitionLock](https://help.aliyun.com/document_detail/67717.html)|acs:cdn:\*:$accountid:domain/$domainName|

|API|Authorization action|Authorization resource|
|:--|:-------------------|:---------------------|
|[QueryDomainList](https://help.aliyun.com/document_detail/67712.html)|domain:QueryCommonInfo|acs:domain:\*:$accountid:\* |
|[QueryDomainByInstanceId](https://help.aliyun.com/document_detail/67714.html)|acs:domain:\*:$accountid:\* |
|[QueryContactInfo](https://help.aliyun.com/document_detail/67706.html)|acs:domain:\*:$accountid:\* |
|[VerifyContactField](https://help.aliyun.com/document_detail/69381.html)|acs:domain:\*:$accountid:\* |
|[QueryTaskList](https://help.aliyun.com/document_detail/67709.html)|domain:QueryDomainTask|acs:domain:\*:$accountid:\* |
|[QueryTaskInfoHistory](https://help.aliyun.com/document_detail/67707.html)| acs:domain:\*:$accountid:\* |
|[QueryTaskDetailList](https://help.aliyun.com/document_detail/67710.html)|acs:domain:\*:$accountid:\* |
|[QueryTaskDetailHistory](https://help.aliyun.com/document_detail/67708.html)|acs:domain:\*:$accountid:\* |
|[PollTaskResult](https://help.aliyun.com/document_detail/69361.html)|acs:domain:\*:$accountid:\* |
|[QueryChangeLogList](https://help.aliyun.com/document_detail/67705.html)|domain:QueryChangeLog|acs:domain:\*:$accountid:\* |
|[QueryTransferInByInstanceId](https://help.aliyun.com/document_detail/69365.html)|domain:QueryDomainTransferIn|acs:domain:\*:$accountid:\* |
|[QueryTransferInList](https://help.aliyun.com/document_detail/69364.html)|acs:domain:\*:$accountid:\* |
|[CheckTransferInFeasibility](https://help.aliyun.com/document_detail/69382.html)|acs:domain:\*:$accountid:\* |
|[TransferInCheckMailToken](https://help.aliyun.com/document_detail/69383.html)|domain:TransferInCheckMailToken|acs:domain:\*:$accountid:\* |
|[QueryTransferOutInfo](https://help.aliyun.com/document_detail/69363.html)|domain:QueryDomainTransferOut|acs:domain:\*:$accountid:\* |
|[QueryDnsHost](https://help.aliyun.com/document_detail/69360.html)|domain:QueryDnsHost|acs:domain:\*:$accountid:\* |
|[QueryRegistrantProfiles](https://help.aliyun.com/document_detail/67701.html)|domain:QueryRegistrantProfile|acs:domain:\*:$accountid:\* |
|[ListEmailVerification](https://help.aliyun.com/document_detail/67711.html)|domain:QueryEmailVerification|acs:domain:\*:$accountid:\* |
|[AcknowledgeTaskResult](https://help.aliyun.com/document_detail/69366.html)|domain:AcknowledgeTaskResult|acs:domain:\*:$accountid:\* |
|[SaveRegistrantProfile](https://help.aliyun.com/document_detail/67700.html)|domain:RegistrantProfileOperation|acs:domain:\*:$accountid:\* |
|[DeleteRegistrantProfile](https://help.aliyun.com/document_detail/67702.html)|acs:domain:\*:$accountid:\* |
|[DeleteEmailVerification](https://help.aliyun.com/document_detail/67716.html)|domain:EmailVerificationOperation|acs:domain:\*:$accountid:\* |
|[VerifyEmail](https://help.aliyun.com/document_detail/67732.html)|acs:domain:\*:$accountid:\* |
|[ResendEmailVerification](https://help.aliyun.com/document_detail/67734.html)|acs:domain:\*:$accountid:\* |
|[SubmitEmailVerification](https://help.aliyun.com/document_detail/67715.html)|acs:domain:\*:$accountid:\* |

|API|Authentication action|Authentication resource|
|:--|:--------------------|:----------------------|
|\*|domain:\*|acs:domain:\*:$accountid:\*|

