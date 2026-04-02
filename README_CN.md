[English](README.md)

# Zhuang Liu Lab Wiki @Princeton


## 论文写作与 Rebuttal

**[Paper writing requirements](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0)**（必须通过）。开始写论文时就读这份文档，不要拖到最后。争取在投稿截止日前至少 5 天拿出一份通过所有要求的完整 draft。arXiv 发布前同样适用。

| 资源 | 链接 |
|------|------|
| Paper writing requirements | [Google Doc](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0) |
| arXiv LaTeX 模板 | [Overleaf](https://www.overleaf.com/read/hvyxmdbzzfhp) |
| Rebuttal guide | [Google Doc](https://docs.google.com/document/d/1OutETpGNG7lvUQwC--z8ia4exMqzEIe1dmdfZNtWNes/edit?usp=sharing) |
| 图表制作指南 | [GitHub](https://github.com/zlab-princeton-internal/figure-guide) |


## 实习生 / 短期成员须知

- **入职**：联系 Taiming 获取 Slack、netID 和集群权限。
- **全职投入**：实习是全职岗位。如果有其他 research project，请及时汇报。
- **GitHub & Overleaf**：实习开始时联系 Taiming 在 [zlab-princeton](https://github.com/zlab-princeton) 下创建 GitHub repo，并创建 Overleaf 项目（Princeton 有高级许可证），方便协作。
- **项目完成标准**：项目只有在公开发布（论文 + 代码/数据上 GitHub）后才算完成，不是投完稿就结束。请从第一天就记住这一点。


## 工具

| 工具 | 描述 | 备注 |
|------|------|------|
| [Overleaf-Dropbox 同步][ol] | 本地编辑、上传图片、Claude Code 访问、备份 | **强烈推荐**。需要安装 [Dropbox 桌面客户端](https://www.dropbox.com/install) |
| [Spokenly](https://spokenly.app/) | 语音转文字，用于 coding 和写作 | **强烈推荐** |
| [Notion AI 会议记录][no] | 自动转录视频会议 | 在设置中选择正确的语言 |
| [Dropbox Business][db] | 云存储和同步 | Princeton 免费提供 |
| [Grammarly](https://app.grammarly.com/) | 语法检查 | 使用浏览器插件配合 Overleaf |
| [GPTZero](https://gptzero.me/) | AI 内容检测 | |

[ol]: https://www.overleaf.com/learn/how-to/Dropbox_Synchronization
[no]: https://www.notion.com/product/ai-meeting-notes
[db]: https://csguide.cs.princeton.edu/software/dropbox


## 计算资源

### 集群手册

所有集群手册在一个 repo 中：[zlab-princeton-internal/cluster-guide](https://github.com/zlab-princeton-internal/cluster-guide)

| 集群 | 实验室手册 | 官方指南 | 备注 |
|------|-----------|----------|------|
| Neuronic | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/neuronic) | [website](https://clusters.cs.princeton.edu/) | L40 GPUs |
| Della (A100) | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/della) | [website](https://researchcomputing.princeton.edu/systems/della) | 所有人可用 |
| Della (H200, AI Lab) | 同上 | 同上 | 需要申请 |
| Della (H100, PLI) | 同上 | 同上 | 需要申请（64+ GPUs）。[PLI 信息](https://zinc-scale-b3f.notion.site/The-Della-cluster-and-the-PLI-partition-a3526cf557334124903964a3fa529f68?pvs=4) |
| TPU | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/tpu) | | **强烈建议** |

**TPU**：我们有相当于数千 GPU 的 TPU 算力。缺点是 TPU 需要 JAX，生态不如 PyTorch。但一旦跑通，你能获得的算力是巨大的。如果 GPU 资源不够用，强烈考虑 TPU。与 Zhuang 讨论。

### 计算资源申请

- [AI Lab H200 GPU 申请](https://docs.google.com/forms/d/e/1FAIpQLSd8eV4eALnjGwwkjGbv4cgUbftmmiFcZVkAttg6VppuvmbVDA/viewform)
- [PLI 大任务申请（64+ GPUs）](https://docs.google.com/forms/d/e/1FAIpQLSd4uZWebGZrQcZX2kKm38v6vBcYPfYGF_0BynA3uzjt_8V0Qg/viewform)

实习生/短期成员：提交申请前请先与 senior student 或 postdoc 讨论。

### Della 存储

存储空间有限，只保留必要的数据。长期不用但不想删的数据可以移到 Tiger data。

如果超出配额，需要在 [存储记账表](https://docs.google.com/spreadsheets/d/18QooTF_YxISmnmQsf6-o6L64_6cvGer76Km3yMhBfA0/edit) 中说明用途，可能会面临更严格的限制。

### API 访问

使用 API 之前，确保你的 benchmark 和 evaluation pipeline 已经定稿。

1. 首先使用 [Princeton AI Sandbox](https://princeton.service-now.com/service?id=kb_article&sys_id=KB0014337)（每人每月 $250 免费额度，支持 OpenAI、Gemini、Llama、Mistral）。联系 Taiming（[taiminglu@princeton.edu](mailto:taiminglu@princeton.edu) 或 Slack）设置。
2. 如果不够，联系 Zhuang 获取额外的 API keys。

### 集群问题

1. 在对应的 Slack 频道提问（#neuronic-users / #della-users / #tpu-users）。
2. 建议：如果问题可能反复出现，在 [cluster-guide](https://github.com/zlab-princeton-internal/cluster-guide) repo 中创建 GitHub issue。


## 实验室账号

联系 Taiming 获取权限。

| 账号 | 链接 | 用途 |
|------|------|------|
| GitHub Organization | [zlab-princeton](https://github.com/zlab-princeton) | 代码/数据发布 |
| Huggingface Organization | [zlab-princeton](https://huggingface.co/zlab-princeton) | 代码/数据发布 |
| GPT-Pro | 实验室共享账号 | 高智能任务 |


## 组会

[组会表格](https://docs.google.com/spreadsheets/d/1ZmoTatluRDaasvbBsAvpknmXuvOjx8f9XQTJhtGV5_o/edit?gid=0) — 报名并上传 slides。


## Claude Code（或其他 Coding Agent）

强烈推荐。[Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) 是一个命令行 AI 助手。

**论文写作设置**：[将 Overleaf 同步到 Dropbox](https://www.overleaf.com/learn/how-to/Dropbox_Synchronization)（需要 [Dropbox 桌面客户端](https://www.dropbox.com/install)），然后在本地 Overleaf 项目文件夹中打开 Claude Code session。这样 Claude Code 就能访问你所有的 .tex 文件和图片。

论文写作的高杠杆用法：

1. 让它对照 [writing requirements](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0) 检查你的论文，采纳有用的建议。
2. 让它以 critical reviewer 的角度给你的 draft 反馈。
3. 搜索可能遗漏的 related work，尤其是最近的论文。尽早做这件事，避免重复已有工作。
4. 让它帮你构思更 exciting 和 simple 的 story（要有结果支撑），并生成候选的 title 和 abstract。
5. 迭代图表、abstract 或 title 时，让它同时提出多个方案并排展示（如 3-4 个只有细微差异的变体），一眼就能比较，大幅加速迭代。
6. 每次针对一个 section，让它按重要性列出最大的弱点（一个 prompt 只问一个 section）。每个 section 都这样过一遍。它可能会漏掉一些细节，但通常能抓到几个真正的问题——清晰度问题、逻辑漏洞、缺失的 context。合理的就采纳。这是请人给反馈前的最基本步骤，不要拖到最后一天。

**务必验证 Claude Code 的输出。** 默认将其结果视为可能的 hallucination。仔细 review AI 生成的代码和实验结果。


## Slack

我们的 workspace：**zhuanglabatprinceton.slack.com**

| 频道 | 用途 |
|------|------|
| #sharing-asking | 分享有趣的东西或提问 |
| #neuronic-users | Neuronic 集群讨论 |
| #della-users | Della 集群讨论 |
| #tpu-users | TPU 集群讨论 |

长期成员（PhD/postdoc/MSE）还请加入以下 Princeton Slack workspace：
- [AI Lab @ Princeton](https://ailab-princeton.slack.com)
- [PrincetonCSGrad](https://gradslack.cs.princeton.edu/)


## 邮件组

| 邮件组 | 成员 |
|--------|------|
| [zl-lab@googlegroups.com](mailto:zl-lab@googlegroups.com) | 博士生和博后 |
| [zl-lab-interns@googlegroups.com](mailto:zl-lab-interns@googlegroups.com) | 实习生 |


## Mailing Lists

订阅以了解 Princeton 的讲座和活动：

- [AI-Lab](https://mailchi.mp/0b913cfd021d/princeton-ai-lab-mailing-list)（最相关）
  - 注册页面也可以勾选订阅 PLI 和其他 initiatives。
- [PiXL talks](https://lists.cs.princeton.edu/mailman3/lists/pixl-talks@lists.cs.princeton.edu/)
- [SAIL (Systems for AI Lab)](https://lists.cs.princeton.edu/mailman3/lists/sail@lists.cs.princeton.edu/)
- [Algorithms/ML Reading Group](https://lists.cs.princeton.edu/mailman3/lists/alg-ml-reading-group@lists.cs.princeton.edu/)
- [Princeton Robotics Seminar](https://robotics.princeton.edu/seminar)
