
> 注：当前项目为 Serverless Devs 应用，由于应用中会存在需要初始化才可运行的变量（例如应用部署地区、函数名等等），所以**不推荐**直接 Clone 本仓库到本地进行部署或直接复制 s.yaml 使用，**强烈推荐**通过 `s init ${模版名称}` 的方法或应用中心进行初始化，详情可参考[部署 & 体验](#部署--体验) 。

# sync-oss-bucket 帮助文档
<p align="center" class="flex justify-center">
    <a href="https://www.serverless-devs.com" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=sync-oss-bucket&type=packageType">
  </a>
  <a href="http://www.devsapp.cn/details.html?name=sync-oss-bucket" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=sync-oss-bucket&type=packageVersion">
  </a>
  <a href="http://www.devsapp.cn/details.html?name=sync-oss-bucket" class="ml-1">
    <img src="http://editor.devsapp.cn/icon?package=sync-oss-bucket&type=packageDownload">
  </a>
</p>

<description>

通过该模版，您可以将一个 OSS Bucket 中的内容同步到另一个 OSS Bucket。

</description>

<codeUrl>



</codeUrl>
<preview>



</preview>


## 前期准备

使用该项目，您需要有开通以下服务并拥有对应权限：

<service>
</service>

<remark>



</remark>

<disclaimers>



</disclaimers>

## 部署 & 体验

<appcenter>
   
- :fire: 通过 [Serverless 应用中心](https://fcnext.console.aliyun.com/applications/create?template=sync-oss-bucket) ，
  [![Deploy with Severless Devs](https://img.alicdn.com/imgextra/i1/O1CN01w5RFbX1v45s8TIXPz_!!6000000006118-55-tps-95-28.svg)](https://fcnext.console.aliyun.com/applications/create?template=sync-oss-bucket) 该应用。
   
</appcenter>
<deploy>
    
- 通过 [Serverless Devs Cli](https://www.serverless-devs.com/serverless-devs/install) 进行部署：
  - [安装 Serverless Devs Cli 开发者工具](https://www.serverless-devs.com/serverless-devs/install) ，并进行[授权信息配置](https://docs.serverless-devs.com/fc/config) ；
  - 初始化项目：`s init sync-oss-bucket -d sync-oss-bucket`
  - 进入项目，并进行项目部署：`cd sync-oss-bucket && s deploy -y`
   
</deploy>

## 案例介绍

<appdetail id="flushContent">

通过该模版，您可以将一个 OSS Bucket 中的内容同步到另一个 OSS Bucket。

</appdetail>

## 使用文档

<usedetail id="flushContent">

您需要选择源 OSS Bucket 和 目标 OSS Bucket。创建完成后，您可以通过 SDK / API 或 控制台调用 Manager 函数，或者为函数添加触发器。

Manger 函数将列取源 Bucket 中的全部 Object，并通过 FC 异步调用将 Object 的信息传递给 Worker 函数。Worker 函数启动后会在目标 Bucket 中查找 Object，如果 Object 不存在或者 Object 的 etag 值与源 Object 不同时将进行同步。

</usedetail>

## 注意事项

<matters id="flushContent">
</matters>


<devgroup>


## 开发者社区

您如果有关于错误的反馈或者未来的期待，您可以在 [Serverless Devs repo Issues](https://github.com/serverless-devs/serverless-devs/issues) 中进行反馈和交流。如果您想要加入我们的讨论组或者了解 FC 组件的最新动态，您可以通过以下渠道进行：

<p align="center">  

| <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407298906_20211028074819117230.png" width="130px" > | <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407044136_20211028074404326599.png" width="130px" > | <img src="https://serverless-article-picture.oss-cn-hangzhou.aliyuncs.com/1635407252200_20211028074732517533.png" width="130px" > |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| <center>微信公众号：`serverless`</center>                                                                                         | <center>微信小助手：`xiaojiangwh`</center>                                                                                        | <center>钉钉交流群：`33947367`</center>                                                                                           |
</p>
</devgroup>
