# 访问控制 RAM {#concept_nyw_3vd_n2b .concept}

本文档介绍访问控制 RAM。

如果您的账户下有多个域名，且有多个用户需要管理这些域名，在这些用户共享使用您的云账号密钥时，就会存在以下问题：

-   您的密钥由多人共享，泄密风险高；
-   您无法限制用户的访问权限，容易出现误操作引发安全风险。

访问控制 RAM 是阿里云提供的资源访问控制服务。通过 RAM，您可以集中管理您的用户（比如员工、系统或应用程序），还可以管理用户权限，控制用户访问您名下的指定资源。

访问控制 RAM 可以帮助您管理用户权限，控制用户访问指定的资源。例如，为了加强安全控制，您可以给某个群组附加一个授权策略，下面列举几种常用的授权策略：

-   AliyunDomainFullAccess 管理域名 \(Domain\) 的权限。该权限允许授权的子账号管理主账号下的域名资源，属于最大权限。

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

-   管理某个域名 \(example.com\) 的权限。该权限允许授权的子账号针对某一个域名进行域名资源管理。

    ```
    {
      "Version": "1",
      "Statement": [
        {
          "Action": [
          "domain:DomainInfoModification",
          "domain:DomainTransferInOperation",
          "domain:DnsModification",
          "domain:SecuritySetting",
          ]
          "Resource": "acs:domain:*:*:domain/example.com",
          "Effect": "Allow"
        },
        {
          "Action":
          "domain:QueryCommonInfo",
          "Resource": "acs:domain:*:*:*",
          "Effect": "Allow"
        }
      ]
    }
    ```

-   AliyunDomainReadOnlyAccess 只读访问域名的权限。该权限允许授权的子账号查看主账号下的域名资源，但不允许其进行管理。

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


更多关于访问控制 RAM 的介绍，请参考 [RAM 产品文档](https://www.alibabacloud.com/help/zh/product/28625.htm)。

