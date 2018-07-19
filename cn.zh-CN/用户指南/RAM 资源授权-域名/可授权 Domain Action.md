# 可授权 Domain Action {#concept_tsh_vjc_n2b .concept}

本文档介绍可授权 Domain Action。

在 RAM 中，可以对资源进行以下 Action 的授权。

|鉴权 Action|描述|API|
|:--------|:-|:--|
|域名基本信息查询 \(QueryCommonInfo\)|查询自己账户下域名列表|QueryDomainList|
|查询自己账户下域名信息|QueryDomainByInstanceId|
|查询域名联系人信息|QueryContactInfo|
|高级搜索自己账户下后缀列表|QueryDomainSuffix|
|高级搜索自己账号下域名列表|QueryAdvancedDomainList|
|校验联系人信息|VerifyContactField|
|域名任务查询 \(QueryDomainTask\)|查询域名任务列表|QueryTaskList|
|查询域名任务历史列表|QueryTaskInfoHistory|
|查询域名任务的详情列表|QueryTaskDetailList|
|查询域名任务的详情历史列表|QueryTaskDetailHistory|
|查询已经执行完成的任务详情列表|PollTaskResult|
|域名日志查询 \(QueryChangeLog\)|查询操作日志|QueryChangeLogList|
|域名信息修改操作 \(DomainInfoModification\)|提交域名信息修改任务|SaveSingleTaskForUpdatingContactInfo|
|批量保存域名备注信息|SaveBatchDomainRemark|
|提交批量通过新联系人信息域名信息修改任务|SaveBatchTaskForUpdatingContactInfoByNewContact|
|提交批量通过模板域名信息修改任务|SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId|
|提交通过信息模板 ID 修改注册联系人信息任务|SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID|
|提交批量通过联系人信息和资料修改注册联系人信息任务|SaveTaskForUpdatingRegistrantInfoByIdentityCredential|
|域名实名认证查询 \(QueryRealNameVerification\)|查询域名实名认证失败原因|QueryFailReasonForDomainRealNameVerification|
|查询实名制认证验证信息|QueryDomainRealNameVerificationInfo|
|域名实名认证操作 \(RealNameVerificationOperation\)|通过信息模板 ID 提交域名实名认证任务|SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID|
|取消域名验证|CancelDomainVerification|
|提交域名实名认证任务|SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential|
|域名转入查询 \(QueryDomainTransferIn\)|根据实例编号查询域名转入信息|QueryTransferInByInstanceId|
|查询域名转入列表|QueryTransferInList|
|校验域名是否可以转入|CheckTransferInFeasibility|
|域名转入验证邮件 \(TransferInCheckMailToken\)|域名转入验证邮件|TransferInCheckMailToken|
|域名转入操作 \(DomainTransferInOperation\)|域名转入重新输入转移密码|TransferInReenterTransferAuthorizationCode|
|域名转入重新抓取 whois 邮箱|TransferInRefetchWhoisEmail|
|域名转入重新发送验证邮件|TransferInResendMailToken|
|提交取消域名转入任务|SaveSingleTaskForCancelingTransferIn|
|域名转出操作 \(DomainTransferOutOperation\)|提交取消域名转出任务|SaveSingleTaskForCancelingTransferOut|
|提交获取域名转移密码任务|SaveSingleTaskForQueryingTransferAuthorizationCode|
|域名转出查询 \(QueryDomainTransferOut\)|查询域名转出信息|QueryTransferOutInfo|
|域名 DNSHost 查询 \(DnsHostQuery\)|查询域名 DNSHost|QueryDnsHost|
|域名 DNSHost 修改 \(DnsHostModification\)|提交修改 DNSHost 任务|SaveSingleTaskForModifyingDnsHost|
|提交创建 DNSHost 任务|SaveSingleTaskForCreatingDnsHost|
|提交同步 DNSHost 任务|SaveSingleTaskForSynchronizingDnsHost|
|提交删除 DNSHost 任务|SaveSingleTaskForDeletingDnsHost|
|域名 DNS 设置 \(DnsModification\)|提交批量修改域名 DNS 任务|SaveBatchTaskForModifyingDomainDns|
|安全设置 \(SecuritySetting\)|提交禁止转移锁任务|SaveSingleTaskForTransferProhibitionLock|
|提交批量禁止转移锁任务|SaveBatchTaskForTransferProhibitionLock|
|提交禁止更新锁任务|SaveSingleTaskForUpdateProhibitionLock|
|提交批量禁止更新锁任务|SaveBatchTaskForUpdateProhibitionLock|
|信息模板操作 \(RegistrantProfileOperation\)|创建或者保存域名信息模板|SaveRegistrantProfile|
|删除指定的域名信息模板|DeleteRegistrantProfile|
|提交信息模板实名认证|RegistrantProfileRealNameVerification|
|信息模板查询 \(QueryRegistrantProfile\)|查询模板实名认证失败原因|QueryFailReasonForRegistrantProfileRealNameVerification|
|查询域名信息模板实名认证资料|QueryRegistrantProfileRealNameVerificationInfo|
|查询自己账户下的域名信息模板|QueryRegistrantProfiles|
|域名分组操作 \(DomainGroupOperation\)|删除域名分组|DeleteDomainGroup|
|保存域名分组|SaveDomainGroup|
|向分组中设置域名|UpdateDomainToDomainGroup|
|域名分组查询 \(QueryDomainGroup\)|查询域名分组列表|QueryDomainGroupList|
|邮箱验证操作 \(EmailVerificationOperation\)|删除邮箱验证|DeleteEmailVerification|
|验证邮箱 Token|VerifyEmail|
|重新发送验证邮件|ResendEmailVerification|
|发送邮箱验证列表|SubmitEmailVerification|
|邮箱验证查询 \(QueryEmailVerification\)|查询邮箱验证列表|ListEmailVerification|
|查询邮件验证|QueryEmailVerification|
|任务确认 \(AcknowledgeTaskResult\)|确认任务详情结果|AcknowledgeTaskResult|

