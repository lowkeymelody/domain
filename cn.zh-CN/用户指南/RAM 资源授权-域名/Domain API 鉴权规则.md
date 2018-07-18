# Domain API 鉴权规则 {#concept_d3r_f2d_n2b .concept}

本文档介绍 Domain API 鉴权规则。

Domain API 发生子账号访问主账号资源时的鉴权规则。

当子账号通过 Domain Open API 对主账号的 Domain 资源进行访问时，Domain 后台向 RAM 进行权限检查，以确保资源拥有者的确将相关资源的相关权限授予了调用者。

每个不同的 Domain API 会根据涉及到的资源以及 API 的语义来确定需要检查哪些资源的权限。具体地，每个 API 的鉴权规则见下表：

|API|鉴权 Action|鉴权 Resource|
|:--|:--------|:----------|
|SaveSingleTaskForUpdatingContactInfo|domain:DomainInfoModification|acs:domain:\*:$accountid:domain/$domainName |
|SaveBatchTaskForUpdatingContactInfoByNewContact|acs:domain:\*:$accountid:domain/$domainName |
|SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId|acs:domain:\*:$accountid:domain/$domainName |
|SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID|acs:domain:\*:$accountid:domain/$domainName |
|SaveTaskForUpdatingRegistrantInfoByIdentityCredential|acs:domain:\*:$accountid:domain/$domainName |
|SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID|domain:RealNameVerificationOperation|acs:domain:\*:$accountid:domain/$domainName |
|CancelDomainVerification|acs:domain:\*:$accountid:domain/$domainName |
|SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential|acs:domain:\*:$accountid:domain/$domainName |
|TransferInReenterTransferAuthorizationCode|domain:DomainTransferInOperation|acs:domain:\*:$accountid:domain/$domainName |
|TransferInRefetchWhoisEmail|acs:domain:\*:$accountid:domain/$domainName |
|TransferInResendMailToken|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForCancelingTransferIn|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForCancelingTransferOut|domain:DomainTransferOutOperation|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForQueryingTransferAuthorizationCode|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForModifyingDnsHost|domain:DnsHostModification|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForCreatingDnsHost|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForSynchronizingDnsHost|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForDeletingDnsHost|acs:domain:\*:$accountid:domain/$domainName|
|SaveBatchTaskForModifyingDomainDns|domain:DnsModification|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForTransferProhibitionLock|domain:SecuritySetting|acs:domain:\*:$accountid:domain/$domainName |
|SaveBatchTaskForTransferProhibitionLock|acs:domain:\*:$accountid:domain/$domainName |
|SaveSingleTaskForUpdateProhibitionLock|acs:domain:\*:$accountid:domain/$domainName |
|SaveBatchTaskForUpdateProhibitionLock|acs:domain:\*:$accountid:domain/$domainName|

| | | |
|:-|:-|:-|
|QueryDomainList|domain:QueryCommonInfo|acs:domain:\*:$accountid:\* |
|QueryDomainByInstanceId|acs:domain:\*:$accountid:\* |
|QueryContactInfo|acs:domain:\*:$accountid:\* |
|QueryDomainSuffix|acs:domain:\*:$accountid:\* |
|QueryAdvancedDomainList|acs:domain:\*:$accountid:\* |
|VerifyContactField|acs:domain:\*:$accountid:\* |
|QueryTaskList|domain:QueryDomainTask|acs:domain:\*:$accountid:\* |
|QueryTaskInfoHistory|acs:domain:\*:$accountid:\* |
|QueryTaskDetailList|acs:domain:\*:$accountid:\* |
|QueryTaskDetailHistory|acs:domain:\*:$accountid:\* |
|PollTaskResult|acs:domain:\*:$accountid:\* |
|QueryChangeLogList|domain:QueryChangeLog|acs:domain:\*:$accountid:\* |
|QueryTransferInByInstanceId|domain:QueryDomainTransferIn|acs:domain:\*:$accountid:\* |
|QueryTransferInList|acs:domain:\*:$accountid:\* |
|CheckTransferInFeasibility|acs:domain:\*:$accountid:\* |
|TransferInCheckMailToken|domain:TransferInCheckMailToken|acs:domain:\*:$accountid:\* |
|QueryTransferOutInfo|domain:QueryDomainTransferOut|acs:domain:\*:$accountid:\* |
|QueryDnsHost|domain:QueryDnsHost|acs:domain:\*:$accountid:\* |
|QueryFailReasonForRegistrantProfileRealNameVerification|domain:QueryRegistrantProfile|acs:domain:\*:$accountid:\* |
|QueryRegistrantProfileRealNameVerificationInfo|acs:domain:\*:$accountid:\* |
|QueryRegistrantProfiles|acs:domain:\*:$accountid:\* |
|QueryDomainGroupList|domain:QueryDomainGroup|acs:domain:\*:$accountid:\* |
|QueryFailReasonForDomainRealNameVerification|domain:QueryRealNameVerification|acs:domain:\*:$accountid:\* |
|QueryDomainRealNameVerificationInfo|acs:domain:\*:$accountid:\* |
|ListEmailVerification|domain:QueryEmailVerification|acs:domain:\*:$accountid:\* |
|QueryEmailVerification|acs:domain:\*:$accountid:\* |
|AcknowledgeTaskResult|domain:AcknowledgeTaskResult|acs:domain:\*:$accountid:\* |
|SaveRegistrantProfile|domain:RegistrantProfileOperation|acs:domain:\*:$accountid:\* |
|DeleteRegistrantProfile|acs:domain:\*:$accountid:\* |
|RegistrantProfileRealNameVerification|acs:domain:\*:$accountid:\* |
|DeleteDomainGroup|domain:DomainGroupOperation|acs:domain:\*:$accountid:\* |
|SaveDomainGroup|acs:domain:\*:$accountid:\* |
|UpdateDomainToDomainGroup|acs:domain:\*:$accountid:\* |
|DeleteEmailVerification|domain:EmailVerificationOperation|acs:domain:\*:$accountid:\* |
|VerifyEmail|acs:domain:\*:$accountid:\* |
|ResendEmailVerification|acs:domain:\*:$accountid:\* |
|SubmitEmailVerification|acs:domain:\*:$accountid:\* |
|SaveBatchDomainRemark|domain:DomainInfoModification|acs:domain:\*:$accountid:\* |

