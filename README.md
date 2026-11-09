# CKA 命令行实操练习

本仓库收录依据 [Linux Foundation CKA 考纲](https://training.linuxfoundation.org/certification/certified-kubernetes-administrator-cka/)编写的原创练习题。题目使用本地 Podman、kind 和 kubectl 搭建环境，模拟按要求操作、排查并验证 Kubernetes 资源的过程。kind 环境与正式考试环境并不完全相同。

## 开始练习

按编号顺序，一次完成一道题：

1. 阅读该题的 `环境准备.md`，使用同目录的 `kind-config.yaml` 和初始配置文件创建或复用 `cka-lab` 集群、部署初始资源。后续题目共用同一集群，无须重复创建。
2. 确认当前 context 为 `kind-cka-lab`，再打开 `题目.md` 开始计时。题面包含目标、操作限制、官方文档链接和验收命令。
3. 独立完成并运行验收命令。需要复盘时，再阅读 `解题思路.md`；考纲依据和资料链接见 `参考资料.md`。
4. 重练前按该题 `环境准备.md` 中的说明重置初始状态。

首次使用请从[第 1 题环境准备](01_恢复Service流量/环境准备.md)开始。需要 `kind` v0.33.0 或更新版本、`kubectl` 和已启动的 Podman；具体命令见环境准备文档，集群配置见同目录的 `kind-config.yaml`。

## 题目目录

| 题号 | 练习内容 | 建议用时 |
| --- | --- | --- |
| [01](01_恢复Service流量/题目.md) | 恢复 Service 流量：排查 Deployment 与 Service | 12 分钟 |
| [02](02_限定审计账号权限/题目.md) | 限定审计账号权限：Role、RoleBinding 与权限验证 | 10 分钟 |
| [03](03_批处理任务专用节点调度/题目.md) | 批处理任务专用节点调度：Indexed Job、节点亲和性与容忍 | 13 分钟 |
| [04](04_本地持久卷与数据保留/题目.md) | 本地持久卷与数据保留：PV、PVC 与节点亲和性 | 15 分钟 |
| [05](05_使用Kustomize部署组件/题目.md) | 使用 Kustomize 部署组件：overlay、镜像与配置生成 | 18 分钟 |

每题按 `环境准备.md`、`题目.md`、`解题思路.md` 和 `参考资料.md` 组织，环境配置另存为可直接使用的文件。仓库编写约定见 [AGENTS.md](AGENTS.md)。
