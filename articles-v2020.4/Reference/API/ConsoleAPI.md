# 云扩控制台API文档<span id="云扩控制台API文档"><span>

最低支持版本：V4.1.78728

更新日期：2022-07-28


## 文档概述<span id="文档概述"><span>

本文档描述了控制台产品对外提供的API接口的详细描述，包括接口用途、请求格式、返回格式和请求实例等。
  
Open API：https://api.encoo.com/openapi/static/consoleapi.html

## 面向对象<span id="面向对象"><span>

本文档主要面向以下对象：

● 二次开发工程师

## 调用方式<span id="调用方式"><span>

### 构造请求<span id="构造请求"><span>

#### 服务端点<span id="服务端点"><span>

本文档主要涉及ApiGateway和SSO两个服务端点。ApiGateway为后台接口提供统一的调用入口，SSO负责提供统一的认证鉴权服务。对于需要认证的接口，均需要在Authorization请求头中带上SSO签发的token信息，格式为Authorization: Bearer &lt;token&gt;。

说明：
Bearer和&lt;token&gt;之间需留一个空格。

● SaaS服务端点：
  > SSO: auth.encoo.com
  ApiGateway:api.encoo.com

● 私有化服务端点：
默认情况下，非https部署，SSO端口为81，ApiGateway端口为8080。 https部署情况下，为对应域名
  >SSO:控制台IP:81或SSO域名
  ApiGateway:控制台IP:8080或ApiGateway域名

#### 请求URI<span id="请求URI"><span>

请求URI由如下部分组成。
{URI-scheme}:</span>//{Endpoint}/{resource-path}?{query-string}
尽管请求URI包含在请求消息头中，但大多数语言或框架都要求您从请求消息中单独传递它，所以在此单独强调。

<table>
<tr><td>参数</td><td> 描述</td></tr>
<tr><td>URI-scheme</td><td> 表示用于传输请求的协议，当前API接口采用HTTPS协议或HTTP协议。</td></tr>
<tr><td>Endpoint</td><td> 指定承载API服务的服务器域名或IP地址加端口号，即调用API服务的接入地址。</td></tr>
<tr><td>resource-path</td><td> 资源路径，也即API的请求路径。从具体API的URI模块获取。</td></tr>
<tr><td>query-string</td><td> 公共请求参数，请求参数前面需要携带“?”，形式为“参数名=参数取值”，例如“AccessKey=d0742694e5784074af7b2c5ecff21455”，参数之间由“&”连接。</td></tr>
</table>

#### 请求方法<span id="请求方法"><span>

<table>
<tr><td>方法</td><td>说明</td></tr>
<tr><td>GET</td><td> 请求服务器返回指定资源。</td></tr>
<tr><td>PUT</td><td> 请求服务器更新指定资源。</td></tr>
<tr><td>POST</td><td> 请求服务器新增资源或执行特殊操作。</td></tr>
<tr><td>DELETE</td><td> 请求服务器删除指定资源，如删除对象等。</td></tr>
<tr><td>HEAD</td><td> 请求服务器资源头部。</td></tr>
<tr><td>PATCH</td><td> 请求服务器更新资源的部分内容。</td></tr>
</table>

#### 请求消息头<span id="请求消息头"><span>

**公共请求消息头是所有API请求都必需的参数。为减少内容重复，公共请求将不在各API详情中列出。**
<table>
<tr><td>名称</td><td>描述</td><td>示例</td></tr>
<tr><td>Content-type</td><td> 指定请求消息体中的MIME类型</td><td> application/json。<b>本系中若未特殊说明通常为application/json</b>,上传文件时通常为application/octet-stream</td></tr>
<tr><td><del>Content-Length</del></td><td> 指定请求消息体的长度</td><td> 3456。<b>通常可省略</b>，因为HttpClient，PostMan等会自动添加</td></tr>
<tr><td>Authorization</td><td> 指定用户的认证令牌token</td><td> Bearer eyJhbGciOiJSUzI1Ni…(后略)即Bearer 拼接通过端口获取到的3.2.2获取到的令牌</td></tr>
<tr><td>CompanyId</td><td> 需要调用接口获取的信息所在公司Id</td><td> 40143948-f359-4b9f-949f-ad179bcf1397</td></tr>
<tr><td>DepartmentId</td><td> 需要调用接口获取的信息所在部门Id</td><td> 1c3464c8-6939-4b13-ba5d-45f44ed8b671</td></tr>
</table>

#### 请求消息体<span id="请求消息体"><span>

该部分可选。请求消息体通常以结构化格式（如JSON）发出，与请求消息头中Content-Type对应，传递除请求消息头之外的内容。
若请求消息体中的参数支持中文，则中文字符必须为UTF-8编码。

### 认证鉴权<span id="认证鉴权"><span>

***认证接口请求目标服务器为SSO，参见[【服务端点】](#服务端点)***


#### 获取令牌<span id="获取令牌"><span>

<!-- ##### 功能介绍
-->
获取用户访问令牌，用于接口调用。

<!-- ##### 基本信息
-->
**Path：** /connect/token

**Method：** POST

**请求参考示例：**

*注意：Header中Content-Type应设置为application/x-www-form-urlencoded
client_id、grant_type为固定值，只需替换XXXXXX对应的字段内容，即：用户名及密码*

    client_id=thirdpartyservice&grant_type=password&username=XXXXXX&password=XXXXXX

**响应参考示例：**

    {
      Access_token: "this is a string",    // 访问令牌
      Expires_in: "this is a string",    // 令牌过期时间，单位秒
      Token_type: "this is a string",    // 令牌类型
      Refresh_token: "this is a string",    // 刷新令牌
      Scope: "this is a string"    // 令牌作用域
    }

#### 刷新令牌<span id="刷新令牌"><span>

<!-- ##### 功能介绍
-->
由于访问令牌生命周期有限，当访问令牌过期时，可使用刷新令牌请求新的访问令牌

**说明：刷新令牌仅能使用一次**


<!-- ##### 基本信息
-->
**Path：** /connect/token

**Method：** POST

**请求参考示例：**

*注意：Header中Content-Type应设置为application/x-www-form-urlencoded
client_id、grant_type为固定值，只需替换XXXXXX对应的字段内容，即：前一次请求（获取令牌/刷新令牌）的返回值*

    client_id=thirdpartyservice&grant_type=refresh_token&refresh_token=XXXXXX

**响应参考示例：**

    {
      Access_token: "this is a string",    // 访问令牌
      Expires_in: "this is a string",    // 令牌过期时间，单位秒
      Token_type: "this is a string",    // 令牌类型
      Refresh_token: "this is a string",    // 刷新令牌
      Scope: "this is a string"    // 令牌作用域
    }

---


### 返回结果<span id="返回结果"><span>

#### 响应消息头<span id="响应消息头"><span>

响应消息头包含如下两部分：

● 一个HTTP状态代码，从2xx成功代码到4xx或5xx错误代码，或者可以返回服务定义的状态码。

● 附加响应头字段，如Content-Type响应消息头。
详细的公共响应消息头字段请参考下表
<table>
<tr><td>名称</td><td> 描述</td><td> 示例</td></tr>
<tr><td>Content-Length</td><td> 服务端返回的消息实体的传输长度，以字节为单位</td><td> 3456</td></tr>
<tr><td>Content-type</td><td> 消息体的MIME类型</td><td> application/json</td></tr>
</table>

#### 响应消息体<span id="响应消息体"><span>

该部分可选。响应消息体通常以结构化格式（如JSON或XML）返回，与响应消息头中Content-Type对应，传递除响应消息头之外的内容。
以下是通用HTTP状态码说明
<table>
<tr><td>HTTP状态码</td><td> 状态描述</td><td> 语义</td></tr>
<tr><td>200</td><td> OK</td><td> 请求成功</td></tr>
<tr><td>204</td><td> NoContent</td><td> 没有返回信息</td></tr>
<tr><td>400</td><td> BadRequest</td><td> 1．请求参数错误 2．因资源被引用而无法删除</td></tr>
<tr><td>404</td><td> NotFound</td><td> 资源未找到</td></tr>
<tr><td>415</td><td> Unsupported Media Type</td><td> 服务端未实现此请求方法，或要传递一个空的Json作为Body，即，”{}”</td></tr>
<tr><td>500</td><td> InternalServerError</td><td> 服务器内部异常</td></tr>
</table>

## 业务接口列表<span id="业务接口列表"><span>

**● 业务接口请求目标服务器为ApiGateway，参见[【服务端点】](#服务端点)**

**● 业务接口请求应使用[公共请求消息头](#请求消息头)，若未特殊说明Content-Type为application/json**


### 公司<span id="公司"><span>

#### 查询用户所属公司列表<span id="查询用户所属公司列表"><span>

<!-- ##### 功能介绍
-->
根据条件查询用户所属公司列表

<!-- ##### 基本信息
-->
**Path：** /openapi/companies/companylist

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>Name</td><td>String</td><td>公司名称，模糊匹配</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Companies: [
        {
          CompanyUserId: "b58e5911-52bd-473d-a98c-9960a1276a09",    // 用户id
          CompanyUserName: "this is a string",    // 用户名称
          Id: "4fa6344f-ce24-49b2-9f81-0006536b8e14",    // 唯一标识
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          Tags: ["this is a string","this is a string"],    // 标签
          Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
          CreatedAt: "2022-07-29T12:13:49.775Z",    // 创建时间
          CreatedBy: "c3048593-d4ab-44d9-aad0-128ff0f31da6",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedBy: "ef0c107a-1ea8-4132-8492-9bbb902dab92",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          ModifiedAt: "2022-07-29T12:13:49.776Z",    // 更新时间
          CompanyId: "5a56b12c-4726-48cd-8050-c6e2b58bff0b",    // 公司id
          Edition: "Enterprise"    // 版本类型:Enterprise-企业版;Community-社区版
        },
        {
          // 略，结构同前一节点
        }
      ]    // 公司列表
    }

---

### 部门<span id="部门"><span>

#### 获取当前公司部门树<span id="获取当前公司部门树"><span>

<!-- ##### 功能介绍
-->
获取公司下整个部门树形层级结构

<!-- ##### 基本信息
-->
**Path：** /openapi/departments/tree

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 35,    // 查询命中总记录数
      RootDepartment: {
        Children: [
          {
            Children: { /* 略，结构同上级节点 */ },    // 子部门列表
            DepartmentPath: "this is a string",    // 部门树路径
            VisitorHasAnyRole: false,    // 用户是否在此部门中拥有角色
            VisitorHasPermission: false,    // 用户是否在此部门中拥有权限
            UserCount: 99,    // 用户数量
            Id: "c4768455-bc87-44a6-9ebf-d73030c53381",    // 唯一标识
            DepartmentId: "04c743fa-2074-4a9a-83a1-ba703e71c3d1",    // 部门id
            ParentId: "aaeace38-b62f-4af3-a732-63929a8d4557",    // parent id
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            ETag: "this is a string",    // 版本控制标记
            Tags: ["this is a string","this is a string"],    // 标签
            Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
            CreatedAt: "2022-07-29T12:13:49.779Z",    // 创建时间
            ModifiedAt: "2022-07-29T12:13:49.779Z",    // 更新时间
            CompanyId: "bea00011-59e7-4d85-ac01-c8ce222875b4"    // 公司id
          },
          {
            // 略，结构同前一节点
          }
        ],    // 子部门列表
        DepartmentPath: "this is a string",    // 部门树路径
        VisitorHasAnyRole: false,    // 用户是否在此部门中拥有角色
        VisitorHasPermission: false,    // 用户是否在此部门中拥有权限
        UserCount: 99,    // 用户数量
        Id: "c4768455-bc87-44a6-9ebf-d73030c53381",    // 唯一标识
        DepartmentId: "04c743fa-2074-4a9a-83a1-ba703e71c3d1",    // 部门id
        ParentId: "aaeace38-b62f-4af3-a732-63929a8d4557",    // parent id
        Name: "this is a string",    // 名称
        Description: "this is a string",    // 备注
        ETag: "this is a string",    // 版本控制标记
        Tags: ["this is a string","this is a string"],    // 标签
        Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
        CreatedAt: "2022-07-29T12:13:49.779Z",    // 创建时间
        ModifiedAt: "2022-07-29T12:13:49.779Z",    // 更新时间
        CompanyId: "bea00011-59e7-4d85-ac01-c8ce222875b4"    // 公司id
      }    // 部门树根节点
    }

---

### 流程包<span id="流程包"><span>

#### 查询流程包列表<span id="查询流程包列表"><span>

<!-- ##### 功能介绍
-->
根据参数查询对应的流程包列表

<!-- ##### 基本信息
-->
**Path：** /openapi/packages

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>IncludeVersions</td><td>Boolean</td><td>是否包含所有版本</td></tr>
<tr><td>SearchString</td><td>String</td><td>关键字，模糊匹配名称、备注、标签</td></tr>
<tr><td>Name</td><td>String</td><td>名称，模糊匹配</td></tr>
<tr><td>IsDesc</td><td>Boolean</td><td>是否按创建时间降序排序，默认true,说明:true-降序；false-升序</td></tr>
<tr><td>StartTime</td><td>DateTime</td><td>开始时间，格式:"2022-07-29T12:13:49.780Z"</td></tr>
<tr><td>EndTime</td><td>DateTime</td><td>结束时间，格式:"2022-07-29T12:13:49.780Z"</td></tr>
<tr><td>PageIndex</td><td>Int</td><td>页码（从0开始）</td></tr>
<tr><td>PageSize</td><td>Int</td><td>页大小（默认20）</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 58,    // 查询命中总记录数
      List: [
        {
          Id: "ee190999-9a73-423b-9fc8-6dde2d91d9f0",    // 唯一标识
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          TotalDownloads: 64,    // 下载计数
          LastVersion: "this is a string",    // 最新版本号
          LastVersionId: "06e19272-2b7d-470e-8227-f27418517f13",    // 最高版本id
          CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
          ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
          CreatedBy: "7aa3d616-b6ea-470e-8205-e50dc886b033",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedBy: "6146fed5-e624-4e2e-8e59-8e4a94af1932",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          Tags: ["this is a string","this is a string"],    // 标签
          CompanyId: "dc120332-1f02-40b3-af01-3de313c51331",    // 公司id
          DepartmentId: "6e75d6af-4bed-4c31-bd33-51861e9e4792",    // 部门id
          IconUrl: "this is a string",    // 图标存放地址
          FullDescription: "this is a string",    // 备注详情
          Versions: [
            {
              Id: "2326bcbc-ebb9-48ad-8f23-338f9307994d",    // 唯一标识
              PackageId: "35282205-087c-4968-8d84-1c2af5eb37fb",    // 流程包id
              Version: "this is a string",    // 机器人版本
              Description: "this is a string",    // 备注
              Arguments: [
                {
                  Name: "this is a string",    // 名称
                  Type: "this is a string",    // 参数类型
                  Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
                  DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
                  AssetContent: {
                    Name: "this is a string",    // 名称
                    Description: "this is a string",    // 备注
                    IsRequiredEncryption: false    // 是否加密
                  }    // 使用的资产
                },
                {
                  // 略，结构同前一节点
                }
              ],    // 参数
              ETag: "this is a string",    // 版本控制标记
              UploadTime: "2022-07-29T12:13:49.781Z",    // 上传时间
              TotalDownloads: 75,    // 下载计数
              CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
              ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
              CreatedBy: "4b973f0c-b298-4062-9ef4-695c58ff42b4",    // 创建人id
              CreatedByName: "this is a string",    // 创建人名称
              ModifiedBy: "b743f25f-2d81-4c5c-a503-8b8cc92573bb",    // 更新人id
              ModifiedByName: "this is a string",    // 更新人名称
              CompanyId: "892c2bcb-6619-442a-8e79-7e5e6465bea2",    // 公司id
              DepartmentId: "1c23661f-724c-461a-b945-372446f4314e",    // 部门id
              FullDescription: "this is a string"    // 备注详情
            },
            {
              // 略，结构同前一节点
            }
          ]    // 流程包所有版本
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 获取流程包详情<span id="获取流程包详情"><span>

<!-- ##### 功能介绍
-->
根据packageId获取一个流程包具体的详细信息

<!-- ##### 基本信息
-->
**Path：** /openapi/packages/{packageId}

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "ee190999-9a73-423b-9fc8-6dde2d91d9f0",    // 唯一标识
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      TotalDownloads: 64,    // 下载计数
      LastVersion: "this is a string",    // 最新版本号
      LastVersionId: "06e19272-2b7d-470e-8227-f27418517f13",    // 最高版本id
      CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
      ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
      CreatedBy: "7aa3d616-b6ea-470e-8205-e50dc886b033",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedBy: "6146fed5-e624-4e2e-8e59-8e4a94af1932",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      Tags: ["this is a string","this is a string"],    // 标签
      CompanyId: "dc120332-1f02-40b3-af01-3de313c51331",    // 公司id
      DepartmentId: "6e75d6af-4bed-4c31-bd33-51861e9e4792",    // 部门id
      IconUrl: "this is a string",    // 图标存放地址
      FullDescription: "this is a string",    // 备注详情
      Versions: [
        {
          Id: "2326bcbc-ebb9-48ad-8f23-338f9307994d",    // 唯一标识
          PackageId: "35282205-087c-4968-8d84-1c2af5eb37fb",    // 流程包id
          Version: "this is a string",    // 机器人版本
          Description: "this is a string",    // 备注
          Arguments: [
            {
              Name: "this is a string",    // 名称
              Type: "this is a string",    // 参数类型
              Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
              DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
              AssetContent: {
                Name: "this is a string",    // 名称
                Description: "this is a string",    // 备注
                IsRequiredEncryption: false    // 是否加密
              }    // 使用的资产
            },
            {
              // 略，结构同前一节点
            }
          ],    // 参数
          ETag: "this is a string",    // 版本控制标记
          UploadTime: "2022-07-29T12:13:49.781Z",    // 上传时间
          TotalDownloads: 75,    // 下载计数
          CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
          ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
          CreatedBy: "4b973f0c-b298-4062-9ef4-695c58ff42b4",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedBy: "b743f25f-2d81-4c5c-a503-8b8cc92573bb",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          CompanyId: "892c2bcb-6619-442a-8e79-7e5e6465bea2",    // 公司id
          DepartmentId: "1c23661f-724c-461a-b945-372446f4314e",    // 部门id
          FullDescription: "this is a string"    // 备注详情
        },
        {
          // 略，结构同前一节点
        }
      ]    // 流程包所有版本
    }

#### 更新流程包<span id="更新流程包"><span>

<!-- ##### 功能介绍
-->
根据流程包packageId更新流程包描述和标签

<!-- ##### 基本信息
-->
**Path：** /openapi/packages/{packageId}

**Method：** PATCH

**请求参考示例：**

    {
      ETag: "this is a string",    // 版本控制标记
      Tags: ["this is a string","this is a string"]    // 标签
    }
**响应参考示例：**

    {
      Id: "ee190999-9a73-423b-9fc8-6dde2d91d9f0",    // 唯一标识
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      TotalDownloads: 64,    // 下载计数
      LastVersion: "this is a string",    // 最新版本号
      LastVersionId: "06e19272-2b7d-470e-8227-f27418517f13",    // 最高版本id
      CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
      ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
      CreatedBy: "7aa3d616-b6ea-470e-8205-e50dc886b033",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedBy: "6146fed5-e624-4e2e-8e59-8e4a94af1932",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      Tags: ["this is a string","this is a string"],    // 标签
      CompanyId: "dc120332-1f02-40b3-af01-3de313c51331",    // 公司id
      DepartmentId: "6e75d6af-4bed-4c31-bd33-51861e9e4792",    // 部门id
      IconUrl: "this is a string",    // 图标存放地址
      FullDescription: "this is a string",    // 备注详情
      Versions: [
        {
          Id: "2326bcbc-ebb9-48ad-8f23-338f9307994d",    // 唯一标识
          PackageId: "35282205-087c-4968-8d84-1c2af5eb37fb",    // 流程包id
          Version: "this is a string",    // 机器人版本
          Description: "this is a string",    // 备注
          Arguments: [
            {
              Name: "this is a string",    // 名称
              Type: "this is a string",    // 参数类型
              Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
              DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
              AssetContent: {
                Name: "this is a string",    // 名称
                Description: "this is a string",    // 备注
                IsRequiredEncryption: false    // 是否加密
              }    // 使用的资产
            },
            {
              // 略，结构同前一节点
            }
          ],    // 参数
          ETag: "this is a string",    // 版本控制标记
          UploadTime: "2022-07-29T12:13:49.781Z",    // 上传时间
          TotalDownloads: 75,    // 下载计数
          CreatedAt: "2022-07-29T12:13:49.781Z",    // 创建时间
          ModifiedAt: "2022-07-29T12:13:49.781Z",    // 更新时间
          CreatedBy: "4b973f0c-b298-4062-9ef4-695c58ff42b4",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedBy: "b743f25f-2d81-4c5c-a503-8b8cc92573bb",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          CompanyId: "892c2bcb-6619-442a-8e79-7e5e6465bea2",    // 公司id
          DepartmentId: "1c23661f-724c-461a-b945-372446f4314e",    // 部门id
          FullDescription: "this is a string"    // 备注详情
        },
        {
          // 略，结构同前一节点
        }
      ]    // 流程包所有版本
    }

#### 删除流程包<span id="删除流程包"><span>

<!-- ##### 功能介绍
-->
根据packageId删除流程包

<!-- ##### 基本信息
-->
**Path：** /openapi/packages/{packageId}

**Method：** DELETE

**请求参考示例：**

无内容

**响应参考示例：**

无内容

#### 上传流程包并创建信息<span id="上传流程包并创建信息"><span>

<!-- ##### 功能介绍
-->
上传流程包文件并生成流程包版本信息。
注意：当流程包（.dgs 文件）大于 200M 时，创建流程包应按如下步骤实施：
1. 获取上传通道/地址，参见[【生成流程包上传地址】](#生成流程包上传地址)
2. 上传流程包 dgs 文件，参见[【通用上传文件流地址】](#通用上传文件流地址)
3. 通知完成上传，参见[【通知流程包上传完成】](#通知流程包上传完成)

<!-- ##### 基本信息
-->
**Path：** /openapi/packages

**Method：** PUT

**请求参考示例：**

*注意：请求头信息Content-Type应设置application/octet-stream*

    [二进制文件流数据]

**响应参考示例：**

    {
      PackageId: "842e892d-dc3b-48ce-ab50-1c9be3fb0721",    // 流程包id
      PackageVersionId: "58975958-4289-4c0e-a800-14311c0444d9",    // 流程包版本id
      PackageName: "this is a string",    // 流程包名称
      LastVersion: "this is a string"    // 最新版本号
    }

#### 生成流程包上传地址<span id="生成流程包上传地址"><span>

<!-- ##### 功能介绍
-->
在不知道 dgs 信息的情况下创建上传通道

<!-- ##### 基本信息
-->
**Path：** /openapi/preloadedVersionFiles

**Method：** POST

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "1b528e05-69bd-4ccc-91bd-1b4a07bc7e63",    // 唯一标识
      Channel: {
        Uri: "this is a string",    // Url地址
        Headers: {"Content-Type":"application/octet-stream"}    // 请求Headers
      },    // 上传通道
      CreatedAt: "2022-07-29T12:13:49.782Z",    // 创建时间
      CompanyId: "5ed1a0ed-b1e3-41a4-b875-f5432af4f606",    // 公司id
      DepartmentId: "cec896b0-c7ac-4532-8197-e94fa637927e"    // 部门id
    }

#### 通用上传文件流地址<span id="通用上传文件流地址"><span>

<!-- ##### 功能介绍
-->
通过获取上传地址后将文件通过该接口上传至控制台

<!-- ##### 基本信息
-->
**Path：** 通过[【生成流程包上传地址】](#生成流程包上传地址)获取到的uri地址

**Method：** PUT

**请求参考示例：**

*注意：需将[【生成流程包上传地址】](#生成流程包上传地址)返回的headers数据以键值对方式填写在该接口的HTTP Headers中*

    [二进制文件流数据]

**响应参考示例：**

无内容

#### 通知流程包上传完成<span id="通知流程包上传完成"><span>

<!-- ##### 功能介绍
-->
通过上传地址完成上传文件后调用该接口, 路径中id为[【生成流程包上传地址】](#生成流程包上传地址)返回的Id

<!-- ##### 基本信息
-->
**Path：** /openapi/preloadedVersionFiles/{id}

**Method：** PATCH

**请求参考示例：**

无内容

**响应参考示例：**

    {
      PackageId: "842e892d-dc3b-48ce-ab50-1c9be3fb0721",    // 流程包id
      PackageVersionId: "58975958-4289-4c0e-a800-14311c0444d9",    // 流程包版本id
      PackageName: "this is a string",    // 流程包名称
      LastVersion: "this is a string"    // 最新版本号
    }

---

### 机器人组<span id="机器人组"><span>

#### 查询机器人组列表<span id="查询机器人组列表"><span>

<!-- ##### 功能介绍
-->
根据指定条件查询机器人组列表

<!-- ##### 基本信息
-->
**Path：** /openapi/queues

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>Name</td><td>String</td><td>名称，模糊匹配</td></tr>
<tr><td>SearchString</td><td>String</td><td>关键字，模糊匹配</td></tr>
<tr><td>IsDesc</td><td>Boolean</td><td>是否按创建时间降序排序，默认true,说明:true-降序；false-升序</td></tr>
<tr><td>AssociatedQueueId</td><td>String</td><td>机器人组id，格式:guid/uuid</td></tr>
<tr><td>PackageId</td><td>String</td><td>流程包id，格式:guid/uuid</td></tr>
<tr><td>PackageVersionId</td><td>String</td><td>流程包版本id，格式:guid/uuid</td></tr>
<tr><td>PageIndex</td><td>Int</td><td>页码（从0开始）</td></tr>
<tr><td>PageSize</td><td>Int</td><td>页大小（默认20）</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 22,    // 查询命中总记录数
      List: [
        {
          Id: "0dc930eb-2e40-446f-93b1-c93c019fb914",    // 唯一标识
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          Tags: ["this is a string","this is a string"],    // 标签
          Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
          CreatedAt: "2022-07-29T12:13:49.783Z",    // 创建时间
          CreatedBy: "948e1573-2dbc-4c42-81e3-495e41f6aaba",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedAt: "2022-07-29T12:13:49.783Z",    // 更新时间
          ModifiedBy: "4540b03c-814d-4d48-ab2e-0ced36bb9e0c",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          RobotCount: 76,    // 包含机器人数量
          CompanyId: "5170669b-fb34-4af2-bc79-51dd05241da0",    // 公司id
          DepartmentId: "ac87d0c2-3db0-4c50-9a0f-d4bdadb55542"    // 部门id
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 根据id获取机器人组信息<span id="根据id获取机器人组信息"><span>

<!-- ##### 功能介绍
-->
根据Id获取机器人组

<!-- ##### 基本信息
-->
**Path：** /openapi/queues/{queueId}

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "0dc930eb-2e40-446f-93b1-c93c019fb914",    // 唯一标识
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"],    // 标签
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      CreatedAt: "2022-07-29T12:13:49.783Z",    // 创建时间
      CreatedBy: "948e1573-2dbc-4c42-81e3-495e41f6aaba",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.783Z",    // 更新时间
      ModifiedBy: "4540b03c-814d-4d48-ab2e-0ced36bb9e0c",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      RobotCount: 76,    // 包含机器人数量
      CompanyId: "5170669b-fb34-4af2-bc79-51dd05241da0",    // 公司id
      DepartmentId: "ac87d0c2-3db0-4c50-9a0f-d4bdadb55542"    // 部门id
    }

#### 删除机器人组<span id="删除机器人组"><span>

<!-- ##### 功能介绍
-->
根据Id删除机器人组

<!-- ##### 基本信息
-->
**Path：** /openapi/queues/{queueId}

**Method：** DELETE

**请求参考示例：**

无内容

**响应参考示例：**

无内容

#### 更新机器人组信息<span id="更新机器人组信息"><span>

<!-- ##### 功能介绍
-->
根据Id更新机器人组信息

<!-- ##### 基本信息
-->
**Path：** /openapi/queues/{queueId}

**Method：** PATCH

**请求参考示例：**

    {
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"]    // 标签
    }
**响应参考示例：**

    {
      Id: "0dc930eb-2e40-446f-93b1-c93c019fb914",    // 唯一标识
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"],    // 标签
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      CreatedAt: "2022-07-29T12:13:49.783Z",    // 创建时间
      CreatedBy: "948e1573-2dbc-4c42-81e3-495e41f6aaba",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.783Z",    // 更新时间
      ModifiedBy: "4540b03c-814d-4d48-ab2e-0ced36bb9e0c",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      RobotCount: 76,    // 包含机器人数量
      CompanyId: "5170669b-fb34-4af2-bc79-51dd05241da0",    // 公司id
      DepartmentId: "ac87d0c2-3db0-4c50-9a0f-d4bdadb55542"    // 部门id
    }

#### 创建机器人组<span id="创建机器人组"><span>

<!-- ##### 功能介绍
-->
创建机器人组

<!-- ##### 基本信息
-->
**Path：** /openapi/queues/{queueId}

**Method：** POST

**请求参考示例：**

    {
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"],    // 标签
      CompanyId: "f0f31fa4-a85b-413e-a9d5-d6c2b650eb41",    // 公司id
      DepartmentId: "5c353854-3640-4c1e-8275-0375ac7a49ad",    // 部门id
      CreateBy: "25540342-ac36-4003-a665-14793a005078",    // 创建人id
      CreateByName: "this is a string"    // 创建人名称
    }
**响应参考示例：**

    {
      Id: "0dc930eb-2e40-446f-93b1-c93c019fb914",    // 唯一标识
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"],    // 标签
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      CreatedAt: "2022-07-29T12:13:49.783Z",    // 创建时间
      CreatedBy: "948e1573-2dbc-4c42-81e3-495e41f6aaba",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.783Z",    // 更新时间
      ModifiedBy: "4540b03c-814d-4d48-ab2e-0ced36bb9e0c",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      RobotCount: 76,    // 包含机器人数量
      CompanyId: "5170669b-fb34-4af2-bc79-51dd05241da0",    // 公司id
      DepartmentId: "ac87d0c2-3db0-4c50-9a0f-d4bdadb55542"    // 部门id
    }

---

### 机器人<span id="机器人"><span>

#### 查询机器人列表<span id="查询机器人列表"><span>

<!-- ##### 功能介绍
-->
根据指定查询条件，获取机器人列表

<!-- ##### 基本信息
-->
**Path：** /openapi/robots

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>Name</td><td>String</td><td>名称，模糊匹配</td></tr>
<tr><td>SearchString</td><td>String</td><td>关键字，模糊匹配</td></tr>
<tr><td>IsDesc</td><td>Boolean</td><td>是否按创建时间降序排序，默认true,说明:true-降序；false-升序</td></tr>
<tr><td>AssociatedQueueId</td><td>String</td><td>机器人组id，格式:guid/uuid</td></tr>
<tr><td>PackageId</td><td>String</td><td>流程包id，格式:guid/uuid</td></tr>
<tr><td>PackageVersionId</td><td>String</td><td>流程包版本id，格式:guid/uuid</td></tr>
<tr><td>PageIndex</td><td>Int</td><td>页码（从0开始）</td></tr>
<tr><td>PageSize</td><td>Int</td><td>页大小（默认20）</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 41,    // 查询命中总记录数
      List: [
        {
          Id: "545b37c3-286a-4296-9b40-e89b974a3b93",    // 唯一标识
          CurrentDeviceId: "7ab942da-9e6f-43db-8149-46472a639b08",    // 当前所在设备的id
          LastHeartbeatTime: "2022-07-29T12:13:49.788Z",    // 最近心跳时间
          ListeningStatus: ,    // 许可状态
          CompanyId: "d572ed1f-c4e8-4335-bbb7-4f882199cf7f",    // 公司id
          DepartmentId: "fea0120a-eafa-49d1-b2ab-521e8db183b5",    // 部门id
          SdkVersion: "this is a string",    // 机器人sdk版本
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          CanUpgrade: false,    // 是否可升级
          LicenseStatus: "Unlicensed",    // 许可状态:Unlicensed-未许可;ClientLicensed-本地许可;ServerLicensed-控制台许可;PoolLicensed-浮动许可
          ClientSku: "this is a string",    // 机器人许可类型
          Version: "this is a string",    // 机器人版本
          Status: "Disconnected"    // 机器人状态:Disconnected-已断开;Ready-空闲;Busy-忙碌
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 获取机器人详情<span id="获取机器人详情"><span>

<!-- ##### 功能介绍
-->
根据id获取机器人详情

<!-- ##### 基本信息
-->
**Path：** /openapi/robots/{robotId}

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "545b37c3-286a-4296-9b40-e89b974a3b93",    // 唯一标识
      CurrentDeviceId: "7ab942da-9e6f-43db-8149-46472a639b08",    // 当前所在设备的id
      LastHeartbeatTime: "2022-07-29T12:13:49.788Z",    // 最近心跳时间
      ListeningStatus: ,    // 许可状态
      CompanyId: "d572ed1f-c4e8-4335-bbb7-4f882199cf7f",    // 公司id
      DepartmentId: "fea0120a-eafa-49d1-b2ab-521e8db183b5",    // 部门id
      SdkVersion: "this is a string",    // 机器人sdk版本
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      CanUpgrade: false,    // 是否可升级
      LicenseStatus: "Unlicensed",    // 许可状态:Unlicensed-未许可;ClientLicensed-本地许可;ServerLicensed-控制台许可;PoolLicensed-浮动许可
      ClientSku: "this is a string",    // 机器人许可类型
      Version: "this is a string",    // 机器人版本
      Status: "Disconnected"    // 机器人状态:Disconnected-已断开;Ready-空闲;Busy-忙碌
    }

---

### 用户<span id="用户"><span>

#### 查询当前用户信息<span id="查询当前用户信息"><span>

<!-- ##### 功能介绍
-->
获取当前公司用户自己的信息

<!-- ##### 基本信息
-->
**Path：** /openapi/companyusers/self

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      UserExtensionInfo: {
        ExtensionId: "this is a string",    // 扩展字段-id
        ExtensionMobile: "this is a string",    // 扩展字段-手机号
        ExtensionEmail: "this is a string"    // 扩展字段-邮箱
      },    // user extensiong info
      IsExternalUser: false,    // is third party user
      HasModifiedPassword: false,    // 
      Id: "b9e1ef45-36a0-459b-abf2-26f6433f3c40",    // 唯一标识
      UserId: "fb2e0462-a048-4da4-b817-572e019a4b42",    // user id
      CompanyId: "9758f386-542e-4c5e-bf0c-ec2aecd4a585",    // 公司id
      IsCompanyOwner: false,    // is company owner
      RoleIds: ["67546cd8-1d7d-475d-a054-4fed08294a39","67546cd8-1d7d-475d-a054-4fed08294a39"],    // roleIds
      Status: "Active",    // 机器人状态:Active-活跃;Inactive-未激活;Banned-禁用
      ResourceType: "Company",    // resource type:Company;Department;CompanyUser;Robot;Workflow;Queue;RunInstance;Dashboard;DataQueue;Asset;App;AppVersion;DataConnection;DataSource;SamplePackage;Package;PackageVersion;RpaLicenseBinding;TaskQueue
      AssignedDepartmentId: "35b7da12-e098-4a10-b88d-8fb27a67f3b6",    // 当前选中部门id
      ParentResourceType: "Company",    // resource type of parent:Company;Department;CompanyUser;Robot;Workflow;Queue;RunInstance;Dashboard;DataQueue;Asset;App;AppVersion;DataConnection;DataSource;SamplePackage;Package;PackageVersion;RpaLicenseBinding;TaskQueue
      ParentId: "42031040-25ae-44bb-a9c0-a90ae21123a3",    // parent id
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      ETag: "this is a string",    // 版本控制标记
      Tags: ["this is a string","this is a string"],    // 标签
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      CreatedAt: "2022-07-29T12:13:49.784Z",    // 创建时间
      ModifiedAt: "2022-07-29T12:13:49.784Z",    // 更新时间
      LastLoginAt: "2022-07-29T12:13:49.784Z",    // 最近登录时间
      DepartmentPath: "this is a string",    // 部门树路径
      Email: "this is a string",    // 邮箱
      PhoneNumber: "this is a string",    // user phone number
      UserName: "this is a string"    // account user name
    }

---

### 流程部署<span id="流程部署"><span>

#### 查询流程部署列表<span id="查询流程部署列表"><span>

<!-- ##### 功能介绍
-->
根据指定查询条件，获取流程部署列表

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>Name</td><td>String</td><td>名称，模糊匹配</td></tr>
<tr><td>SearchString</td><td>String</td><td>关键字，模糊匹配</td></tr>
<tr><td>IsDesc</td><td>Boolean</td><td>是否按创建时间降序排序，默认true,说明:true-降序；false-升序</td></tr>
<tr><td>AssociatedQueueId</td><td>String</td><td>机器人组id，格式:guid/uuid</td></tr>
<tr><td>PackageId</td><td>String</td><td>流程包id，格式:guid/uuid</td></tr>
<tr><td>PackageVersionId</td><td>String</td><td>流程包版本id，格式:guid/uuid</td></tr>
<tr><td>PageIndex</td><td>Int</td><td>页码（从0开始）</td></tr>
<tr><td>PageSize</td><td>Int</td><td>页大小（默认20）</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 17,    // 查询命中总记录数
      List: [
        {
          Id: "ac87fd69-af43-4378-984a-ca806f826e50",    // 唯一标识
          DepartmentId: "01b6ca01-0e54-45a5-8a11-533157f16599",    // 部门id
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          Arguments: [
            {
              Name: "this is a string",    // 名称
              Type: "this is a string",    // 参数类型
              Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
              DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
              AssetContent: {
                Name: "this is a string",    // 名称
                Description: "this is a string",    // 备注
                IsRequiredEncryption: false    // 是否加密
              }    // 使用的资产
            },
            {
              // 略，结构同前一节点
            }
          ],    // 参数
          Tags: ["this is a string","this is a string"],    // 标签
          VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
          Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
          JobStateNotification: {
            SwitchOn: false,    // 通知功能是否启用
            JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
            Conditions: ,    // 通知条件
            Recipients: ["this is a string","this is a string"]    // 邮件接收者
          },    // 运行状态通知
          PackageName: "this is a string",    // 流程包名称
          PackageId: "9e34c367-9d32-4890-afb9-235e06490c92",    // 流程包id
          PackageVersionId: "bf6a36a7-0fe5-4174-a80e-e86d578585d9",    // 流程包版本id
          PackageVersion: "this is a string",    // 流程包版本号
          AssociatedQueueId: "7a69bce7-f6b4-40c8-86a9-57529cb3c890",    // （执行目标）机器人组id
          Priority: 2000,    // 优先级，范围:0-5000
          MaxRetryCount: 1,    // 最大重试次数,范围:0-10
          TriggerPolicy: "SkipWhenNoResource",    // 执行策略:SkipWhenNoResource-无可用机器人时取消任务;AnyTime-无可用机器人时等待
          LastTriggeredAt: "2022-07-29T12:13:49.787Z",    // 最后触发时间
          TriggeredCount: 80,    // 触发计数
          CreatedAt: "2022-07-29T12:13:49.787Z",    // 创建时间
          CreatedBy: "86f58195-c889-4bd2-ae4f-d23f9aead58a",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedAt: "2022-07-29T12:13:49.787Z",    // 更新时间
          ModifiedBy: "d8a954e6-d40c-456b-a569-d2126741068f",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          CompanyId: "48c412a1-2940-4100-80e2-046faf7f958e"    // 公司id
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 获取流程部署详情<span id="获取流程部署详情"><span>

<!-- ##### 功能介绍
-->
根据id获取流程部署详情

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "ac87fd69-af43-4378-984a-ca806f826e50",    // 唯一标识
      DepartmentId: "01b6ca01-0e54-45a5-8a11-533157f16599",    // 部门id
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      Tags: ["this is a string","this is a string"],    // 标签
      VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      JobStateNotification: {
        SwitchOn: false,    // 通知功能是否启用
        JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
        Conditions: ,    // 通知条件
        Recipients: ["this is a string","this is a string"]    // 邮件接收者
      },    // 运行状态通知
      PackageName: "this is a string",    // 流程包名称
      PackageId: "9e34c367-9d32-4890-afb9-235e06490c92",    // 流程包id
      PackageVersionId: "bf6a36a7-0fe5-4174-a80e-e86d578585d9",    // 流程包版本id
      PackageVersion: "this is a string",    // 流程包版本号
      AssociatedQueueId: "7a69bce7-f6b4-40c8-86a9-57529cb3c890",    // （执行目标）机器人组id
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1,    // 最大重试次数,范围:0-10
      TriggerPolicy: "SkipWhenNoResource",    // 执行策略:SkipWhenNoResource-无可用机器人时取消任务;AnyTime-无可用机器人时等待
      LastTriggeredAt: "2022-07-29T12:13:49.787Z",    // 最后触发时间
      TriggeredCount: 80,    // 触发计数
      CreatedAt: "2022-07-29T12:13:49.787Z",    // 创建时间
      CreatedBy: "86f58195-c889-4bd2-ae4f-d23f9aead58a",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.787Z",    // 更新时间
      ModifiedBy: "d8a954e6-d40c-456b-a569-d2126741068f",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      CompanyId: "48c412a1-2940-4100-80e2-046faf7f958e"    // 公司id
    }

#### 创建流程部署<span id="创建流程部署"><span>

<!-- ##### 功能介绍
-->
创建流程部署

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows

**Method：** POST

**请求参考示例：**

    {
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Tags: ["this is a string","this is a string"],    // 标签
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
      JobStateNotification: {
        SwitchOn: false,    // 通知功能是否启用
        JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
        Conditions: ,    // 通知条件
        Recipients: ["this is a string","this is a string"]    // 邮件接收者
      },    // 运行状态通知
      PackageName: "this is a string",    // 流程包名称
      PackageId: "b0adccf0-97a7-4d27-9dc5-ede4096c3ffb",    // 流程包id
      PackageVersionId: "b544c811-2cc7-4b5a-8b98-fd724a2331e2",    // 流程包版本id
      PackageVersion: "this is a string",    // 流程包版本号
      AssociatedQueueId: "d677ae87-8274-485a-a918-76ee9e9fb772",    // （执行目标）机器人组id
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1,    // 最大重试次数,范围:0-10
      TriggerPolicy: "SkipWhenNoResource"    // 执行策略:SkipWhenNoResource-无可用机器人时取消任务;AnyTime-无可用机器人时等待
    }
**响应参考示例：**

    {
      Id: "ac87fd69-af43-4378-984a-ca806f826e50",    // 唯一标识
      DepartmentId: "01b6ca01-0e54-45a5-8a11-533157f16599",    // 部门id
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      Tags: ["this is a string","this is a string"],    // 标签
      VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      JobStateNotification: {
        SwitchOn: false,    // 通知功能是否启用
        JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
        Conditions: ,    // 通知条件
        Recipients: ["this is a string","this is a string"]    // 邮件接收者
      },    // 运行状态通知
      PackageName: "this is a string",    // 流程包名称
      PackageId: "9e34c367-9d32-4890-afb9-235e06490c92",    // 流程包id
      PackageVersionId: "bf6a36a7-0fe5-4174-a80e-e86d578585d9",    // 流程包版本id
      PackageVersion: "this is a string",    // 流程包版本号
      AssociatedQueueId: "7a69bce7-f6b4-40c8-86a9-57529cb3c890",    // （执行目标）机器人组id
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1,    // 最大重试次数,范围:0-10
      TriggerPolicy: "SkipWhenNoResource",    // 执行策略:SkipWhenNoResource-无可用机器人时取消任务;AnyTime-无可用机器人时等待
      LastTriggeredAt: "2022-07-29T12:13:49.787Z",    // 最后触发时间
      TriggeredCount: 80,    // 触发计数
      CreatedAt: "2022-07-29T12:13:49.787Z",    // 创建时间
      CreatedBy: "86f58195-c889-4bd2-ae4f-d23f9aead58a",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.787Z",    // 更新时间
      ModifiedBy: "d8a954e6-d40c-456b-a569-d2126741068f",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      CompanyId: "48c412a1-2940-4100-80e2-046faf7f958e"    // 公司id
    }

#### 更新流程部署<span id="更新流程部署"><span>

<!-- ##### 功能介绍
-->
根据id更新流程部署详情

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}

**Method：** PATCH

**请求参考示例：**

    {
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      Tags: ["this is a string","this is a string"],    // 标签
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      VideoRecordMode: ,    // 视频录制模式
      JobStateNotification: {
        SwitchOn: false,    // 通知功能是否启用
        JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
        Conditions: ,    // 通知条件
        Recipients: ["this is a string","this is a string"]    // 邮件接收者
      },    // 运行状态通知
      TriggerPolicy: ,    // 执行策略
      PackageName: "this is a string",    // 流程包名称
      PackageVersionId: "afcb66b1-b7e5-4e7d-9ee7-5d7672118e4f",    // 流程包版本id
      PackageVersion: "this is a string",    // 流程包版本号
      AssociatedQueueId: "560f9708-164a-4336-80bf-9b81e49aa2b1",    // （执行目标）机器人组id
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1    // 最大重试次数,范围:0-10
    }
**响应参考示例：**

    {
      Id: "ac87fd69-af43-4378-984a-ca806f826e50",    // 唯一标识
      DepartmentId: "01b6ca01-0e54-45a5-8a11-533157f16599",    // 部门id
      Name: "this is a string",    // 名称
      Description: "this is a string",    // 备注
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      Tags: ["this is a string","this is a string"],    // 标签
      VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
      Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
      JobStateNotification: {
        SwitchOn: false,    // 通知功能是否启用
        JustNoticeAgainstLastRuninstance: false,    // 通知功能是否启用
        Conditions: ,    // 通知条件
        Recipients: ["this is a string","this is a string"]    // 邮件接收者
      },    // 运行状态通知
      PackageName: "this is a string",    // 流程包名称
      PackageId: "9e34c367-9d32-4890-afb9-235e06490c92",    // 流程包id
      PackageVersionId: "bf6a36a7-0fe5-4174-a80e-e86d578585d9",    // 流程包版本id
      PackageVersion: "this is a string",    // 流程包版本号
      AssociatedQueueId: "7a69bce7-f6b4-40c8-86a9-57529cb3c890",    // （执行目标）机器人组id
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1,    // 最大重试次数,范围:0-10
      TriggerPolicy: "SkipWhenNoResource",    // 执行策略:SkipWhenNoResource-无可用机器人时取消任务;AnyTime-无可用机器人时等待
      LastTriggeredAt: "2022-07-29T12:13:49.787Z",    // 最后触发时间
      TriggeredCount: 80,    // 触发计数
      CreatedAt: "2022-07-29T12:13:49.787Z",    // 创建时间
      CreatedBy: "86f58195-c889-4bd2-ae4f-d23f9aead58a",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.787Z",    // 更新时间
      ModifiedBy: "d8a954e6-d40c-456b-a569-d2126741068f",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      CompanyId: "48c412a1-2940-4100-80e2-046faf7f958e"    // 公司id
    }

#### 删除流程部署<span id="删除流程部署"><span>

<!-- ##### 功能介绍
-->
根据id删除流程部署

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}

**Method：** DELETE

**请求参考示例：**

无内容

**响应参考示例：**

无内容

#### 执行流程部署<span id="执行流程部署"><span>

<!-- ##### 功能介绍
-->
根据id执行流程部署

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}/execute

**Method：** POST

**请求参考示例：**

    {
      Source: "External",    // 来源:External-外部系统
      Arguments: [
        {
          Name: "this is a string",    // 名称
          Type: "this is a string",    // 参数类型
          Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
          DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
          AssetContent: {
            Name: "this is a string",    // 名称
            Description: "this is a string",    // 备注
            IsRequiredEncryption: false    // 是否加密
          }    // 使用的资产
        },
        {
          // 略，结构同前一节点
        }
      ],    // 参数
      VideoRecordMode: ,    // 视频录制模式
      Priority: 2000,    // 优先级，范围:0-5000
      MaxRetryCount: 1,    // 最大重试次数,范围:0-10
      StartupType: ,    // 启动类型
      StartupId: "fbf73372-34c5-4e82-a971-d01e3819f3fa",    // 启动资源Id
      StartupName: "this is a string",    // 启动资源名
      JobSubjectId: "51b2a214-b8c5-4f78-b280-b8ad80983985",    // Job关联体id
      JobSubjectName: "this is a string",    // Job关联体名称
      JobSubjectType: "this is a string"    // Job关联体类型
    }
**响应参考示例：**

    [
      {
        Id: "ad3e31ac-8980-43a0-9266-bdecfb022f3f",    // 唯一标识
        WorkflowId: "148eeb2b-9938-4029-ae93-009a265df2d0",    // 流程部署id
        Name: "this is a string",    // 名称
        Description: "this is a string",    // 备注
        PackageId: "af65447f-8a68-4f65-8526-da6246ea39d5",    // 流程包id
        PackageName: "this is a string",    // 流程包名称
        PackageVersion: "this is a string",    // 流程包版本号
        PackageVersionId: "bcd6c134-1eca-493e-b69f-c3d2c060cd3d",    // 流程包版本id
        Arguments: [
          {
            Name: "this is a string",    // 名称
            Type: "this is a string",    // 参数类型
            Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
            DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
            AssetContent: {
              Name: "this is a string",    // 名称
              Description: "this is a string",    // 备注
              IsRequiredEncryption: false    // 是否加密
            }    // 使用的资产
          },
          {
            // 略，结构同前一节点
          }
        ],    // 参数
        ContainingQueueId: "b19e7d10-d65a-4ea7-af99-1e6efeb8f423",    // 运行目标机器人组id
        Priority: 2000,    // 优先级，范围:0-5000
        State: "Queued",    // 状态:Queued-等待中;Running-运行中;Failed-失败;Cancelled-已取消;Succeeded-成功;Paused-已暂停
        DisplayState: "Queued",    // 显示状态:Queued-等待中;Running-运行中;Failed-失败;Cancelled-已取消;Succeeded-成功;Paused-已暂停
        VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
        Message: "this is a string",    // 原因说明
        LastRunInstaceId: "6f5991aa-f2a2-429b-855c-87082f4876fc",    // 最近运行实例id
        LastRobotName: "this is a string",    // 最近运行的机器人名称
        StartedAt: "2022-07-29T12:13:49.790Z",    // 开始运行时间
        FinishedAt: "2022-07-29T12:13:49.790Z",    // 结束运行时间
        RetriedCount: 2,    // 重试计数
        MaxRetryCount: 1,    // 最大重试次数,范围:0-10
        DepartmentId: "9a4f049f-fa1e-479d-890e-7b012b590321",    // 部门id
        CompanyId: "e20bce36-c239-4251-95ed-3cdf0c0f42bf",    // 公司id
        CronTriggerId: "4048caea-1fc6-4716-8262-7e2f359f107b",    // 触发的定时器id,非定时器触发时为null
        JobExecutionPolicy: ,    // 执行策略
        CreatedAt: "2022-07-29T12:13:49.790Z",    // 创建时间
        CreatedBy: "534d71f9-38fa-4813-b93b-b7c2ab8e812f",    // 创建人id
        CreatedByName: "this is a string",    // 创建人名称
        ModifiedAt: "2022-07-29T12:13:49.790Z",    // 更新时间
        ModifiedBy: "ac6dc477-6aab-4fe8-9f23-0745e2de563b",    // 更新人id
        ModifiedByName: "this is a string",    // 更新人名称
        JobStartupType: ,    // 启动方式
        JobStartupId: "75baaaff-04d0-41f9-b524-c1b0f35eedd6",    // 启动方式id，例如定时器id，或任务队列id
        JobStartupName: "this is a string",    // 启动方式名称,例如定时器名称，或任务队列名称
        JobGroupId: "2ef33453-9763-4587-b264-9f21e1db3830",    // 所属任务组id
        SeqNum: 78,    // 执行序号
        Step: "this is a string",    // 步骤编号，用于展示
        JobSubjectId: "4493488f-6e50-4ecd-92e8-1c25fddf8411",    // Job关联体id
        JobSubjectName: "this is a string",    // Job关联体名称
        JobSubjectType: "this is a string"    // Job关联体类型
      },
      {
        // 略，结构同前一节点
      }
    ]

#### 获取流程部署关联机器人列表<span id="获取流程部署关联机器人列表"><span>

<!-- ##### 功能介绍
-->
根据指定流程部署Id，获取流程部署关联的机器人列表

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}/robots

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 41,    // 查询命中总记录数
      List: [
        {
          Id: "545b37c3-286a-4296-9b40-e89b974a3b93",    // 唯一标识
          CurrentDeviceId: "7ab942da-9e6f-43db-8149-46472a639b08",    // 当前所在设备的id
          LastHeartbeatTime: "2022-07-29T12:13:49.788Z",    // 最近心跳时间
          ListeningStatus: ,    // 许可状态
          CompanyId: "d572ed1f-c4e8-4335-bbb7-4f882199cf7f",    // 公司id
          DepartmentId: "fea0120a-eafa-49d1-b2ab-521e8db183b5",    // 部门id
          SdkVersion: "this is a string",    // 机器人sdk版本
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          CanUpgrade: false,    // 是否可升级
          LicenseStatus: "Unlicensed",    // 许可状态:Unlicensed-未许可;ClientLicensed-本地许可;ServerLicensed-控制台许可;PoolLicensed-浮动许可
          ClientSku: "this is a string",    // 机器人许可类型
          Version: "this is a string",    // 机器人版本
          Status: "Disconnected"    // 机器人状态:Disconnected-已断开;Ready-空闲;Busy-忙碌
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 批量增加流程部署关联机器人<span id="批量增加流程部署关联机器人"><span>

<!-- ##### 功能介绍
-->
根据指定流程部署Id，为流程部署关联执行使用的机器人

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}/robots

**Method：** POST

**请求参考示例：**

    {
      RobotIds: ["8a11ba8f-66b3-44ec-a8c2-fd10fca58c9a","8a11ba8f-66b3-44ec-a8c2-fd10fca58c9a"]    // 机器人id列表
    }
**响应参考示例：**

    [
      {
        WorkflowId: "ba41bc8e-d636-4c01-9d7c-e4027799eb57",    // 流程部署id
        RobotId: "4f8065b9-5569-42d3-a2cc-920abea214de",    // 机器人Id
        ErrorMessage: "this is a string"    // 关联失败原因
      },
      {
        // 略，结构同前一节点
      }
    ]

#### 删除流程部署执行目标机器人<span id="删除流程部署执行目标机器人"><span>

<!-- ##### 功能介绍
-->
根据指定流程部署Id，为流程部署移除关联的机器人

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/{workflowId}/robots/{robotId}

**Method：** DELETE

**请求参考示例：**

无内容

**响应参考示例：**

无内容

#### 批量更新（关联的）流程包到最新版本<span id="批量更新（关联的）流程包到最新版本"><span>

<!-- ##### 功能介绍
-->
批量更新流程部署，使其使用最新版本流程包

<!-- ##### 基本信息
-->
**Path：** /openapi/workflows/batch/upgrade

**Method：** POST

**请求参考示例：**

    {
      WorkflowIds: ["970d4d24-81db-4ca4-8509-153195d10e83","970d4d24-81db-4ca4-8509-153195d10e83"]    // 流程部署id列表
    }
**响应参考示例：**

    {
      Total: 20,    // 批量操作总数目
      SuccessCount: 18,    // 成功数量
      FailureCount: 1,    // 失败数量
      MissingCount: 1,    // 缺失（未找到记录）数量
      FailedList: [
        {
          Id: "this is a string",    // 唯一标识
          Name: "this is a string",    // 名称
          Message: "this is a string"    // 原因说明
        },
        {
          // 略，结构同前一节点
        }
      ],    // 失败详情
      WarningList: [
        {
          Id: "this is a string",    // 唯一标识
          Name: "this is a string",    // 名称
          Message: "this is a string"    // 原因说明
        },
        {
          // 略，结构同前一节点
        }
      ]    // 告警详情
    }

---

### 流程编排<span id="流程编排"><span>

#### 获取流程编排列表<span id="获取流程编排列表"><span>

<!-- ##### 功能介绍
-->
根据指定查询条件，获取流程编排列表

<!-- ##### 基本信息
-->
**Path：** /openapi/workflowlayouts

**Method：** GET
**Query string：**

<table>
<tr><td> 参数名称</td><td>参数类型</td><td>描述</td></tr>
<tr><td>Name</td><td>String</td><td>名称，模糊匹配</td></tr>
<tr><td>SearchString</td><td>String</td><td>关键字，模糊匹配名称、备注、标签</td></tr>
<tr><td>IsDesc</td><td>Boolean</td><td>是否按创建时间降序排序，默认true,说明:true-降序；false-升序</td></tr>
<tr><td>PageIndex</td><td>Int</td><td>页码（从0开始）</td></tr>
<tr><td>PageSize</td><td>Int</td><td>页大小（默认20）</td></tr>
</table>

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 60,    // 查询命中总记录数
      List: [
        {
          Id: "7affc8af-b6c9-45a1-b5f1-c3482e16d4ae",    // 唯一标识
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          Tags: ["this is a string","this is a string"],    // 标签
          Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
          Nodes: [
            {
              Id: "87cf506e-211d-4c5d-a5e2-b3264a109083",    // 唯一标识
              Index: 6,    // 索引
              Name: "this is a string",    // 名称
              WorkflowId: "c2b72aa1-5ea6-498d-add5-b13d68954d12",    // 流程部署id
              Description: "this is a string",    // 备注
              Tags: ["this is a string","this is a string"],    // 标签
              Arguments: [
                {
                  Name: "this is a string",    // 名称
                  Type: "this is a string",    // 参数类型
                  Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
                  DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
                  AssetContent: {
                    Name: "this is a string",    // 名称
                    Description: "this is a string",    // 备注
                    IsRequiredEncryption: false    // 是否加密
                  }    // 使用的资产
                },
                {
                  // 略，结构同前一节点
                }
              ],    // 参数
              CreatedAt: "2022-07-29T12:13:49.789Z",    // 创建时间
              CreatedBy: "4a4ca8b8-4ac5-4593-9f8d-c8c7861a7ecf",    // 创建人id
              CreatedByName: "this is a string",    // 创建人名称
              ModifiedAt: "2022-07-29T12:13:49.789Z",    // 更新时间
              ModifiedBy: "05c219d7-ae72-4fa6-97a3-183e746e9def",    // 更新人id
              ModifiedByName: "this is a string"    // 更新人名称
            },
            {
              // 略，结构同前一节点
            }
          ],    // 子任务列表
          LastTriggeredAt: "2022-07-29T12:13:49.789Z",    // 最后触发时间
          TriggeredCount: 38,    // 触发计数
          CompanyId: "9f2e097d-77af-4361-8edd-d8434bf5d52c",    // 公司id
          DepartmentId: "2f4c17fc-16ef-400f-bc86-da5e5252958c",    // 部门id
          CreatedAt: "2022-07-29T12:13:49.789Z",    // 创建时间
          CreatedBy: "91480078-dc08-4a60-b228-1ce19eb11aca",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedAt: "2022-07-29T12:13:49.789Z",    // 更新时间
          ModifiedBy: "b6a860cd-30d9-4d41-a4ab-af3b234250b5",    // 更新人id
          ModifiedByName: "this is a string"    // 更新人名称
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 根据id获取流程编排<span id="根据id获取流程编排"><span>

<!-- ##### 功能介绍
-->
根据id获取流程编排详情

<!-- ##### 基本信息
-->
**Path：** /openapi/workflowlayouts/{workflowlayoutId}

**Method：** GET

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Count: 60,    // 查询命中总记录数
      List: [
        {
          Id: "7affc8af-b6c9-45a1-b5f1-c3482e16d4ae",    // 唯一标识
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          Tags: ["this is a string","this is a string"],    // 标签
          Properties: {"Field1":"value1","Field2":"value2"},    // 附加属性
          Nodes: [
            {
              Id: "87cf506e-211d-4c5d-a5e2-b3264a109083",    // 唯一标识
              Index: 6,    // 索引
              Name: "this is a string",    // 名称
              WorkflowId: "c2b72aa1-5ea6-498d-add5-b13d68954d12",    // 流程部署id
              Description: "this is a string",    // 备注
              Tags: ["this is a string","this is a string"],    // 标签
              Arguments: [
                {
                  Name: "this is a string",    // 名称
                  Type: "this is a string",    // 参数类型
                  Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
                  DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
                  AssetContent: {
                    Name: "this is a string",    // 名称
                    Description: "this is a string",    // 备注
                    IsRequiredEncryption: false    // 是否加密
                  }    // 使用的资产
                },
                {
                  // 略，结构同前一节点
                }
              ],    // 参数
              CreatedAt: "2022-07-29T12:13:49.789Z",    // 创建时间
              CreatedBy: "4a4ca8b8-4ac5-4593-9f8d-c8c7861a7ecf",    // 创建人id
              CreatedByName: "this is a string",    // 创建人名称
              ModifiedAt: "2022-07-29T12:13:49.789Z",    // 更新时间
              ModifiedBy: "05c219d7-ae72-4fa6-97a3-183e746e9def",    // 更新人id
              ModifiedByName: "this is a string"    // 更新人名称
            },
            {
              // 略，结构同前一节点
            }
          ],    // 子任务列表
          LastTriggeredAt: "2022-07-29T12:13:49.789Z",    // 最后触发时间
          TriggeredCount: 38,    // 触发计数
          CompanyId: "9f2e097d-77af-4361-8edd-d8434bf5d52c",    // 公司id
          DepartmentId: "2f4c17fc-16ef-400f-bc86-da5e5252958c",    // 部门id
          CreatedAt: "2022-07-29T12:13:49.789Z",    // 创建时间
          CreatedBy: "91480078-dc08-4a60-b228-1ce19eb11aca",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedAt: "2022-07-29T12:13:49.789Z",    // 更新时间
          ModifiedBy: "b6a860cd-30d9-4d41-a4ab-af3b234250b5",    // 更新人id
          ModifiedByName: "this is a string"    // 更新人名称
        },
        {
          // 略，结构同前一节点
        }
      ]    // 当前页记录集合
    }

#### 执行流程编排<span id="执行流程编排"><span>

<!-- ##### 功能介绍
-->
根据id执行流程编排

<!-- ##### 基本信息
-->
**Path：** /openapi/workflowlayouts/{workflowlayoutId}/execute

**Method：** POST

**请求参考示例：**

无内容

**响应参考示例：**

    {
      Id: "95b1af59-67e6-4e99-8113-65cb603b9721",    // 唯一标识
      Name: "this is a string",    // 名称
      StartedAt: "2022-07-29T12:13:49.789Z",    // 执行开始时间
      FinishedAt: "2022-07-29T12:13:49.789Z",    // 执行结束时间
      DepartmentId: "bc2779c4-a655-42a8-ae7b-f9f5b7a5ed35",    // 部门id
      CompanyId: "f626412f-dfc0-4a11-bc40-9e53bb02a601",    // 公司id
      CreatedAt: "2022-07-29T12:13:49.789Z",    // 创建时间
      CreatedBy: "a3be2e74-37e4-4d65-a931-1427555a9e78",    // 创建人id
      CreatedByName: "this is a string",    // 创建人名称
      ModifiedAt: "2022-07-29T12:13:49.789Z",    // 更新时间
      ModifiedBy: "a66eaada-d7b2-4077-9ec1-2406d0eba099",    // 更新人id
      ModifiedByName: "this is a string",    // 更新人名称
      JobStartupType: ,    // 启动方式
      JobStartupId: "cecade63-9369-4428-9ce9-748096bf4660",    // 启动方式id，例如定时器id，或任务队列id
      JobStartupName: "this is a string",    // 启动方式名称,例如定时器名称，或任务队列名称
      OwnerId: "0fb16b20-18b7-4a37-bdf3-b24df1adca42",    // 记录所属对象id，例如流程部署Id
      Jobs: [
        {
          Id: "ad3e31ac-8980-43a0-9266-bdecfb022f3f",    // 唯一标识
          WorkflowId: "148eeb2b-9938-4029-ae93-009a265df2d0",    // 流程部署id
          Name: "this is a string",    // 名称
          Description: "this is a string",    // 备注
          PackageId: "af65447f-8a68-4f65-8526-da6246ea39d5",    // 流程包id
          PackageName: "this is a string",    // 流程包名称
          PackageVersion: "this is a string",    // 流程包版本号
          PackageVersionId: "bcd6c134-1eca-493e-b69f-c3d2c060cd3d",    // 流程包版本id
          Arguments: [
            {
              Name: "this is a string",    // 名称
              Type: "this is a string",    // 参数类型
              Direction: "In",    // 参数方向:In-入参;Out-出参;InOut-出入参
              DefaultValue: "this is a string",    // 参数默认值; 当使用资产（即AssetContent不为null）时，这里为资产id
              AssetContent: {
                Name: "this is a string",    // 名称
                Description: "this is a string",    // 备注
                IsRequiredEncryption: false    // 是否加密
              }    // 使用的资产
            },
            {
              // 略，结构同前一节点
            }
          ],    // 参数
          ContainingQueueId: "b19e7d10-d65a-4ea7-af99-1e6efeb8f423",    // 运行目标机器人组id
          Priority: 2000,    // 优先级，范围:0-5000
          State: "Queued",    // 状态:Queued-等待中;Running-运行中;Failed-失败;Cancelled-已取消;Succeeded-成功;Paused-已暂停
          DisplayState: "Queued",    // 显示状态:Queued-等待中;Running-运行中;Failed-失败;Cancelled-已取消;Succeeded-成功;Paused-已暂停
          VideoRecordMode: "NeverRecord",    // 视频录制模式:NeverRecord-从不录制;ReportOnlyWhenSucceeded-仅成功时上传;ReportOnlyWhenFailed-仅失败时上传;AlwaysRecord-总是录制;AlwaysReport-总是上传
          Message: "this is a string",    // 原因说明
          LastRunInstaceId: "6f5991aa-f2a2-429b-855c-87082f4876fc",    // 最近运行实例id
          LastRobotName: "this is a string",    // 最近运行的机器人名称
          StartedAt: "2022-07-29T12:13:49.790Z",    // 开始运行时间
          FinishedAt: "2022-07-29T12:13:49.790Z",    // 结束运行时间
          RetriedCount: 2,    // 重试计数
          MaxRetryCount: 1,    // 最大重试次数,范围:0-10
          DepartmentId: "9a4f049f-fa1e-479d-890e-7b012b590321",    // 部门id
          CompanyId: "e20bce36-c239-4251-95ed-3cdf0c0f42bf",    // 公司id
          CronTriggerId: "4048caea-1fc6-4716-8262-7e2f359f107b",    // 触发的定时器id,非定时器触发时为null
          JobExecutionPolicy: ,    // 执行策略
          CreatedAt: "2022-07-29T12:13:49.790Z",    // 创建时间
          CreatedBy: "534d71f9-38fa-4813-b93b-b7c2ab8e812f",    // 创建人id
          CreatedByName: "this is a string",    // 创建人名称
          ModifiedAt: "2022-07-29T12:13:49.790Z",    // 更新时间
          ModifiedBy: "ac6dc477-6aab-4fe8-9f23-0745e2de563b",    // 更新人id
          ModifiedByName: "this is a string",    // 更新人名称
          JobStartupType: ,    // 启动方式
          JobStartupId: "75baaaff-04d0-41f9-b524-c1b0f35eedd6",    // 启动方式id，例如定时器id，或任务队列id
          JobStartupName: "this is a string",    // 启动方式名称,例如定时器名称，或任务队列名称
          JobGroupId: "2ef33453-9763-4587-b264-9f21e1db3830",    // 所属任务组id
          SeqNum: 78,    // 执行序号
          Step: "this is a string",    // 步骤编号，用于展示
          JobSubjectId: "4493488f-6e50-4ecd-92e8-1c25fddf8411",    // Job关联体id
          JobSubjectName: "this is a string",    // Job关联体名称
          JobSubjectType: "this is a string"    // Job关联体类型
        },
        {
          // 略，结构同前一节点
        }
      ]    // 任务列表
    }

---


## 示例代码<span id="示例代码"><span>
- [C#代码示例](https://docimages.blob.core.chinacloudapi.cn/images/API/C%23%E7%A4%BA%E4%BE%8B%E4%BB%A3%E7%A0%81.zip)
- [Java代码示例](https://docimages.blob.core.chinacloudapi.cn/images/API/Java%E7%A4%BA%E4%BE%8B%E4%BB%A3%E7%A0%81.zip)
- [Postman代码示例](https://docimages.blob.core.chinacloudapi.cn/images/API/Postman%E7%A4%BA%E4%BE%8B%E4%BB%A3%E7%A0%81.zip)
