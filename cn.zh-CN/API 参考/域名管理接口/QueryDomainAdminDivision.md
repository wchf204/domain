# QueryDomainAdminDivision {#reference_x4y_sln_xgb .reference}

通过QueryDomainAdminDivision接口：查询中国行政区划。

## 描述 {#section_zvs_5ln_xgb .section}

查询中国行政区划。

## 请求参数 {#section_ycw_xln_xgb .section}

公共请求参数，详见[公共参数](cn.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必需|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryDomainAdminDivision。|
|Lang|String|否|接口返回错误信息语言，枚举值范围： -   zh：中文
-   en：英文
-   默认为en。

 |

## 返回参数 {#section_ugp_bnn_xgb .section}

|名称|类型|描述|
|--|--|--|
|RequestId|String|唯一请求识别码。|
|AdminDivision|AdminDivisionType|行政区划。|

## 错误码 {#section_zd5_zjg_h2b .section}

|错误代码|描述|HTTP状态码|语义|
|----|--|-------|--|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络IO异常。|

## 示例 {#section_rll_vnn_xgb .section}

**请求示例**

``` {#codeblock_m06_kjo_8bf}
http://domain.aliyuncs.com/?Action=QueryDomainAdminDivision
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_b31_fmh_wv4}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryDomainAdminDivisionResponse>
    <adminDivisions></adminDivisions>
    <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
    </SQueryDomainAdminDivisionResponse>
    ```

-   JSON示例

    ``` {#codeblock_zj6_a4h_z0u}
    {
    "requestId": "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
    "adminDivisions"[]
    }
    ```


