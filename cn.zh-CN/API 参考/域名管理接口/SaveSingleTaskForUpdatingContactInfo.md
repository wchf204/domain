# SaveSingleTaskForUpdatingContactInfo {#concept_enl_j5r_b2b .concept}

SaveSingleTaskForUpdatingContactInfo：提交域名信息修改任务。任务执行结果请通过[查询任务详情列表](intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md#)接口来查询。

## 请求参数 {#section_fd3_gvr_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveSingleTaskForUpdatingContactInfo。|
|InstanceId|String|可选|域名实例编号。|
|DomainName|String|是|域名。|
|RegistrantProfileId|Long|是|信息模板编号。|
|ContactType|String|是|联系人类型，枚举值范围：registrant、admin、billing、tech。|
|AddTransferLock|Boolean|可选|是否添加禁止转出限制，此参数只对 ContactType=registrant 情况下起作用，表示持有者修改后是否限制域名60天转出。默认为false，不限制转出。|
|Lang|String|否|接口返回错误信息语言，枚举值范围：zh 中文，en 英文。默认为en。|

## 返回参数 {#section_kx5_nvr_b2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|TaskNo|String|任务编号。|

## 错误码 {#section_hdm_rvr_b2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|
|DomainNotExist|The domain name does not exist.|400|域名不存在。|
|TaskIsBeingProcessed|An operation is being processed. Please try again later.|400|该域名存在正在处理中的操作，请稍后再试。|

## 示例 {#section_evc_wvr_b2b .section}

**请求示例**

``` {#codeblock_fsh_wkp_a9e}
http://domain-intl.aliyuncs.com/?Action=SaveSingleTaskForUpdatingContactInfo
&RegistrantProfileId=1
&DomainName=test.com
&ContactType=registrant
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_uc9_h0p_fth}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveSingleTaskForUpdatingContactInfoResponse>
        <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
        <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
    </SaveSingleTaskForUpdatingContactInfoResponse>
    ```

-   JSON示例

    ``` {#codeblock_3f4_zow_ao9}
    {    
      "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
      "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
    }
    ```


