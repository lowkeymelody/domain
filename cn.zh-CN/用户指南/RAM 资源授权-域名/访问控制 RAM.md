# 访问控制 RAM {#concept_nyw_3vd_n2b .concept}

本文档介绍访问控制 RAM。

如果您账户下有多个域名，您的企业里有多个用户需要管理这些域名。如果这些用户共享使用您的云账号密钥，那么存在以下问题：

-   您的密钥由多人共享，泄密风险高；
-   您无法限制用户的访问权限，容易出现误操作导致安全风险。

访问控制 RAM \(Resource Access Management\) 是阿里云提供的资源访问控制服务。通过 RAM，您可以集中管理您的用户（比如员工、系统或应用程序），以及控制用户可以访问您名下哪些资源的权限。

访问控制 RAM 将帮助您管理用户对资源的访问权限控制。例如，为了加强安全控制，您可以给某个群组附加一个授权策略，下面列举几个常用的授权策略：

-   AliyunDomainFullAccess 管理域名 \(Domain\) 的权限，该权限允许授权的子账号管理主账号下的域名资源，属于最大权限。

    ```
    {
      "Statement": [
        {
          "Action": "domain:*",
          "Effect": "Allow",
          "Resource": "*"
        }
      ],
      "Version": "1"
    }
    ```

-   对子账号某个域名 \(example.com\) 授权，该权限允许授权子账号针对某一个域名进行域名资源管理。

    ```
    {
      "Version": "1",
      "Statement": [
        {
          "Action": [
          " domain: DomainInfoModification ",
          " domain: DomainTransferInOperation",
          " domain:DnsModification ",
          " domain:SecuritySetting ",
          ]
          "Resource": "acs:domain:*:*:domain/example.com",
          "Effect": "Allow"
        },
        {
          "Action":
          " domain: QueryCommonInfo ",
          "Resource": "acs: domain:*:*:*",
          "Effect": "Allow"
        }
      ]
    }
    ```

-   AliyunDomainReadOnlyAccess 只读访问域名的权限，该权限允许授权子账号查看主账号下的域名资源，但不允许其进行管理。

    ```
    {
       "Version": "1",
       "Statement": [
         {
           "Action": [
             "domain:Query*",
           ],
           "Resource": "acs:domain:*:*:domain/*",
           "Effect": "Allow"
         }
        ]
    }
    ```


更多关于访问控制 RAM的介绍，请参考 [RAM 产品文档](https://help.aliyun.com/document_detail/28627.html)。

