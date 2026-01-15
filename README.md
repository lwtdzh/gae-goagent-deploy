# gae-deploy

自己修改的 gae GoAGent 部署脚本，强化了流量计量能力。
新增了 GAE 退出时保存一次最新流量的功能。新增了保存最新流量时加锁的能力，防止并发更新流量用量时出现不准确的问题。

原始代码来源及使用说明（来自 XX-Net 的 GAE 部署部分）：https://github.com/XX-net/XX-Net/wiki/GAE_Module

=======

前置条件：
1.
已申请 app id

2.
已授予 cloud build 权限：
打开cloud build的权限，并将"App Engine"后面改成ENABLED
https://console.cloud.google.com/cloud-build/settings/service-account

3.
IAM 管理中已授予 Storage Admin 权限

=======

执行步骤：
1.
下载gcloud sdk，安装
https://cloud.google.com/sdk/docs/install

2.
cd 到这个项目的根目录

3.
执行 gcloud init
例如：xxx/google-cloud-sdk/bin/gcloud init
登录google账号，然后选择当前项目

4.
执行 gcloud app deploy
例如：xxx/google-cloud-sdk/bin/gcloud app deploy

=======

检查部署结果：
1.
用已经翻墙的浏览器，访问 https://$appid.appspot.com 看到
GoAgent 服务端已经升级到 python3 版本。
Version: 4.0.0