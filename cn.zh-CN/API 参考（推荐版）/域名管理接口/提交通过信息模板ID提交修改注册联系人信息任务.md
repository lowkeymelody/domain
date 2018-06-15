# 提交通过信息模板ID提交修改注册联系人信息任务 {#concept_dqp_t4r_b2b .concept}

通过信息模板ID提交修改注册联系人信息任务，任务执行结果请通过[QueryTaskDetailList](cn.zh-CN/API 参考（推荐版）/域名管理接口/查询任务详情.md#)接口来查询。修改后注册联系人信息和模板信息一致，如果域名是强制实名认证域名，修改成功后域名会变为实名认证成功状态。

## 请求参数 {#section_emv_dpr_b2b .section}

公共请求参数，详见[公共参数](cn.zh-CN/API 参考（推荐版）/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID。|
|DomainName|[DomainListType](#table_bfl_hpr_b2b)|是|域名列表。|
|RegistrantProfileId|Long|是|信息模板ID。|
|TransferOutProhibited|Boolean|可选|是否添加禁止转出限制，表示所有者修改后是否限制域名60天转出。不传此参数默认不限制。|

|名称|类型|描述|
|:-|:-|:-|
|DomainName|String|域名|

## 返回参数 {#section_klx_qpr_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_elz_xpr_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|contactTemplateRealNamedNotExist|The Registrant Profile completed Real-name verification does not exist.|400|域名不存在。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_ks1_fqr_b2b .section}

**请求示例**

```
http://domain.aliyuncs.com/?Action=SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID
&ContactTemplateId=1
&DomainName.1=test.com
&RegistrantProfileId=1
&AddTransferProhibitionLock=true
&<公共请求参数>
```

**返回示例**

-   XML示例

    ```
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveTaskForUpdatingRegistrantInfoByRegistrantProfileIDResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveTaskForUpdatingRegistrantInfoByRegistrantProfileIDResponse>
    ```

-   JSON示例

    ```
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


