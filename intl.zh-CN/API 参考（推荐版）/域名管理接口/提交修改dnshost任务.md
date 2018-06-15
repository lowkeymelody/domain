# 提交修改dnshost任务 {#concept_n21_gcs_b2b .concept}

提交修改dnshost任务。任务执行结果请通过[查询任务详情列表](intl.zh-CN/API 参考（推荐版）/域名管理接口/查询任务详情.md#)接口来查询。

## 请求参数 {#section_vvk_mcs_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveSingleTaskForModifyingDnsHost。|
|InstanceId|String|是|域名实例编号，可通过查询域名列表接口（[QueryDomainList](intl.zh-CN/API 参考（推荐版）/域名管理接口/查询域名列表.md#)）获得。|
|DnsName|String|是|例如：dns1。|
|Ips|[IpListType](#table_z22_bb4_c2b)|是|IP地址列表。|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文，en 英文。默认为en。|

|名称|类型|描述|
|:-|:-|:-|
|ip|String|ip地址|

## 返回参数 {#section_iw4_scs_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_hxt_wcs_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_nf4_1ds_b2b .section}

**请求示例**

```
http://domain-intl.aliyuncs.com/
?Action=SaveSingleTaskForModifyingDnsHost
&DnsName=ns3
&Ip.2=185.27.134.201
&Ip.1=218.83.159.236
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveSingleTaskForModifyingDnsHostResponse>
    <TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
    <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
    </SaveSingleTaskForModifyingDnsHostResponse>
    ```

-   JSON示例

    ```
    {
      "requestId": "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
      "taskNo": "e9b8e8b4-7334-4548-9cec-c30b6891f292"
    }
    ```


