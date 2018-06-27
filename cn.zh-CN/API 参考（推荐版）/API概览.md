# API概览 {#concept_xt1_n2b_b2b .concept}

支持域名购买、续费以及管理操作（包括信息修改、DNS修改、创建DNS、信息模板的管理等），以及域名列表和域名信息的查询。

## 域名管理接口 {#section_z25_r2b_b2b .section}

|API|描述|
|:--|:-|
|[QueryDomainList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名列表.md#)|查询自己账户下域名列表|
|[QueryDomainByInstanceId](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名信息.md#)|查询自己账户下域名信息|
|[QueryContactInfo](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询联系人信息.md#)|查询域名联系人信息|
|[QueryChangeLogList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询操作日志.md#)|查询操作日志|
|[DeleteEmailVerification](cn.zh-CN/API 参考（推荐版）/域名管理接口/删除邮箱验证.md#)|删除邮箱验证|
|[VerifyEmail](cn.zh-CN/API 参考（推荐版）/域名管理接口/验证邮箱Token.md#)|验证邮箱|
|[ListEmailVerification](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询邮箱验证列表.md#)|查询邮箱验证列表|
|[ResendEmailVerification](cn.zh-CN/API 参考（推荐版）/域名管理接口/重新发送验证邮件.md#)|重新发送验证邮件|
|[SubmitEmailVerification](cn.zh-CN/API 参考（推荐版）/域名管理接口/发送邮件验证邮件.md#)|发送邮箱验证列表|
|[SaveSingleTaskForCreatingOrderActivate](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名注册任务.md#)|提交域名注册任务|
|[SaveSingleTaskForCreatingOrderRenew](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名续费任务.md#)|提交域名续费任务|
|[SaveBatchTaskForModifyingDomainDns](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量修改域名DNS任务.md#)|提交批量修改域名dns任务|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量通过新联系人信息域名信息修改任务.md#)|提交批量通过联系人信息和资料修改注册联系人信息任务|
|[SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量通过模板域名信息修改任务.md#)|提交批量通过模板域名信息修改任务|
|[SaveBatchTaskForCreatingOrderActivate](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量域名注册任务.md#)|提交批量域名注册任务|
|[SaveBatchTaskForCreatingOrderRenew](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量域名续费任务.md#)|提交批量域名续费任务|
|[SaveBatchTaskForDomainNameProxyService](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量域名隐私保护服务任务.md#)|提交批量域名隐私保护服务任务|
|[SaveBatchTaskForUpdateProhibitionLock](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量禁止更新锁任务.md#)|提交批量禁止更新锁任务|
|[SaveBatchTaskForTransferProhibitionLock](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量禁止转移锁任务.md#)|提交批量禁止转移锁任务|
|[QueryTaskList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务列表.md#)|查询域名任务列表|
|[QueryTaskInfoHistory](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务历史列表.md#)|查询域名任务历史列表|
|[QueryTaskDetailList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务详情.md#)|查询域名任务的详情列表|
|[QueryTaskDetailHistory](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务历史详情.md#)|查询域名任务的详情历史列表|
|[SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID](cn.zh-CN/API 参考（推荐版）/域名管理接口/通过信息模板ID提交域名实名认证任务.md#)|通过信息模板ID提交域名实名认证任务|
|[SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名实名认证任务.md#)|提交域名实名认证任务|
|[SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交通过信息模板ID提交修改注册联系人信息任务.md#)|提交通过信息模板ID修改注册联系人信息任务|
|[SaveTaskForUpdatingRegistrantInfoByIdentityCredential](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量通过联系人信息和资料修改注册联系人信息任务.md#)|提交批量通过联系人信息和资料修改注册联系人信息任务|
|[QueryFailReasonForDomainRealNameVerification](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名实名认证失败原因.md#)|查询域名实名认证失败原因|
|[CheckDomain](cn.zh-CN/API 参考（推荐版）/域名管理接口/域名Check接口.md#)|检查域名是否可以注册接口|
|[AcknowledgeTaskResult](cn.zh-CN/API 参考（推荐版）/域名管理接口/确认任务详情结果.md#)|确认任务详情结果|
|[CheckTransferInFeasibility](cn.zh-CN/API 参考（推荐版）/域名管理接口/校验域名是否可以转入.md#)|校验域名是否可以转入|
|[PollTaskResult](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询已经执行完成的任务详情列表.md#)|查询已经执行完成的任务详情列表|
|[QueryDomainGroupList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名分组列表.md#)|查询域名分组列表|
|[QueryTransferInByInstanceId](cn.zh-CN/API 参考（推荐版）/域名管理接口/根据实例编号查询域名转入信息.md#)|根据实例编号查询域名转入信息|
|[QueryTransferInList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名转入列表.md#)|查询域名转入列表|
|[QueryTransferOutInfo](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名转出信息.md#)|查询域名转出信息|
|[SaveBatchTaskForCreatingOrderTransfer](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量域名转入任务.md#)|提交批量域名转入任务|
|[SaveSingleTaskForCreatingOrderTransfer](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名转入任务.md#)|提交域名转入任务|
|[SaveSingleTaskForCancelingTransferIn](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交取消域名转入任务.md#)|提交取消域名转入任务|
|[SaveSingleTaskForCancelingTransferOut](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交取消域名转出任务.md#)|提交取消域名转出任务|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交获取域名转移密码任务.md#)|提交获取域名转移密码任务|
|[TransferInCheckMailToken](cn.zh-CN/API 参考（推荐版）/域名管理接口/域名转入验证邮件.md#)|域名转入验证邮件|
|[TransferInReenterTransferAuthorizationCode](cn.zh-CN/API 参考（推荐版）/域名管理接口/域名转入重新输入转移密码.md#)|域名转入重新输入转移密码|
|[TransferInRefetchWhoisEmail](cn.zh-CN/API 参考（推荐版）/域名管理接口/域名转入重新抓取whois邮箱.md#)|域名转入重新抓取whois邮箱|
|[TransferInResendMailToken](cn.zh-CN/API 参考（推荐版）/域名管理接口/域名转入重新发送验证邮件.md#)|域名转入重新发送验证邮件|
|[VerifyContactField](cn.zh-CN/API 参考（推荐版）/域名管理接口/校验联系人信息.md#)|校验联系人信息|
|[SaveSingleTaskForCreatingOrderRedeem](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名赎回任务.md#)|提交域名赎回任务|
|[SaveBatchTaskForCreatingOrderRedeem](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交批量域名赎回任务.md#)|提交批量域名赎回任务|
|[SaveSingleTaskForCreatingDnsHost](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交创建dnshost任务.md#)|提交创建dnshost任务|
|[SaveSingleTaskForDomainNameProxyService](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名隐私保护服务任务.md#)|提交域名隐私保护服务任务|
|[SaveSingleTaskForModifyingDnsHost](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交修改dnshost任务.md#)|提交修改dnshost任务|
|[SaveSingleTaskForSynchronizingDnsHost](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交同步dnshost任务.md#)|提交同步dnshost任务|
|[SaveSingleTaskForTransferProhibitionLock](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交禁止转移锁任务.md#)|提交禁止转移锁任务|
|[SaveSingleTaskForUpdateProhibitionLock](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交禁止更新锁任务.md#)|提交禁止更新锁任务|
|[SaveSingleTaskForUpdatingContactInfo](cn.zh-CN/API 参考（推荐版）/域名管理接口/提交域名信息修改任务.md#)|提交域名域名信息修改任务|
|[QueryDnsHost](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询域名DnsHost.md#)|查询域名dnshost|
|[DeleteDomainGroup](cn.zh-CN/API 参考（推荐版）/域名管理接口/删除域名分组.md#)|删除域名分组|
|[SaveDomainGroup](cn.zh-CN/API 参考（推荐版）/域名管理接口/保存域名分组.md#)|保存域名分组|
|[UpdateDomainToDomainGroup](cn.zh-CN/API 参考（推荐版）/域名管理接口/向分组中设置域名.md#)|向分组中设置域名|
|[SaveBatchDomainRemark](cn.zh-CN/API 参考（推荐版）/域名管理接口/批量保存域名备注.md#)|批量保存域名备注信息|
|[QueryDomainSuffix](cn.zh-CN/API 参考（推荐版）/域名管理接口/高级搜索后缀列表.md#)|高级搜索自己账户下后缀列表|
|[QueryAdvancedDomainList](cn.zh-CN/API 参考（推荐版）/域名管理接口/高级搜索域名列表.md#)|高级搜索自己账号下域名列表|

## 信息模板接口 {#section_zdt_d3b_b2b .section}

|API|描述|
|:--|:-|
|[SaveRegistrantProfile](cn.zh-CN/API 参考（推荐版）/信息模板接口/保存信息模板.md#)|创建或者保存域名信息模板|
|[QueryRegistrantProfiles](cn.zh-CN/API 参考（推荐版）/信息模板接口/查询信息模板.md#)|查询自己账户下的域名信息模板|
|[DeleteRegistrantProfile](cn.zh-CN/API 参考（推荐版）/信息模板接口/删除信息模板.md#)|删除指定的域名信息模板|
|[RegistrantProfileRealNameVerification](cn.zh-CN/API 参考（推荐版）/信息模板接口/提交信息模板实名认证.md#)|提交信息模板实名认证|
|[QueryFailReasonForRegistrantProfileRealNameVerification](cn.zh-CN/API 参考（推荐版）/信息模板接口/查询模板实名认证失败原因.md#)|查询模板实名认证失败原因|
|[QueryRegistrantProfileRealNameVerificationInfo](cn.zh-CN/API 参考（推荐版）/信息模板接口/查询信息模板实名认证资料.md#)|查询域名信息模板实名认证资料|

