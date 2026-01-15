# gae-deploy

自己修改的 gae GoAGent 部署脚本，强化了流量计量能力。
新增了 GAE 退出时保存一次最新流量的功能。新增了保存最新流量时加锁的能力，防止并发更新流量用量时出现不准确的问题。

原始代码来源及使用说明（来自 XX-Net 的 GAE 部署部分）：https://github.com/XX-net/XX-Net/wiki/GAE_Module

