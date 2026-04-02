[中文版](README_CN.md)

# Zhuang Liu Lab Wiki @Princeton


## Paper Writing & Rebuttal

**[Paper writing requirements](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0)** (must pass). Read this when you start writing your paper, not at the end. Aim to have a complete draft that passes all requirements at least 5 days before the submission deadline. This also applies before arXiv release.

| Resource | Link |
|----------|------|
| Paper writing requirements | [Google Doc](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0) |
| LaTeX template for arXiv | [Overleaf](https://www.overleaf.com/read/hvyxmdbzzfhp) |
| Rebuttal guide | [Google Doc](https://docs.google.com/document/d/1OutETpGNG7lvUQwC--z8ia4exMqzEIe1dmdfZNtWNes/edit?usp=sharing) |
| Figure & table guide | [GitHub](https://github.com/zlab-princeton-internal/figure-guide) |


## Intern / Short-term Member Guidelines

- **Onboarding**: Contact Taiming for Slack, netID, and cluster access.
- **Full-time commitment**: Internships are full-time positions. If you have outside research projects, report them promptly.
- **GitHub & Overleaf**: At the start of your internship, contact Taiming to create a GitHub repo (under [zlab-princeton](https://github.com/zlab-princeton)) and an Overleaf project (Princeton has a premium license) for easy collaboration.
- **Project completion**: A project is only considered complete after public release (paper + code/data on GitHub), not just conference submission. Please keep this in mind from day one.


## Tools

| Tool | Description | Note |
|------|-------------|------|
| [Overleaf-Dropbox sync][ol] | Local editing, figure upload, Claude Code access, backup | **Strongly recommended**. Requires [Dropbox desktop client](https://www.dropbox.com/install) |
| [Spokenly](https://spokenly.app/) | Voice-to-text prompting for coding and writing | **Strongly recommended** |
| [Notion AI meeting notes][no] | Auto-transcribe video meetings | Set correct language in settings |
| [Dropbox Business][db] | Cloud storage and sync | Free via Princeton |
| [Grammarly](https://app.grammarly.com/) | Grammar checking | Use browser plugin for Overleaf |
| [GPTZero](https://gptzero.me/) | AI content detection | |

[ol]: https://www.overleaf.com/learn/how-to/Dropbox_Synchronization
[no]: https://www.notion.com/product/ai-meeting-notes
[db]: https://csguide.cs.princeton.edu/software/dropbox


## Computation Resources

### Cluster Manuals

All cluster guides are in one repo: [zlab-princeton-internal/cluster-guide](https://github.com/zlab-princeton-internal/cluster-guide)

| Cluster | Lab Guide | Official | Note |
|---------|-----------|----------|------|
| Neuronic | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/neuronic) | [website](https://clusters.cs.princeton.edu/) | L40 GPUs |
| Della (A100) | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/della) | [website](https://researchcomputing.princeton.edu/systems/della) | Available to everyone |
| Della (H200, AI Lab) | same as above | same as above | Requires request |
| Della (H100, PLI) | same as above | same as above | Requires request (64+ GPUs). [PLI info](https://zinc-scale-b3f.notion.site/The-Della-cluster-and-the-PLI-partition-a3526cf557334124903964a3fa529f68?pvs=4) |
| TPU | [guide](https://github.com/zlab-princeton-internal/cluster-guide/tree/main/tpu) | | **Strongly encouraged** |

**TPU**: We have TPU compute equivalent to thousands of GPUs. The tradeoff is that TPUs require JAX, which has a smaller ecosystem than PyTorch. But once you get it working, the compute you unlock is massive. If GPU resources are limiting your project, strongly consider TPUs. Discuss with Zhuang.

### Compute Requests

- [AI Lab H200 GPU request](https://docs.google.com/forms/d/e/1FAIpQLSd8eV4eALnjGwwkjGbv4cgUbftmmiFcZVkAttg6VppuvmbVDA/viewform)
- [PLI large job request (64+ GPUs)](https://docs.google.com/forms/d/e/1FAIpQLSd4uZWebGZrQcZX2kKm38v6vBcYPfYGF_0BynA3uzjt_8V0Qg/viewform)

Interns/short-term members: discuss with a senior student or postdoc before submitting these requests.

### Della Storage

We have a limited total amount of storage. Only keep what you need. For long-term data you don't want to delete, move it to Tiger data.

If you exceed your quota, you must justify your usage in the [storage accounting spreadsheet](https://docs.google.com/spreadsheets/d/18QooTF_YxISmnmQsf6-o6L64_6cvGer76Km3yMhBfA0/edit) and may face stricter limits.

### API Access

Make sure your benchmarks and evaluation pipeline are finalized before spending API credits.

1. Start with the [Princeton AI Sandbox](https://princeton.service-now.com/service?id=kb_article&sys_id=KB0014337) ($250/month free per user, covers OpenAI, Gemini, Llama, Mistral). Contact Taiming ([taiminglu@princeton.edu](mailto:taiminglu@princeton.edu), or Slack) for setup.
2. If that's not enough, contact Zhuang for additional API keys.

### Cluster Issues

1. Ask in the corresponding Slack channel (#neuronic-users / #della-users / #tpu-users).
2. Recommended: create a GitHub issue in the [cluster-guide](https://github.com/zlab-princeton-internal/cluster-guide) repo if the issue might recur.


## Lab Accounts

Contact Taiming for access.

| Account | Link | Purpose |
|---------|------|---------|
| GitHub Organization | [zlab-princeton](https://github.com/zlab-princeton) | Code/data release |
| Huggingface Organization | [zlab-princeton](https://huggingface.co/zlab-princeton) | Code/data release |
| GPT-Pro | Lab shared account | High-intelligence tasks |


## Group Meetings

[Meeting spreadsheet](https://docs.google.com/spreadsheets/d/1ZmoTatluRDaasvbBsAvpknmXuvOjx8f9XQTJhtGV5_o/edit?gid=0) — sign up and upload your slides.


## Claude Code (or Other Coding Agents)

Strongly recommended. [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) is a command-line AI assistant.

**Setup for paper writing**: [Sync your Overleaf to Dropbox](https://www.overleaf.com/learn/how-to/Dropbox_Synchronization) (requires the [Dropbox desktop client](https://www.dropbox.com/install)), then open a Claude Code session in your local Overleaf project folder. This gives Claude Code full access to all your .tex files and figures.

High-leverage uses for paper writing:

1. Check your paper against the [writing requirements](https://docs.google.com/document/d/11c2vt91LjPNHI85lZdMVyQB_NOZnODwIrGlxoLn2W-c/edit?tab=t.0) and adopt useful suggestions.
2. Get critical reviewer-style feedback on your draft.
3. Search for missing related work, especially recent papers. Do this early to avoid duplicating existing work.
4. Ask it to help craft a more exciting and simple story (one that is supported by your results), and generate candidate titles and abstracts.
5. When iterating on figures, abstracts, or titles, ask it to propose multiple options side by side (e.g., 3–4 variants with small differences). This lets you compare at a glance and speeds up iteration dramatically.
6. Ask it to list the biggest weaknesses of one section at a time, ranked by importance. Do this for each section separately (one prompt per section). It may miss details, but it will usually catch a few real issues — clarity problems, logical gaps, or missing context. Adopt what makes sense. This is a minimal step you should do before asking for human feedback, not something to leave until the last day.

**Always verify Claude Code's output.** Treat its results as hallucination candidates by default. Review AI-generated code and experimental results carefully.


## Slack

Our workspace: **zhuanglabatprinceton.slack.com**.

| Channel | Purpose |
|---------|---------|
| #sharing-asking | Share interesting stuff or ask questions |
| #neuronic-users | Neuronic cluster discussion |
| #della-users | Della cluster discussion |
| #tpu-users | TPU cluster discussion |

For long-term members (PhD/postdoc/MSE), also join these Princeton Slack workspaces:
- [AI Lab @ Princeton](https://ailab-princeton.slack.com)
- [PrincetonCSGrad](https://gradslack.cs.princeton.edu/)


## Email Groups

| Group | Members |
|-------|---------|
| [zl-lab@googlegroups.com](mailto:zl-lab@googlegroups.com) | Graduate students and Postdocs |
| [zl-lab-interns@googlegroups.com](mailto:zl-lab-interns@googlegroups.com) | Interns |


## Mailing Lists

Subscribe to stay informed about talks and events across Princeton:

- [AI-Lab](https://mailchi.mp/0b913cfd021d/princeton-ai-lab-mailing-list) (most relevant)
  - The sign-up page also lets you subscribe to PLI and other initiatives via checkboxes.
- [PiXL talks](https://lists.cs.princeton.edu/mailman3/lists/pixl-talks@lists.cs.princeton.edu/)
- [SAIL (Systems for AI Lab)](https://lists.cs.princeton.edu/mailman3/lists/sail@lists.cs.princeton.edu/)
- [Algorithms/ML Reading Group](https://lists.cs.princeton.edu/mailman3/lists/alg-ml-reading-group@lists.cs.princeton.edu/)
- [Princeton Robotics Seminar](https://robotics.princeton.edu/seminar)
