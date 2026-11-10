# CKA 命令行实操练习

本仓库收录依据 [Linux Foundation CKA 考纲](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/)编写的原创练习题。题目使用本地 kind、kubectl 和可用的容器运行时搭建环境，模拟按要求操作、排查并验证 Kubernetes 资源的过程。kind 环境与正式考试环境并不完全相同。

## 开始练习

按编号顺序，一次完成一道题：

1. 阅读该题的 `环境准备.md`，使用同目录的 `kind-config.yaml` 和初始配置文件创建或复用 `cka-lab` 集群、部署初始资源。后续题目共用同一集群，无须重复创建。
2. 确认当前 context 为 `kind-cka-lab`，再打开 `题目.md` 开始计时。题面包含目标、操作限制、官方文档链接和验收命令。
3. 独立完成并运行验收命令。需要复盘时，再阅读 `解题思路.md`；考纲依据和资料链接见 `参考资料.md`。
4. 重练前按该题 `环境准备.md` 中的说明重置初始状态。

首次使用请从[第 1 题环境准备](01_恢复Service流量/环境准备.md)开始。需要 `kind` v0.33.0 或更新版本、`kubectl` 和已启动的 Docker、Podman 或 nerdctl 等 kind 支持的运行时。kind 默认自动选择运行时；具体命令见环境准备文档，集群配置见同目录的 `kind-config.yaml`。

## 题目目录

| 题号 | 练习内容 | 建议用时 |
| --- | --- | --- |
| [01](01_恢复Service流量/题目.md) | 恢复 Service 流量：排查 Deployment 与 Service | 12 分钟 |
| [02](02_限定审计账号权限/题目.md) | 限定审计账号权限：Role、RoleBinding 与权限验证 | 10 分钟 |
| [03](03_批处理任务专用节点调度/题目.md) | 批处理任务专用节点调度：Indexed Job、节点亲和性与容忍 | 13 分钟 |
| [04](04_本地持久卷与数据保留/题目.md) | 本地持久卷与数据保留：PV、PVC 与节点亲和性 | 15 分钟 |
| [05](05_使用Kustomize部署组件/题目.md) | 使用 Kustomize 部署组件：overlay、镜像与配置生成 | 18 分钟 |
| [06](06_回滚失败的Deployment/题目.md) | 回滚失败的 Deployment：版本历史与滚动更新排障 | 15 分钟 |
| [07](07_排查Pod内DNS解析/题目.md) | 排查 Pod 内 DNS 解析：Service 名称与客户端 DNS 策略 | 18 分钟 |
| [08](08_创建带校验的CRD/题目.md) | 创建带校验的 CRD：结构化 schema、status 与打印列 | 20 分钟 |
| [09](09_轮换不可变应用配置/题目.md) | 轮换不可变应用配置：ConfigMap、Secret 与 projected 卷 | 18 分钟 |
| [10](10_配置Ingress多路径TLS/题目.md) | 配置 Ingress 多路径 TLS：路径优先级、证书与集群内验证 | 22 分钟 |
| [11](11_修复HPA指标链路/题目.md) | 修复 HPA 指标链路：Metrics API、kubelet TLS 与资源请求 | 22 分钟 |
| [12](12_修复控制平面静态Pod/题目.md) | 修复控制平面静态 Pod：节点调试、主机清单与镜像 Pod | 24 分钟 |
| [13](13_修复动态卷延迟绑定/题目.md) | 修复动态卷延迟绑定：StorageClass、StatefulSet 与拓扑感知 | 24 分钟 |

每题按 `环境准备.md`、`题目.md`、`解题思路.md` 和 `参考资料.md` 组织，环境配置另存为可直接使用的文件。仓库编写约定见 [AGENTS.md](AGENTS.md)。
