# Domain actions that can be authorized {#concept_tsh_vjc_n2b .concept}

This document describes the domain actions that can be authorized.

Authorized resources can carry out the following domain actions through RAM.

|Authentication action|Description|API|
|:--------------------|:----------|:--|
|Query common domain name information \(QueryCommonInfo\)|Query the domain name list under the current account.|[QueryDomainList](https://www.alibabacloud.com/help/zh/doc-detail/67712.htm)|
|Query a domain name under the current account.|[QueryDomainByInstanceId](https://www.alibabacloud.com/help/zh/doc-detail/67714.htm)|
|Query the contact information of a domain name.|[QueryContactInfo](https://www.alibabacloud.com/help/zh/doc-detail/67706.htm)|
|Verify the contact information.|[VerifyContactField](https://www.alibabacloud.com/help/zh/doc-detail/69381.htm)|
|Query domain name logs \(QueryChangeLog\)|Queries operation logs.|[QueryChangeLogList](https://www.alibabacloud.com/help/zh/doc-detail/67705.htm)|
|Query domain name task \(QueryDomainTask\)|Query the domain name task list.|[QueryTaskList](https://www.alibabacloud.com/help/zh/doc-detail/67709.htm)|
|Query the task history list of a domain name task.|[QueryTaskInfoHistory](https://www.alibabacloud.com/help/zh/doc-detail/67707.htm)|
|Query the detail list of a domain name task.|[QueryTaskDetailList](https://www.alibabacloud.com/help/zh/doc-detail/67710.htm)|
|Query the detail history list of a domain name task.|[QueryTaskDetailHistory](https://www.alibabacloud.com/help/zh/doc-detail/67708.htm)|
|Query the task detail list of completed domain name tasks.|[PollTaskResult](https://www.alibabacloud.com/help/zh/doc-detail/69361.htm)|
|Modify domain name information \(DomainInfoModification\)|Submit a single task for modifying domain name information.|[SaveSingleTaskForUpdatingContactInfo](https://www.alibabacloud.com/help/zh/doc-detail/69378.htm)|
|Submit a batch task for modifying domain name information.|[SaveBatchTaskForModifyingDomainDns](https://www.alibabacloud.com/help/zh/doc-detail/67722.htm)|
|Submit a batch task for modifying domain name information by new registrant.|[SaveBatchTaskForUpdatingContactInfoByNewContact](https://www.alibabacloud.com/help/zh/doc-detail/67721.htm)|
|Submit a single task for deleting a DNSHost.|SaveSingleTaskForDeletingDnsHost|
|Query email token \(QueryEmailVerification\)|Query email token|[ListEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67711.htm)|
|Operations related to email token \(EmailVerificationOperation\)|Verify an email token.|[DeleteEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67716.htm)|
|Verify an email token.|[VerifyEmail](https://www.alibabacloud.com/help/zh/doc-detail/67732.htm)|
|Re-send an email token.|[ResendEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67734.htm)|
|Send the list of email tokens.|[SubmitEmailVerification](https://www.alibabacloud.com/help/zh/doc-detail/67715.htm)|
|Query the information related to transferring in a domain name \(QueryDomainTransferIn\)|Check if it is permitted to transfer in a domain name .|[CheckTransferInFeasibility](https://www.alibabacloud.com/help/zh/doc-detail/69382.htm)|
|Query the information related to transferring in a domain name by instance Id.|[QueryTransferInByInstanceId](https://www.alibabacloud.com/help/zh/doc-detail/69365.htm)|
|Query the list of domain names transferred in.|[QueryTransferInList](https://www.alibabacloud.com/help/zh/doc-detail/69364.htm)|
|Email token for transferring in a domain name \(TransferInCheckMailToken\)|Email token for transferring in a domain name.|[TransferInCheckMailToken](https://www.alibabacloud.com/help/zh/doc-detail/69383.htm)|
|Transfer in a domain name \(DomainTransferInOperation\)|Re-enter the authorization code for transferring in a domain name.|[TransferInReenterTransferAuthorizationCod](https://www.alibabacloud.com/help/zh/doc-detail/69385.htm)|
|Re-fetch the WHOIS email for transferring in a domain name.|[TransferInRefetchWhoisEmail](https://www.alibabacloud.com/help/zh/doc-detail/69386.htm)|
|Re-send the email token for transferring in a domain name.|[TransferInResendMailToken](https://www.alibabacloud.com/help/zh/doc-detail/69384.htm)|
|Cancel a single task for transferring in a domain name.|[SaveSingleTaskForCancelingTransferIn](https://www.alibabacloud.com/help/zh/doc-detail/69374.htm)|
|Query the information related to transferring out a domain name \(QueryDomainTransferOut\)|Query the information related to transferring out a domain name.|[QueryTransferOutInfo](https://www.alibabacloud.com/help/zh/doc-detail/69363.htm)|
|Transfer out a domain name \(DomainTransferOutOperation\).|Cancel a single task for transferring out a domain name.|[SaveSingleTaskForCancelingTransferOut](https://www.alibabacloud.com/help/zh/doc-detail/69373.htm)|
|Submit a single task for querying transfer authorization code.|[SaveSingleTaskForQueryingTransferAuthorizationCode](https://www.alibabacloud.com/help/zh/doc-detail/69368.htm)|
|Modify the DNSHost of a domain name \(DnsHostModification\)|Submit a single task for creating a DNSHost.|[SaveSingleTaskForCreatingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69367.htm)|
|Submit a single task for modifying a DNSHost.|[SaveSingleTaskForModifyingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69376.htm)|
|Submit a single task for synchronizing a DNSHost.|[SaveSingleTaskForSynchronizingDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69375.htm)|
|Query the DNSHost of a domain name \(DnsHostQuery\)|Query the DNSHost of a domain name|[QueryDnsHost](https://www.alibabacloud.com/help/zh/doc-detail/69360.htm)|
|Domain name DNS settings \(DnsModification\)|Submit a batch task for modifying DNS.|[SaveBatchTaskForModifyingDomainDns](https://www.alibabacloud.com/help/zh/doc-detail/67722.htm)|
|Security settings \(SecuritySetting\)|Submit a single task for transfer prohibition lock.|[SaveSingleTaskForTransferProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/69370.htm)|
|Submit batch task for transfer prohibition locks.|[SaveBatchTaskForTransferProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/67718.htm)|
|Submit a single task for update prohibition lock.|[SaveSingleTaskForUpdateProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/69369.htm)|
|Submit batch task for update prohibition locks.|[SaveBatchTaskForUpdateProhibitionLock](https://www.alibabacloud.com/help/zh/doc-detail/67717.htm)|
|Operations related to registrant profile \(RegistrantProfileOperation\)|Create or save registrant profile of a domain name.|[SaveRegistrantProfile](https://www.alibabacloud.com/help/zh/doc-detail/67700.htm)|
|Create or save the specified registrant profile of a domain name.|[DeleteRegistrantProfile](https://www.alibabacloud.com/help/zh/doc-detail/67702.htm)|
|Query registrant profile \(QueryRegistrantProfile\).|Query registrant profile in your account.|[QueryRegistrantProfiles](https://www.alibabacloud.com/help/zh/doc-detail/67701.htm)|
| Acknowledge task result \(AcknowledgeTaskResult\)|Acknowledge task result.|[AcknowledgeTaskResult](https://www.alibabacloud.com/help/zh/doc-detail/69366.htm)|

