# Resource Access Management {#concept_nyw_3vd_n2b .concept}

This document introduces Resource Access Management \(RAM\).

If you have more than one domain name under your account, and more than one user needs to manage those domain names, the following problems exist when these users share your account key:

-   The shared key has a high risk of leakage.
-   You are prone to security risks caused by misoperations because you cannot control other users’ access permissions.

RAM is a resource access control service provided by Alibaba Cloud. You can manage your users with RAM, such as employees, systems, or applications, and you can also manage user permissions to control user access to specified resources in your account.

RAM can help you manage user permissions and control user access to specified resources. For example, you can apply one of the following authorization policies to a group to enhance security control:

-   Aliyundomainfullaccess - Permission for managing domain names. This is the highest-level permission. The authorized sub-account is permitted to manage the domain name resources under the master account.

    ```
    {
      "Statement": [
        {
     "Action": "domain:*",
     "Effect": "Allow",
     "Resource": "*"
        }
      ],
      "Version": "1"
    }
    ```

-   Permission for managing a specific domain name. The authorized sub-account is permitted to manage the resources of a specific domain name.

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

-   AliyunDomainReadOnlyAccess - Permission for accessing domain names in a read-only state. The authorized sub-account is permitted to view but not manage the domain name resources under the master account.

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


For more information about RAM, see [RAM product documentation](https://www.alibabacloud.com/help/zh/product/28625.htm).

