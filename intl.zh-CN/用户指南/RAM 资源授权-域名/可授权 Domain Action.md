# 可授权 Domain Action {#concept_tsh_vjc_n2b .concept}

本文档介绍可授权 Domain Action。

在 RAM 中，您可以授权资源进行以下操作。

|鉴权 Action|描述|API|
|:--------|:-|:--|
|域名基本信息查询 \(QueryCommonInfo\)|查询自己账户下域名列表|[QueryDomainList](https://www.alibabacloud.com/help/zh/doc-detail/67712.htm)|
|查询自己账户下域名信息|[QueryDomainByInstanceId](https://www.alibabacloud.com/help/zh/doc-detail/67714.htm)|
|查询域名联系人信息|[QueryContactInfo](https://www.alibabacloud.com/help/zh/doc-detail/67706.htm)|
|校验联系人信息|[VerifyContactField](https://www.alibabacloud.com/help/zh/doc-detail/69381.htm)|
|域名日志查询 \(QueryChangeLog\)|查询操作日志|[QueryChangeLogList](https://www.alibabacloud.com/help/zh/doc-detail/67705.htm)|
|域名任务查询 \(QueryDomainTask\)|查询域名任务列表|[QueryTaskList](https://www.alibabacloud.com/help/zh/doc-detail/67709.htm)|
|查询域名任务历史列表|[QueryTaskInfoHistory](https://www.alibabacloud.com/help/zh/doc-detail/67707.htm)|
|查询域名任务的详情列表|[QueryTaskDetailList](https://www.alibabacloud.com/help/zh/doc-detail/67710.htm)|
|查询域名任务的详情历史列表|[QueryTaskDetailHistory](https://www.alibabacloud.com/help/zh/doc-detail/67708.htm)|
|查询已经执行完成的任务详情列表|[PollTaskResult](https://www.alibabacloud.com/help/zh/doc-detail/69361.htm)|
|域名信息修改操作 \(DomainInfoModification\)|提交域名信息修改任务|[SaveSingleTaskForUpdatingContactInfo](https://www.alibabacloud.com/help/zh/doc-detail/69378.htm)|
|批量提交域名域名信息修改任务|[SaveBatchTaskForModifyingDomainDns](https://www.alibabacloud.com/help/zh/doc-detail/67722.htm)|
|提交批量通过新联系人信息域名信息修改任务|[SaveBatchTaskForUpdatingContactInfoByNewContact](https://www.alibabacloud.com/help/zh/doc-detail/67721.htm)|
|提交删除dnshost任务|SaveSingleTaskForDeletingDnsHost|
|邮箱验证查询 \(QueryEmailVerification\)|邮箱验证查询|[ListEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67711.htm)|
|邮箱验证操作 \(EmailVerificationOperation\)|删除邮箱验证|[DeleteEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67716.htm)|
|验证邮箱 Token|[VerifyEmail](https://www.alibabacloud.com/help/zh/doc-detail/67732.htm)|
|重新发送验证邮件|[ResendEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67734.htm)|
|发送邮箱验证列表|[SubmitEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67715.htm)|
|域名转入查询 \(QueryDomainTransferIn\)|校验域名是否可以转入|[CheckTransferInFeasibility](https://www.alibabacloud.com/help/zh/doc-detail/69382.htm)|
|根据实例编号查询域名转入信息|[QueryTransferInByInstanceId](https://www.alibabacloud.com/help/zh/doc-detail/69365.htm)|
|查询域名转入列表|[QueryTransferInList](https://www.alibabacloud.com/help/zh/doc-detail/69364.htm)|
|域名转入验证邮件 \(TransferInCheckMailToken\)|域名转入验证邮件|[TransferInCheckMailToken](https://www.alibabacloud.com/help/zh/doc-detail/69383.htm)|
|域名转入操作 \(DomainTransferInOperation\)|域名转入重新输入转移密码|[TransferInReenterTransferAuthorizationCode](https://www.alibabacloud.com/help/zh/doc-detail/69385.htm)|
|域名转入重新抓取 whois 邮箱|[TransferInRefetchWhoisEmail](https://www.alibabacloud.com/help/zh/doc-detail/69386.htm)|
|域名转入重新发送验证邮件|[TransferInResendMailToken](https://www.alibabacloud.com/help/zh/doc-detail/69384.htm)|
|提交取消域名转入任务|[SaveSingleTaskForCancelingTransferIn](https://www.alibabacloud.com/help/zh/doc-detail/69374.htm)|
|域名转出查询 \(QueryDomainTransferOut\)|查询域名转出信息|[QueryTransferOutInfo](https://www.alibabacloud.com/help/zh/doc-detail/69363.htm)|
|域名转出操作 \(DomainTransferOutOperation\)|提交取消域名转出任务|[SaveSingleTaskForCancelingTransferOut](https://www.alibabacloud.com/help/zh/doc-detail/69373.htm)|
|提交获取域名转移密码任务|[SaveSingleTaskForQueryingTransferAuthorizationCode](https://www.alibabacloud.com/help/zh/doc-detail/69368.htm)|
|域名 DNSHost 修改 \(DnsHostModification\)|提交创建 DNSHost 任务|[SaveSingleTaskForCreatingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69367.htm)|
|提交修改 DNSHost 任务|[SaveSingleTaskForModifyingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69376.htm)|
|提交同步 DNSHost 任务|[SaveSingleTaskForSynchronizingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69375.htm)|
|域名 DNSHost 查询 \(DnsHostQuery\)|查询域名 DNSHost|[QueryDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69360.htm)|
|域名 DNS 设置 \(DnsModification\)|提交批量修改域名 DNS 任务|[SaveBatchTaskForModifyingDomainDns](https://www.alibabacloud.com/help/zh/doc-detail/67722.htm)|
|安全设置 \(SecuritySetting\)|提交禁止转移锁任务|[SaveSingleTaskForTransferProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/69370.htm)|
|提交批量禁止转移锁任务|[SaveBatchTaskForTransferProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/67718.htm)|
|提交禁止更新锁任务|[SaveSingleTaskForUpdateProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/69369.htm)|
|提交批量禁止更新锁任务|[SaveBatchTaskForUpdateProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/67717.htm)|
|信息模板操作 \(RegistrantProfileOperation\)|创建或者保存域名信息模板|[SaveRegistrantProfile](https://www.alibabacloud.com/help/zh/doc-detail/67700.htm)|
|删除指定的域名信息模板|[DeleteRegistrantProfile](https://www.alibabacloud.com/help/zh/doc-detail/67702.htm)|
|信息模板查询 \(QueryRegistrantProfile\)|查询自己账户下的域名信息模板|[QueryRegistrantProfiles](https://www.alibabacloud.com/help/zh/doc-detail/67701.htm)|
|任务确认 \(AcknowledgeTaskResult\)|确认任务详情结果|[AcknowledgeTaskResult](https://www.alibabacloud.com/help/zh/doc-detail/69366.htm)|

