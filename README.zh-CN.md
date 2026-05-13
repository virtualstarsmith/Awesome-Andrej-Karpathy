# Awesome Andrej Karpathy [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[⬆️ Back to English](./README.md)
**Language / 语言**：[English](./README.md) · [简体中文 / Chinese](#关于-andrej-karpathy)
> 一份精选地图：Andrej Karpathy 的开源遗产以及在他思想之上构建的 200+ 社区项目 —— 从 `micrograd` 到 `LLM Wiki`，从 `Software 2.0` 到 `Vibe Coding`。
> **注**：这是一份遵循 `awesome-*` 惯例的精选列表。

## 图例
- ⭐ Karpathy 本人维护的官方仓库或 gist
- 🌟 该子派系的事实标准 / 旗舰项目
- 🇨🇳 中文项目
- 📺 视频或演讲
- 📖 博客或文章
- 🪧 X / Twitter 长推（思想种子）
- 🎓 课程或讲座系列
- ⚙️ 框架 / 库
- 📚 awesome 列表 / 精选

## 目录
- [关于 Andrej Karpathy](#关于-andrej-karpathy)
- [基础仓库](#基础仓库)
  - [教学原语](#教学原语)
  - [极简 GPT 实现](#极简-gpt-实现)
  - [全栈 ChatGPT 速通](#全栈-chatgpt-速通)
  - [拒绝 PyTorch 的必然性](#拒绝-pytorch-的必然性)
  - [单文件推理](#单文件推理)
  - [从零写分词器](#从零写分词器)
  - [RNN 时代](#rnn-时代)
  - [浏览器深度学习](#浏览器深度学习)
  - [强化学习入门](#强化学习入门)
- [概念与宣言](#概念与宣言)
- [社区同人项目](#社区同人项目)
  - [LLM Wiki](#llm-wiki)
  - [`CLAUDE.md` / Karpathy Skills](#claudemd-karpathy-skills)
  - [AutoResearch](#autoresearch)
  - [NanoGPT speedrun](#nanogpt-speedrun)
  - [Recipe for Training NN](#recipe-for-training-nn)
  - [LLM OS](#llm-os)
  - [Vibe Coding](#vibe-coding)
  - [Pong from Pixels 复现](#pong-from-pixels-复现)
  - [nn-zero-to-hero 配套教材](#nn-zero-to-hero-配套教材)
  - [nanochat 复现](#nanochat-复现)
  - [LLM Council 衍生](#llm-council-衍生)
  - [reader3 衍生](#reader3-衍生)
  - [多语言移植 (microgpt / minbpe / llm.c / llama2.c)](#多语言移植)
  - [GPT 极简衍生与跨模态](#gpt-极简衍生与跨模态)
  - [Graphify / 原始文件夹优先派](#graphify--原始文件夹优先派)
  - [Agentic Engineering](#agentic-engineering)
  - [HN Time Capsule](#hn-time-capsule)
  - [AI 职业暴露](#ai-职业暴露)
  - [Idea File 元标准](#idea-file-元标准)
  - [微型种子](#微型种子)
  - [概念引文层](#概念引文层)
- [演讲与文章](#演讲与文章)
- [时间线 2015 → 2026](#时间线-2015--2026)
- [相关 Awesome Lists](#相关-awesome-lists)
- [贡献指南](#贡献指南)
- [免责声明](#免责声明)
- [许可](#许可)

## 关于 Andrej Karpathy
**Andrej Karpathy** 是少数几位「持续交付 *并且* 持续讲解」的研究者：把复杂系统剥到算法核心，再把代码与课程一并公开。OpenAI 创始成员（2015–2017，2023–2024）、特斯拉前 AI 高级总监（Autopilot 视觉栈，2017–2022）、斯坦福 CS231n 联合讲师、李飞飞门下博士。2024 年创办 [Eureka Labs](http://eurekalabs.ai)，一所 AI 原生学校。
- 🏠 [karpathy.ai](http://karpathy.ai)
- 🐙 [github.com/karpathy](http://github.com/karpathy)
- 🐦 [x.com/karpathy](http://x.com/karpathy)
- 🎓 [Neural Networks: Zero to Hero](http://karpathy.ai/zero-to-hero.html)
---

## 基础仓库
### 教学原语
- ⭐ [karpathy/micrograd](https://github.com/karpathy/micrograd) - ~100 行自动求导 + ~50 行神经网络，PyTorch 风格 API。Zero-to-Hero 第 1 课配套代码。
- ⭐ [karpathy/makemore](https://github.com/karpathy/makemore) - 字符级语言模型，分 5 个阶段从 bigram → MLP → RNN → Transformer 一路演进。
- ⭐ [karpathy/nn-zero-to-hero](https://github.com/karpathy/nn-zero-to-hero) - Zero-to-Hero 全部讲座的官方 notebook 合集。
### 极简 GPT 实现
- ⭐ [karpathy/minGPT](https://github.com/karpathy/minGPT) - ~300 行 PyTorch GPT，附带教学级加法演示（99.9% 准确率）。
- ⭐ [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) - 训练/微调中等规模 GPT 最简单、最快的仓库（★57K+）。
### 全栈 ChatGPT 速通
- ⭐ [karpathy/nanochat](https://github.com/karpathy/nanochat) - 「\$100 能买到的最好 ChatGPT」：单机全栈训练 + 聊天 UI，约 8000 行手写代码。
- ⭐ [karpathy/microgpt](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95) - 200 行零依赖纯 Python：数据集、分词器、自动求导、GPT、Adam、训练、推理一应俱全。
- ⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch) - 630 行单 GPU 训练核心，让智能体自行编辑 `program.md` 并跑 5 分钟级实验闭环（★66K+，9.6K fork）。
- ⭐ [karpathy/llm-council](https://github.com/karpathy/llm-council) - 多 LLM「议会」：并行回答、互相打分、由「主席 LLM」综合最终回复。
- ⭐ [karpathy/reader3](https://github.com/karpathy/reader3) - 专为「让 LLM 陪你读书」打造的 EPUB 章节阅读器。两天破 1.5K★。
- ⭐ [karpathy/KarpathyTalk](https://github.com/karpathy/KarpathyTalk)（2026/04） - 围绕演讲构建的「构建者 + 智能体共享平台」实验项目。
### 拒绝 PyTorch 的必然性
- ⭐ [karpathy/llm.c](https://github.com/karpathy/llm.c) - 纯 C / CUDA 训练 GPT-2/3，附 ~1000 行 CPU 参考实现。Karpathy 明确鼓励将各种语言移植放在外部仓库。
### 单文件推理
- ⭐ [karpathy/llama2.c](https://github.com/karpathy/llama2.c) - 单文件 C 推理 Llama 2，附 PyTorch 训练脚本。**Karpathy 仓库中多语言移植最多的一个**。
### 从零写分词器
- ⭐ [karpathy/minbpe](https://github.com/karpathy/minbpe) - 三段式教学实现（Basic / Regex / GPT4 三种分词器），与 *Let's build the GPT Tokenizer* 视频配套。
### RNN 时代
- ⭐ [karpathy/char-rnn](https://github.com/karpathy/char-rnn) - 当年那个 Torch/Lua 多层 RNN/LSTM/GRU 字符级语言模型，*Unreasonable Effectiveness of RNNs* 一文的代码后盾。
- ⭐ [karpathy/min-char-rnn](https://gist.github.com/karpathy/d4dee566867f8291f086) - 100 行纯 NumPy 的 vanilla RNN（★4K+）。
### 浏览器深度学习
- ⭐ [karpathy/convnetjs](https://github.com/karpathy/convnetjs) - JS 实现的 CNN/RL 训练库；很多人第一次「亲眼看到」反向传播就在这里。
- ⭐ [karpathy/reinforcejs](https://github.com/karpathy/reinforcejs) - DP / SARSA / Q-learning / DQN / Policy Gradient 的 JS 实现，全部带 Web 演示。
### 强化学习入门
- ⭐ [karpathy/pg-pong](https://gist.github.com/karpathy/a4166c7fe253700972fcbc77e4ea32c5) - 130 行 NumPy 策略梯度智能体玩 ATARI Pong，《Pong from Pixels》一文的代码配套。
---

## 概念与宣言
> 下面 [社区同人项目](#社区同人项目) 中所有内容的「思想种子」。
- 📖 [Software 2.0](https://karpathy.medium.com/software-2-0-a64152b37c35)（2017） - 「神经网络是一种新的代码，权重就是程序。」
- 📺 [Software is Changing (Again)](https://www.ycombinator.com/library/MW-andrej-karpathy-software-is-changing-again)（YC 2025） - 英语就是新的编程语言；Software 3.0 吞食 1.0/2.0。[逐字稿注释](https://www.latent.space/p/s3)。
- 📺 [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) + 🪧 [LLM OS 推](https://x.com/karpathy/status/1723140519554105733)（2023/11） - LLM 是 CPU、上下文是 RAM、向量库是文件系统、工具是外设。
- 🪧 [Vibe coding 推](https://x.com/karpathy/status/1886192184808149383) + 📖 [MenuGen 博客](https://karpathy.bearblog.dev/vibe-coding-menugen/)（2025/02） - 「彻底沉浸于氛围，忘掉代码本身的存在。」
- 🪧 [Agentic engineering / `CLAUDE.md` 系列](https://x.com/karpathy)（2025/12 → 2026/01） - `CLAUDE.md` 是新的 system prompt；*skills* 是新的函数库。
- ⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch)（2026/03） - Software 3.0 应用于科研：智能体改写 `program.md`、跑实验、再迭代。
- 🪧 [LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)（2026/04） - 预先编译的知识库 + LLM 渲染器；一篇反 RAG 宣言。
- 📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/)（2019） - 「先在一个 batch 上过拟合，再谈泛化」的训练 SOP。
- 📖 [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)（2015） - RNN 时代被转发最多的博客；催生了几乎所有语言的 char-rnn 移植。
---

## 社区同人项目
> 每个子小节中收录的项目，其 README/About 都明确引用了某个 Karpathy 仓库、文章或推文。星标和 fork 数量变化很快，发布前请再次核对。
### LLM Wiki
> 思想种子：🪧 [LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)（2026/04，仅 gist 本身就有 ★28K+，6188 fork）。本表中体量最大的子生态 —— **30+ 实现，6 种形态**，每个项目都在 README/About 中明确署名 Karpathy。
**Web 应用 / 桌面产品**
- 🌟 [lucasastorian/llmwiki](https://github.com/lucasastorian/llmwiki) - 严格按 gist 规范实现。Web 应用 + MCP + Claude 账号集成，托管于 [llmwiki.app](http://llmwiki.app)。Apache-2.0。
- [nashsu/llm_wiki](https://github.com/nashsu/llm_wiki) - 跨平台桌面应用；Obsidian 兼容存储，明确「反 RAG」框架。
**Claude Code skill / 插件 / Agent Skills**
- [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki) - 兼容 Agent Skills（Claude Code / Cursor / Codex / OpenCode）的封装 skill。
- [kfchou/wiki-skills](https://github.com/kfchou/wiki-skills) - 轻量级 Claude Code skill；持续累积的复利知识库。
- [ussumant/llm-wiki-compiler](https://github.com/ussumant/llm-wiki-compiler) - Claude Code 插件，把 markdown 编译成主题型 wiki。
- [praneybehl/llm-wiki-plugin](https://github.com/praneybehl/llm-wiki-plugin) - Claude Code 插件；与 vanillaflava、OmegaWiki、Synthadoc 互相交叉引用。
- [atomicmemory/llm-wiki-compiler](https://github.com/atomicmemory/llm-wiki-compiler) - 命令行知识编译器（「原始素材进，互联 wiki 出」）。
- [micuintus/llm-wiki](https://github.com/micuintus/llm-wiki) - 与具体 agent 解耦的极简 skill；自称「锋利」参考实现。
- [charlie947/ai-second-brain](https://github.com/charlie947/ai-second-brain) - 从 ChatGPT/Claude/research 历史中构建可检索的第二大脑。
- [coleam00/claude-memory-compiler](https://github.com/coleam00/claude-memory-compiler) - 「记忆学派」：把对话历史编译成 wiki。
**Obsidian（追加派 vs 改写派）**
- 🌟 [Ar9av/obsidian-wiki](https://github.com/Ar9av/obsidian-wiki) - Obsidian × 多智能体共享 Wiki Skills 框架；「Obsidian 是阅读器，LLM 是维护者」的代表（★933）。
- 🌟 [eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain) - 「改写学派」代表；31 条命令 + 4 个定时智能体反复重写 vault。
- [NicholasSpisak/second-brain](https://github.com/NicholasSpisak/second-brain) - 经典「原始文件夹 → 编译 wiki → Obsidian 浏览」管线。
- [AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian) - Claude + Obsidian 搭档，配 `/wiki` `/save` `/autoresearch` 斜杠命令。
- [MehmetGoekce/llm-wiki](https://github.com/MehmetGoekce/llm-wiki) - Claude Code + Logseq/Obsidian；L1/L2 缓存式架构。
- [balukosuri/llm-wiki-karpathy](https://github.com/balukosuri/llm-wiki-karpathy) - Cursor / Obsidian 个人 KB 轻量配方。
- [kytmanov/obsidian-llm-wiki-local](https://github.com/kytmanov/obsidian-llm-wiki-local) - 100% 本地、Ollama 驱动的 Obsidian wiki。
- [green-dalii/obsidian-llm-wiki](https://github.com/green-dalii/obsidian-llm-wiki) - Obsidian 插件，支持多页实体/概念生成 + 对话式查询。
- [2233admin/obsidian-llm-wiki](https://github.com/2233admin/obsidian-llm-wiki) - Obsidian 极简 fork。
**多智能体 / 工业级扩展**
- [nvk/llm-wiki](https://github.com/nvk/llm-wiki) - 并行多智能体研究编译器；命题驱动调研 + 工件生成。
- [redmizt/multi-agent-wiki-toolkit](https://github.com/redmizt/multi-agent-wiki-toolkit) - 身份令牌、安全钩子、调度、污染防火墙、主动学习一应俱全。
- [skyllwt/OmegaWiki](https://github.com/skyllwt/OmegaWiki) - 完整科研平台：论文 → 知识图谱 → 缺口检测 → idea 生成 → 实验设计 → 论文写作 → 审稿回复。
- [yologdev/karpathy-llm-wiki](https://github.com/yologdev/karpathy-llm-wiki) - 把 Karpathy 的初始 prompt 喂给 agent 后「自我生长」出来的全栈应用。
- [cablate/llm-atomic-wiki](https://github.com/cablate/llm-atomic-wiki) - 原子化扩展：原子层 + 主题分支 + 双层 lint。
**中文实现**
- 🇨🇳 [zhurudong/andrej-karpathy-llm-wiki](https://github.com/zhurudong/andrej-karpathy-llm-wiki) - gist 中文翻译 + 实现笔记。
- 🇨🇳 [gatelynch/llm-knowledge-base](https://github.com/gatelynch) - 繁体中文实践。
- 🇨🇳 [chengjialu8888/LLM-Wiki-KB](https://github.com/chengjialu8888) - 简体中文实现。
### `CLAUDE.md` / Karpathy Skills
> 思想种子：🪧 Agentic engineering 推文系列（2025/12 → 2026/01）+ 📺 [Sequoia AI Ascent: From Vibe Coding to Agentic Engineering](https://www.youtube.com/watch?v=96jN2OCOfLs)（2026/04）。
- 🌟 [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) - 把 Karpathy 散落在 X 上的观察压缩进一个 `CLAUDE.md`（4 条行为规则）。**★119K**，11.9K fork；本子派系的事实标准。
- [renezander030 / Karpathy-skills `CLAUDE.md` v2 (gist)](https://gist.github.com/renezander030/2898eb5f0100688f4197b5e493e156a2)(https://gist.github.com/renezander030/2898eb5f0100688f4197b5e493e156a2) - 在 forrestchang 基础上扩展为 6 条来自 `fixclaw` 实战的运行时规则；覆盖 prompt 注入与预算护栏。
- [K-Dense-AI/karpathy](https://github.com/K-Dense-AI/karpathy) - 基于 Claude Agent SDK + Google ADK 的 Agentic ML Engineer；「Scientific Agent Skills」框架。
- [Smithbox-ai/ControlFlow](https://github.com/Smithbox-ai/ControlFlow) - 把 Karpathy-skills 思路 fork 成更结构化的 ControlFlow agent。
- [PBNZ/newton-skill](https://github.com/PBNZ/newton-skill) - 从该系列衍生的「牛顿式第一性原理」单 skill。
- 📚 [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - 235 个 Claude skill 的精选清单，源头追溯到 forrestchang。
- [mattpocock/skills](https://github.com/mattpocock/skills) - Matt Pocock 的 TypeScript 风格 skills 合集。
- [karpathy/llm-council · `CLAUDE.md`（官方范本）](https://github.com/karpathy/llm-council/blob/master/CLAUDE.md) - Karpathy 自己仓库里的项目级 `CLAUDE.md`（166 行，LLM Council 的技术备忘）。
### AutoResearch
> 思想种子：⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch)（2026/03）。
**领域迁移**
- [RightNow-AI/autokernel](https://github.com/RightNow-AI/autokernel) - autoresearch 闭环用于 GPU kernel 自动调优。
- [saikatkumardey/autoresearch-tabular](https://github.com/saikatkumardey/autoresearch-tabular) - 表格类 ML 研究 agent。
- [trantrikien239/autoresearch-tabular](https://github.com/trantrikien239/autoresearch-tabular) - 表格方向的另一实现。
- [jhamandeep/autoresearch-tabular-case-study](https://github.com/jhamandeep/autoresearch-tabular-case-study) - 带消融实验的表格案例研究。
- [monk1337/Bio-Autoresearch](https://github.com/monk1337/Bio-Autoresearch) - 生物信息学方向。
- [aiming-lab/AutoResearchClaw](https://github.com/aiming-lab/AutoResearchClaw) - AI 安全 / 红队视角。
- [ArchishmanSengupta/autovoiceevals](https://github.com/ArchishmanSengupta/autovoiceevals) - 语音 eval 自动化。
- [dorringel/epsiclaw](https://github.com/dorringel/epsiclaw) - 运筹学方向。
**多 LLM 后端**
- [ajzhanghk/autoresearch-glm](https://github.com/ajzhanghk/autoresearch-glm) - GLM 后端。
- [supratikpm/autoresearch-gemini](https://github.com/supratikpm) - Gemini CLI 后端。
- [romovpa/Claudini](https://github.com/romovpa/Claudini) - Claude / 多模型混合。
- [Entrpi/autoresearch-everywhere](https://github.com/Entrpi/autoresearch-everywhere) - 跨云闭环。
- [abcdedf/autoresearch-anycloud](https://github.com/abcdedf/autoresearch-anycloud) - 跨厂商闭环。
**Agent 风味改造**
- [hwchase17/autoresearch-agents](https://github.com/hwchase17/autoresearch-agents) - LangChain CTO 的移植：不再优化 ML 训练，而是用 LangSmith eval **自动改进 agent**。
- [uditgoenka/autoresearch](https://github.com/uditgoenka/autoresearch) - 加了一层 `AGENTS.md` 适配，让任意编程 agent 都能驱动这个闭环。
**框架与精选**
- ⚙️ [VectorInstitute/helix](https://github.com/VectorInstitute/helix) + [helix-examples](https://github.com/VectorInstitute/helix-examples) - Vector Institute 的 autoresearch 框架，附可复现的 Karpathy + 推理 TPS 示例。
- ⚙️ [agentsmd/](https://github.com/agentsmd/agents.md)`agents.md` - 开源 `AGENTS.md` 标准（★21K），autoresearch 生态广泛采用。
- 📚 [GitHub topic: karpathy-inspired](https://github.com/topics/karpathy-inspired) - 社区 topic，汇集 autoresearch 式自主改进循环。
- 📚 [WecoAI/awesome-autoresearch](https://github.com/WecoAI/awesome-autoresearch) - 早期合集。
- 📚 [alvinreal/awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch) - 主流 awesome-list（★1.7K）。
- 📚 🇨🇳 [yibie/awesome-autoresearch](https://github.com/yibie/awesome-autoresearch) - 中文精选。
**工业级集成**
- ⚙️ [Red Hat OpenShift AI · autoresearch 集成](https://www.redhat.com/en/blog) - 198 个实验示范，在 OpenShift AI 上跑 autoresearch 闭环。
- 🎓 [Lightning AI · autoresearch 教程平台](https://lightning.ai/) - 把 autoresearch 全流程整合进 Lightning AI 教学。
- [revis · 多 agent autoresearch fork](https://www.reddit.com/r/LocalLLaMA/) - Reddit 上讨论的多 agent 协作 fork。
- Ascend/CANN fork - 华为昇腾 NPU 适配（[Discussion #519](https://github.com/karpathy/autoresearch/issues/519)）。
- Colab/Kaggle T4 fork - 免费 T4 GPU 移植，零成本零本地环境（[Discussion #208](https://github.com/karpathy/autoresearch/issues/208)）。
### NanoGPT speedrun
> 思想种子：⭐ [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) + ⭐ [llm.c](https://github.com/karpathy/llm.c) 训练基线。
- 🌟 [KellerJordan/modded-nanogpt](https://github.com/KellerJordan/modded-nanogpt) - 8×H100 训练时长速通赛，目前 **127.7s**（一年前为 8.2 分钟）。本子派系的标准。
- ⚙️ [KellerJordan/Muon](https://kellerjordan.github.io/posts/muon/) - 衍生优化器；催生了 MARS / SWAN / AdaMuon 等变体。
- [tyler-romero/nanogpt-speedrun](https://github.com/tyler-romero/nanogpt-speedrun) - 在 2×RTX 4090 上复现 modded-nanoGPT，逐步记录每一项收益。
- [alexjc/nanogpt-speedrun](https://github.com/alexjc/nanogpt-speedrun) - 消费级显卡上的 speedrun。
- [VatsaDev/NanoPoor](https://github.com/VatsaDev/NanoPoor) - 「为穷人 T4 准备的 NanoGPT speedrun」 —— Colab T4 / A100 非官方排行榜。
- [cat-state/modded-nanogpt-moe](https://github.com/cat-state/modded-nanogpt-moe) - 在 10.8 分钟纪录处分叉的 MoE 变体。
- [BlinkDL/modded-nanogpt-rwkv](https://github.com/BlinkDL/modded-nanogpt-rwkv) - RWKV 风味 speedrun fork。
- [nikhilvyas/modded-nanogpt-SOAP](https://github.com/nikhilvyas/modded-nanogpt-SOAP) - SOAP 优化器变体。
- [Faster-nanoGPT](https://github.com/Faster-nanoGPT) - 多机 speedrun 实验。
- [Marin Speedrun](https://www.marin.community/) - 工业级 speedrun 排行榜。
- [Prime Intellect leaderboard](https://www.primeintellect.ai/) - 工业级 speedrun 排行榜。
- 📖 [Automated LLM Speedrunning Benchmark](https://openreview.net/) - OpenReview 上把 speedrun 转化为 benchmark 的论文。
### Recipe for Training NN
> 思想种子：📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/)（2019）。
- ⚙️ [BlackHC/neural_net_checklist](https://github.com/BlackHC/neural_net_checklist) - 把 Karpathy 训练 SOP 封装成可调用的 PyPI 库。
- [chicobentojr 的 NN training checklist gist](https://gist.github.com/chicobentojr) - 个人 checklist 实现。
### LLM OS
> 思想种子：🪧 [LLM OS 推](https://x.com/karpathy/status/1723140519554105733)（2023/11）。
- [victor-iyi/llm-os](https://github.com/victor-iyi/llm-os) - 明确标注「灵感来自 Andrej Karpathy」。
- 📚 [bilalonur/awesome-llm-os](https://github.com/bilalonur/awesome-llm-os) - LLM OS 项目、论文与讨论的专题 awesome-list。
- ⚙️ [agno-agi/agno](https://github.com/agno-agi/agno)（前 phidata） - LLMOS Cookbook；商业级 LLM OS 框架。
- ⚙️ [microsoft/JARVIS](https://github.com/microsoft/JARVIS) - 多模型 OS 风格 agent。
- 📖 [agiresearch/AIOS](https://github.com/agiresearch/AIOS) - 罗格斯学术派「LLM Agent OS」。
- ⚙️ [letta-ai/letta](https://github.com/letta-ai/letta)（前 MemGPT） - 面向长上下文的 OS 风格分级记忆。
- 📖 [HuggingFace shivance/illustrated-llm-os](https://huggingface.co/blog/shivance/illustrated-llm-os) - 图解长文。
### Vibe Coding
> 思想种子：🪧 [Vibe coding 推](https://x.com/karpathy/status/1886192184808149383)（2025/02）。
**Awesome 列表**
- 📚 [filipecalegario/awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding) - 工具 / 项目 / 文章；开篇即引用 Karpathy。
- 📚 [taskade/awesome-vibe-coding](https://github.com/taskade/awesome-vibe-coding) - Taskade 精选列表。
- 📚 [ai-for-developers/awesome-vibe-coding](https://github.com/ai-for-developers/awesome-vibe-coding) - 面向开发者的精选。
- 📚 [0xWelt/Awesome-Vibe-Coding](https://github.com/0xWelt/Awesome-Vibe-Coding) - 偏开源工具方向。
- 📚 [levz0r/awesome-vibecoded-apps](https://github.com/levz0r/awesome-vibecoded-apps) - 真正用 vibe coding 做出来的 app 集。
**教程与中文**
- 🎓 [goker/vibe-coding-101](https://github.com/goker/vibe-coding-101) - Vibe Coding 101 课程。
- 🇨🇳 🎓 [datawhalechina/easy-vibe](https://github.com/datawhalechina/easy-vibe) - Datawhale 中文教程。
- 🇨🇳 [EnzeD/vibe-coding](https://github.com/EnzeD/vibe-coding) - 中文集合（★1.3K+）。
- [JasonRobertDestiny/VibeDoc](https://github.com/JasonRobertDestiny/VibeDoc) - Vibe-doc 生成器。
- [DeadWaveWave/demo2apk](https://github.com/DeadWaveWave/demo2apk) - Demo→APK vibe 流水线。
- [cporter202/lovable-for-beginners](https://github.com/cporter202/lovable-for-beginners) - Lovable 新手指南。
- [Zentrun](https://github.com/Zentrun) - 多实验 vibe coding 集合。
### Pong from Pixels 复现
> 思想种子：⭐ [karpathy/pg-pong](https://gist.github.com/karpathy/a4166c7fe253700972fcbc77e4ea32c5) + 📖 [Pong from Pixels](http://karpathy.github.io/2016/05/31/rl/)（2016）。
- 🌟 [omkarv/pong-from-pixels](https://github.com/omkarv/pong-from-pixels) - 注释、修复并扩展为完整 RL 入门课。
- [johnrobinsn/pongfrompixels](https://github.com/johnrobinsn/pongfrompixels) - 现代化为 Python 3 + Tensorboard。
- [gameofdimension/policy-gradient-pong](https://github.com/gameofdimension/policy-gradient-pong) - 明确基于博客的 TensorFlow 实现。
- [omerbsezer/PolicyGradient_PongGame](https://github.com/omerbsezer/PolicyGradient_PongGame) - 变体实现。
- [stewy33/pong-with-policy-gradients](https://github.com/stewy33/pong-with-policy-gradients) - 变体实现。
- [julian-q/policy-gradient](https://github.com/julian-q/policy-gradient) - 在 Pong 上的纯 NumPy 策略梯度。
- [xanderex-sid / pg-pong PyTorch](https://gist.github.com/xanderex-sid/ae6cd3ea0c3759c1e3f92835ebd6e158) - PyTorch CNN/MLP 重写并在 Colab 验证；以原 gist 评论形式发布。
- [washburn125/Atari-Pong](https://github.com/washburn125/Atari-Pong) - 明确基于该文的 OpenAI Gym RL 项目。
- [8bitmp3/NumPy-org-Tutorial-Policy-Gradients-Deep-RL-with-Pong-from-Scratch](https://github.com/8bitmp3/NumPy-org-Tutorial-Policy-Gradients-Deep-RL-with-Pong-from-Scratch) - 官方 NumPy 教程（Google Season of Docs 2020）。
- [mlitb/pong](https://github.com/mlitb/pong) - DQN / DDQN 三人小组学生复现。
- [shehio/Karpathy-Pong](https://github.com/shehio/Karpathy-Pong) - 「一次只跑一种算法」的复现 + 衍生。
- 📖 [Ian McKenzie — Pong from pixels without reading "Pong from Pixels"](https://www.lesswrong.com/posts/ipxmEgNeqFkjJAmx3) - LessWrong 文章，作为对照直接照原 DeepMind DQN 论文实现。
### nn-zero-to-hero 配套教材
> 思想种子：⭐ [karpathy/nn-zero-to-hero](https://github.com/karpathy/nn-zero-to-hero)（★20.3K）+ 🎓 [Zero-to-Hero 系列](http://karpathy.ai/zero-to-hero.html)。
**注释式课堂笔记**
- 🌟 [chizkidd/Karpathy-Neural-Networks-Zero-to-Hero](https://github.com/chizkidd/Karpathy-Neural-Networks-Zero-to-Hero) - 逐课注释 notebook；理想的「第二遍」材料。
- [MK2112/nn-zero-to-hero-notes](https://github.com/MK2112/nn-zero-to-hero-notes) - 覆盖每个视频的详细 Markdown + Jupyter 笔记。
- [ryankillian/karpathy-lectures-workbooks](https://github.com/ryankillian/karpathy-lectures-workbooks) - 配套练习 + Colab 链接。
- [0ssamaak0/Karpathy-Neural-Networks-Zero-to-Hero](https://github.com/0ssamaak0/Karpathy-Neural-Networks-Zero-to-Hero) - 整套讲座完整跑通（micrograd + makemore + minBPE + nanoGPT + GPT2）。
**其他语言改写**
- [Anri-Lombard/micrograd](https://github.com/Anri-Lombard/micrograd) - 逐步改写（Karpathy 在 X 上点过赞）。
- [Anri-Lombard/makemore](https://github.com/Anri-Lombard/makemore) - 同作者的 makemore 改写。
- [shoestringinc/microgradr](https://github.com/shoestringinc/microgradr) - micrograd 的 Rust 改写。
- [shoestringinc/makemore-rs](https://github.com/shoestringinc/makemore-rs) - makemore 的 Rust 改写。
- [danielway/micrograd-rs](https://github.com/danielway/micrograd-rs) - Rust 标量自动求导引擎。
- [msminhas93/ferric-micrograd](https://github.com/msminhas93/ferric-micrograd) - Rust 实现，支持批量反向模式自动求导与完整神经网络。
- [AlphaGit/alpha-micrograd-rust](https://github.com/AlphaGit/alpha-micrograd-rust) - 活跃的 Rust 移植（v0.4.0），附带博客。
- [kfish/micrograd-cpp-2023](https://github.com/kfish/micrograd-cpp-2023) - micrograd 的 C++ 移植，跟随 YouTube 教程节奏。
- [kfish/makemore-cpp-2023](https://github.com/kfish/makemore-cpp-2023) - makemore 的 C++ 移植（ZTH 第 2-5 课）。
- [turingcompl33t/makemore-and-friends](https://github.com/turingcompl33t/makemore-and-friends) - 配套 micrograd + makemore 演示 notebook。
**课程扩展项目**
- [niloydebbarma-code/Learn-nanoGPT](https://github.com/niloydebbarma-code/Learn-nanoGPT) - 面向低端 GPU 学习者的硬件自适应训练配置。
### nanochat 复现
> 思想种子：⭐ [karpathy/nanochat](https://github.com/karpathy/nanochat)（★44K，7.1K fork；当前排行榜纪录 Run 6：1.65h，CORE 0.263，2026-03-14）。
**Apple Silicon / MLX**
- 🌟 [scasella/nanochat-mlx](https://github.com/scasella/nanochat-mlx) - 自包含 MLX 移植；一个 `--depth` 旋钮控制全部参数。完全无 PyTorch。
- [ettrickshepherd/mlx_nanochat](https://github.com/tkwn2080/mlx_nanochat) - 另一份完整 MLX 实现（tokenizer + pretrain + SFT + chat + eval）。
- [vithursant/nanoGPT_mlx](https://github.com/vithursant/nanoGPT_mlx) - 早期 nanoGPT → MLX 移植，奠定基础；M3 Pro 上 Shakespeare 0.37 it/s。
- [zsiegel/mlx-gpt](https://github.com/zsiegel/mlx-gpt) - 跟 Karpathy 视频一起从零写 GPT，M4 Max 30 分钟训练。
- [ediestel/picochat-mlx](https://github.com/ediestel/picochat-mlx) - 极简 Apple Silicon MLX 移植。
**家用机房 / 消费级 GPU**
- 🌟 [matt-langston/nanochat-dgx-spark](https://github.com/matt-langston/nanochat-dgx-spark) - 在 2× Blackwell 桌面 GPU 上跑全流程；62.6h 训练日志中找出 17 个 bug（[discussion #710](https://github.com/karpathy/nanochat/discussions/710)）。
- Trelis nanochat-fork - 4 小时 / \$100 训练 500M 参数 LLM 并附 HuggingFace 推送脚本。
- *Reproducing nanochat in Colab Single GPU* - DeepWiki + Gemini 把 nanochat 压缩到单张 Colab GPU 上（[Reddit](https://www.reddit.com/r/LocalLLaMA/comments/1o76ev6)）。
- [saranormous/supa-beginna-nanochat](https://github.com/karpathy/nanochat/discussions/677) - 在租 GPU 之前先把每个阶段在笔记本上跑一遍。
**邻接 / 更快的极简核心**
- [Entrpi/EEmicroGPT](https://github.com/Entrpi/EEmicroGPT) - 比 microgpt 快约 10×（也列于 autoresearch 一节）。
- [webml-community/nanochat-webgpu](https://huggingface.co/spaces/webml-community/nanochat-webgpu) - Xenova 的 WebGPU 移植；nanochat 模型 100% 在浏览器本地运行，无需服务器。
- [chrisjmccormick / Exploring Nanochat](https://github.com/KellerJordan/modded-nanogpt/discussions/206) - modded-nanogpt 与 nanochat 代码间的交叉笔记。
### LLM Council 衍生
> 思想种子：⭐ [karpathy/llm-council](https://github.com/karpathy/llm-council)（★18.5K，3.6K fork；3 阶段议会：collect → 匿名互评 → Chairman 综合）。
**多 LLM 议会**
- [am-will/llm-council](https://github.com/am-will/llm-council) - 面向 Claude Code 的多 agent 编排；OpenCode/Claude Code/Gemini-CLI/Codex 多种 agent 类型 + judge-merge。
- [hideki5123/multi-agent-council](https://github.com/hideki5123/multi-agent-council) - Claude + OpenAI + Gemini 三轮协议（Independent → Cross Review → Chair Synthesis）。
- [Sentry01/AgentCouncil](https://github.com/Sentry01/AgentCouncil) - 在 GitHub Copilot CLI 之上的协作 / 对抗式多 agent。
- [andrewvaughan/agent-council](https://github.com/andrewvaughan/agent-council) - 13 种 agent 人格横跨 6 个议会；SAST 扫描 + 安全/质量/测试/文档 4 人审议。
- [MrLesk/agents-council](https://github.com/MrLesk/agents-council) - 跨 Claude Code、Codex、Gemini、Cursor 的 agent 会话桥接。
- [danielrosehill/LLM-Council-V3](https://github.com/danielrosehill/LLM-Council-V3) - 加入「context-prompt」分离与 prompt 落地执行。
- KobyStam *LLM Council Plus* - 现代 UI + 设置页 + 多 API + 网络搜索 + Ollama 支持（[视频](https://www.youtube.com/watch?v=HOdyIyccOCE)）。
**Claude Code 技能 / 插件**
- [valorisa/llm-council-skill](https://github.com/valorisa/llm-council-skill) - 把 5 种顾问角色（反派 / 第一性原理 / 扩张派 / 旁观者 / 执行者）封装为 Claude skill。
- [ngmeyer/council-review](https://github.com/topics/llm-council) - Claude Code skill：决策 / 代码 / 计划走 5 顾问议会 + 匿名互评。
- [Zandereins/hydra](https://github.com/topics/llm-council) - 多视角代码审议；深度模式 3 顾问 / 10 agent（Opus + Codex），证据链。
- [valpere/chorus](https://github.com/topics/llm-council) - Claude Code / OpenCode / Gemini CLI / Codex 跨 agent 插件（议会、并行审议、调试模式）。
- [looptroop-ai/LoopTroop](https://github.com/topics/llm-council) - LLM 议会做规划，Ralph 循环兜底，OpenCode worktree 出货。
- [tenfoldmarc/llm-council-skill](https://github.com/tenfoldmarc/llm-council-skill) - 5 顾问角色 Claude Code skill，含匿名互评。
- [gcpdev/llm-council-skill](https://github.com/gcpdev/llm-council-skill) - ChatGPT + Gemini 协作式头脑风暴 Claude Code skill。
- [aiwithremy/claude-skills-llm-council](https://github.com/aiwithremy/claude-skills-llm-council) - 教 Claude 召集 5 顾问辩论并给出裁决。
- [shuntacurosu/llm_council_skill](https://github.com/shuntacurosu/llm_council_skill) - 编排多 LLM 进行互评与主席综合。
- [dair-ai/dair-academy-plugins](https://github.com/dair-ai/dair-academy-plugins) - 基于 Fireworks AI 多阶段审议的 LLM Council skill 插件。
**变体与集成**
- [malik-builds/better-llm-council](https://github.com/malik-builds/better-llm-council) - 改进的打分流水线。
- [YonasValentin/llm-council](https://github.com/YonasValentin/llm-council) - 早期 fork 带 Web UI。
- [sjsreehari/debate-engine](https://github.com/topics/llm-council) - Pro/Con/Judge 三 agent + 记忆 + 不确定性信号；OpenRouter + Ollama。
- [microsoft/hve-core](https://github.com/microsoft/hve-core/issues/1326) - 微软提案：在 hve-core 中加入 LLM Council 编排器（GPT-5.4 / Opus 4.6 / Gemini 3.1 Pro）。
- [sherifkozman/the-llm-council](https://github.com/sherifkozman/the-llm-council) - 把 3 阶段议会模式封装成 Claude Code 框架（collect → 匿名互评 → Chairman 综合）。
- [jacob-bd/llm-council-plus](https://github.com/jacob-bd/llm-council-plus) - 现代 UI fork，支持多 API + 网络搜索 + Ollama。
- 📚 [danielrosehill/Awesome-LLM-Council-Projects](https://github.com/danielrosehill/Awesome-LLM-Council-Projects) - 多模型审议系统精选列表。
### reader3 衍生
> 思想种子：⭐ [karpathy/reader3](https://github.com/karpathy/reader3)（★3.4K，456+ fork；「90% vibe-coded，目的就是演示如何用 LLM 读书」）。
**独立重新实现**
- [yongkangc/llmreader](https://github.com/yongkangc/llmreader) - 在 EPUB 之上加入 PDF 支持；以「LLMReader」为名重新包装。
**原仓库上的 PR（正统 fork）**
- [sharathdoes/reader3](https://github.com/sharathdoes) - ChatGroq LLM 聊天集成 + HTML UI（[PR](https://github.com/karpathy/reader3/pulls)）。
- [jerithlawrence/reader3](https://github.com/jerithlawrence) - 段落 / 章节 / 整章复制按钮。
- [HenokB/reader3](https://github.com/HenokB) - 上下方向键翻页。
- [andrestobelem/reader3](https://github.com/andrestobelem) - 西班牙语翻译 + TAR。
### 多语言移植
> 思想种子：⭐ [microgpt gist](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95) · ⭐ [minbpe](https://github.com/karpathy/minbpe) · ⭐ [llm.c](https://github.com/karpathy/llm.c) · ⭐ [llama2.c](https://github.com/karpathy/llama2.c)。
**microgpt 移植**
- [mplekh/rust-microgpt](https://github.com/mplekh/rust-microgpt) - 单文件 Rust 移植。
- [Entrpi/EEmicroGPT](https://github.com/Entrpi/EEmicroGPT) - 约 10× 提速，同样列于 nanochat 一节。
**minbpe 移植**
- [justinhj/minbpe-cc](https://github.com/justinhj/minbpe-cc) - C++ 移植（训练快 ~50×）。
- [dorjeduck/minbpe.mojo](https://github.com/dorjeduck/minbpe.mojo) - Mojo 移植。
- [kuprel/minbpe-pytorch](https://github.com/kuprel/minbpe-pytorch) - PyTorch / CUDA 加速（~120×）。
- [gnp/minbpe-rs](https://github.com/gnp/minbpe-rs) - Rust 移植。
- [Jaward/mlx-minbpe](https://github.com/Jaward/mlx-minbpe) - 面向 Apple Silicon 的 MLX 移植。
- [minbpe-hs](https://www.reddit.com/r/haskell/comments/1czkpk5/) - Haskell 移植。
- ⚙️ [atsentia/mojo-tokenizer](https://github.com/atsentia/mojo-tokenizer) - 纯 Mojo BPE 分词器；M3 Ultra 上 144M tok/s（比 tiktoken 快 3.1×）。
- ⚙️ [swaits/bpe-tokenizer](https://github.com/swaits/bpe-tokenizer) - Rust BPE 库，含 BPEmb 多语言词表（275 种语言）。
- ⚙️ [sweepai/bpe-qwen](https://github.com/sweepai/bpe-qwen) - 专为 Qwen 优化的 Rust BPE（比 HF tokenizers 快 6× / 12×）。
**llm.c 移植**
- [gevtushenko/llm.c](https://github.com/gevtushenko/llm.c) - CUDA C++ Core Libraries 重写；CUDA MODE 案例研究。
- [GaoYusong/llm.cpp](https://github.com/GaoYusong/llm.cpp) - 自带 `tinytorch` 头文件的 C++ 移植。
- [joshcarp/llm.go](https://github.com/joshcarp/llm.go) - Go 移植。
- [Saimirbaci/llm.zig](https://github.com/Saimirbaci/llm.zig) - Zig 移植。
- [rbitr/llm.f90](https://github.com/rbitr/llm.f90) - Fortran 移植。
- [nietras/Llm.cs](https://github.com/nietras/Llm.cs) - C# 移植；从 Hugging Face 自动下载，克隆即跑。
- [azret/llm.cs](https://github.com/azret/llm.cs) - C# 移植；CPU 已完成，CUDA 开发中。
- [otabuzzman/llm.java](https://github.com/otabuzzman/llm.java) - Java 移植，Stream 并行化 + TornadoVM GPU 加速。
- [otabuzzman/llm.swift](https://github.com/otabuzzman/llm.swift) - llm.c 的 Swift 移植。
**llama2.c 移植**（Karpathy 仓库中移植族最庞大者，作者维护着「notable forks」PR 线程）
- [`srush/llama2.rs`](https://github.com/srush/llama2.rs) - Rust 移植，扩展到 70B + 4-bit GPT-Q 量化、批量 prefill、SIMD。
- [`gaxler/llama2.rs`](https://github.com/gaxler/llama2.rs) - 另一份 Rust 移植。
- [`leo-du/llama2.rs`](https://github.com/leo-du/llama2.rs) - 另一份 Rust 移植。
- [`ademyanchuk/llama2-rs`](https://github.com/ademyanchuk/llama2-rs) - 多文件结构的 Rust 学习改写。
- [`danielgrittner/llama2-rs`](https://github.com/danielgrittner/llama2-rs) - 另一份 Rust 移植。
- [`rhlbhatnagar/llama2.rs`](https://github.com/rhlbhatnagar/llama2.rs) - 基于 llama2.c 15M 模型的极简 Rust 移植。
- [`mukel/llama2.java`](https://github.com/mukel/llama2.java) - Java 单文件移植（Llama 2 7B，1.6 tok/s）。
- [`mukel/llama3.java`](https://github.com/mukel/llama3.java) - 后继 Llama 3 实现，带 `--chat`。
- [`neoremind/llama2.java`](https://github.com/neoremind/llama2.java) - 另一份 Java 移植；fp32 7B 性能与 C 对齐。
- [`cgbur/llama2.zig`](https://github.com/cgbur/llama2.zig) - Zig SIMD ~5× 提速。
- [`thxcode/llm-box`](https://pkg.go.dev/github.com/thxcode/llm-box/port/llama2.c) - Go 移植（`port/llama2.c`）。
- ⚙️ [huggingface/candle](https://github.com/huggingface/candle) - HuggingFace 的 Rust 框架；`candle-llama` 由 llama2.c 演化而来。
### GPT 极简衍生与跨模态
> 思想种子：⭐ [minGPT](https://github.com/karpathy/minGPT) + ⭐ [nanoGPT](https://github.com/karpathy/nanoGPT)。
**纯移植**
- [akanyaani/minGPTF](https://github.com/akanyaani/minGPTF) - minGPT 的 TensorFlow 移植。
- [mgrankin/minGPT](https://github.com/mgrankin/minGPT) - minGPT 的 JAX 移植。
- [pytorch/examples · minGPT-ddp](https://github.com/pytorch/examples/blob/main/distributed/minGPT-ddp/mingpt/model.py) - PyTorch 官方 DDP 教学示例。
- ⚙️ [Lightning-AI/lit-llama](https://github.com/Lightning-AI/lit-llama) - PyTorch Lightning 团队基于 nanoGPT 的训练框架。
- [EleutherAI/nanoGPT-mup](https://github.com/EleutherAI/nanoGPT-mup) - nanoGPT fork，集成 Maximal Update Parameterization（μP）用于超参数缩放。
- ⚙️ [stanford-crfm/levanter](https://github.com/stanford-crfm/levanter) - 基于 JAX 的大模型训练器，明显延续 nanoGPT 血统。
**MoE / 稀疏**
- [wolfecameron/nanoMoE](https://github.com/wolfecameron/nanoMoE) - 在 nanoGPT 上加 MoE 层 + 辅助损失 + 稳定性技巧（[博客](https://cameronrwolfe.substack.com/nano-moe)）。
- [Antlera/nanoGPT-moe](https://github.com/Antlera/nanoGPT-moe) - 一行 `use_moe = True` 即可切换。
- [plugyawn/NanoGPT-MoE](https://github.com/plugyawn/NanoGPT-MoE) - 紧凑字符级 Transformer + MoE + Rotary attention + F-gram 上下文增强。
**跨模态**
- [johnnygreco/midiGPT](https://github.com/johnnygreco/midiGPT) - 把 minGPT 用于 MIDI 音乐生成。
- [deepanwadhwa/nanogpt-Audio](https://github.com/deepanwadhwa/nanogpt-Audio) - nanoGPT 消费 EnCodec 音频 token。
- [sugiv/nanochat-audio](https://blog.sugiv.fyi/nanochat-audio) - 用 Kyutai 神经音频编解码器把 nanochat 扩展为多模态（\$5 成本）。
**逐步复现**
- [EdIzaguirre/ChatGPT-from-Scratch](https://github.com/EdIzaguirre/ChatGPT-from-Scratch) - 在 minGPT 驱动下走读原始 GPT 论文。
---
### Graphify / 原始文件夹优先派
> 思想种子：🪧 [raw/ folder 推文](https://x.com/karpathy/status/2039805659)（2026/04）- 把 LLM Wiki 的输入当作原始文件的图来处理，最后再编译；反 RAG 更进一步。
- 🌟 [safishamsi/graphify](https://github.com/safishamsi/graphify) - 旗舰级图优先编译器，处理原始 markdown 文件夹；**~40K★ in 26 days，450K+ 下载**。
- [lucasrosati/claude-code-memory-setup](https://github.com/lucasrosati/claude-code-memory-setup) - 基于图的 Claude Code 记忆布局；据报在智能体召回上节省 **71.5× token**。
- [amarodeabreu/claude-graph-memory](https://github.com/amarodeabreu/claude-graph-memory) - Claude 端图记忆存储；graphify 的极简伴侣。
- [memory-graph/memory-graph](https://github.com/memory-graph/memory-graph) - 通用 memory-graph 库，被多个 fork 复用。
- 📖 [Medium — LLM Wiki Codes: Graphify](https://medium.com/) - 对比 graphify 与 MindStudio 和 [ai-chain.tw](http://ai-chain.tw) 的配套解读。
### Agentic Engineering
> 思想种子：🪧 [Agentic Engineering 转折推文](https://x.com/karpathy)（2026/02/25）+ 📺 [Sequoia AI Ascent: From Vibe Coding to Agentic Engineering](https://www.youtube.com/watch?v=96jN2OCOfLs)（2026/04）。Vibe Coding 的严谨兄弟——用 spec、eval、skill 和智能体编队替代纯粹的 vibes。
- 📚 [jordimas/awesome-agentic-engineering](https://github.com/jordimas/awesome-agentic-engineering) - Agentic Engineering 工具、演讲与案例的精选列表。
- [software-mansion/agentic-engineering](https://github.com/software-mansion/agentic-engineering) - 生产级 Agentic Engineering 脚手架（skills + evals + safety）。
- 📚 [EthicalML/awesome-agentic-engineering-resources](https://github.com/EthicalML/awesome-agentic-engineering-resources) - Ethical-ML 社区精选。
- [DimitriGeelen/agentic-engineering-framework](https://github.com/DimitriGeelen/agentic-engineering-framework) - AI 编程智能体治理框架；任务追溯、结构化门控、会话连续性。
- [K-Dense-AI/karpathy](https://github.com/K-Dense-AI/karpathy) - Agentic ML Engineer 脚手架（同时收录于 [`CLAUDE.md` / Karpathy Skills](#claudemd-karpathy-skills)）。
### HN Time Capsule
> 思想种子：📖 [Auto-grading decade-old HN](http://karpathy.github.io/)（2025/12/10）+ ⭐ [karpathy/hn-time-capsule](https://github.com/karpathy/hn-time-capsule)。LLM 陪审团对旧预测进行回顾性评分。
- ⭐ [karpathy/hn-time-capsule](https://github.com/karpathy/hn-time-capsule) - 用 LLM 陪审团自动为十年前的 Hacker News 预测打分。
- [knowtrend.ai](http://knowtrend.ai) - 财报电话会议回顾性评分器；HN 帖子明确引用了 Karpathy 模板。
### AI 职业暴露
> 思想种子：🪧 AI 自动化风险表推文（已删除后恢复，2026）+ ⭐ [karpathy/jobs](https://github.com/karpathy/jobs)（[在线版](http://karpathy.ai/jobs)）。按职业的 AI 暴露评分。
- ⭐ [karpathy/jobs](https://github.com/karpathy/jobs) - Karpathy 的按职业自动化风险表；在线版 [karpathy.ai/jobs](http://karpathy.ai/jobs)。
- [JoshKale/jobs](https://github.com/JoshKale/jobs) - 重新发布前捕获的首个公开镜像。
- [0xtreme/aus-jobs](https://github.com/0xtreme/aus-jobs) - 澳大利亚特定 fork，含本地化职业分类。
### Idea File 元标准
> 思想种子：🪧 [`IDEA.md`](https://x.com/karpathy/status/2040470801506541998)[ 推文](https://x.com/karpathy/status/2040470801506541998)（2026/04/04）。每个仓库一份的想法日志，`README.md` 和 `AGENTS.md` 的兄弟文件。
- [pithpusher/IDEA.md](https://github.com/pithpusher/IDEA.md) - `IDEA.md` 的 CC0 标准化提案。
- 📚 [GitHub topic: idea-file](https://github.com/topics/idea-file) - 推文后创建的 topic；收集早期 `IDEA.md` 采用者。
### 微型种子
> 单项目种子集中放置，以免遗失。
- 🪧 [`HELLO.md` gist](https://gist.github.com/karpathy/)（2026/04/21）- "Agent free time" 概念（27★ / 3 forks）。尚无成熟衍生，但讨论热烈。
- [ranton256/microgpt_jl](https://github.com/ranton256/microgpt_jl) - [microgpt gist](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95) 的 Julia 移植。
- 📖 [Deep Neural Nets: 33 years ago](http://karpathy.github.io/2022/03/14/lecun1989/)（2022/03）→ [teaching-on-testbeds/deep-nets-reproducing](https://github.com/teaching-on-testbeds/deep-nets-reproducing) - LeCun 1989 的课堂复现，以及 Chameleon Cloud Trovi 可复现制品。
### 概念引文层
> Karpathy 思想碎片，大多以 README 内引用形式存在，而非衍生出独立子派系。列于此处，以便贡献者不必寻找缺失的子章节。
- 🪧 [The Space of Minds](https://x.com/karpathy)（2025/11/29）- 在 skills/wiki README 中被引用。
- 🪧 Animals vs Ghosts（[Dwarkesh Podcast 2025/10](https://www.dwarkeshpatel.com/)）- 在 agentic-engineering README 中被引用。
- 🪧 Verifiability 推文 - 被 [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) 逐字引用。
- 🪧 [LLM GUI / Generative UI 推文](https://x.com/karpathy/status/1917920257)（2025/04）- 后来被 Google DeepMind 的 Gemini 3 生成式 UI 工作呼应；尚无专属 OSS 派系。
- 📖 Power to the people（2025/04）- 评论密集型种子；无代码项目。
- 📖 2025 LLM Year in Review - 锚点文章；被广泛引用。
- 📄 [arXiv:2601.07573 — A Model of Artificial Jagged Intelligence](https://arxiv.org/abs/2601.07573) - "锯齿状智能"的学术操作化。

## 演讲与文章
### 长篇演讲
- 📺 [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g)（2023/11，1h） - 首次系统化提出 LLM-OS 框架。
- 📺 [State of GPT](https://www.youtube.com/watch?v=bZQun8Y4L2A)（Microsoft Build 2023） - GPT 训练流水线全景。
- 📺 [Software is Changing (Again)](https://www.ycombinator.com/library/MW-andrej-karpathy-software-is-changing-again)（YC AI Startup School 2025） - Software 3.0 论纲。
- 📺 [Let's build GPT: from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY)（2023） - nanoGPT 配套讲座。
- 📺 [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI)（2025，3.5h） - 面向大众的 LLM 深度解析；无需编程经验。
- 📺 [Let's build the GPT Tokenizer](https://www.youtube.com/watch?v=zduSFxRajkE)（2024） - minbpe 配套讲座。
- 📺 [Let's reproduce GPT-2 (124M)](https://www.youtube.com/watch?v=l8pRSuU81PU)（2024，4h） - llm.c 配套讲座。
### 博客文章
- 📖 [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)（2015）
- 📖 [Deep Reinforcement Learning: Pong from Pixels](http://karpathy.github.io/2016/05/31/rl/)（2016）
- 📖 [Software 2.0](https://karpathy.medium.com/software-2-0-a64152b37c35)（2017）
- 📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/)（2019）
- 📖 [Vibe Coding MenuGen](https://karpathy.bearblog.dev/vibe-coding-menugen/)（2025）
- 📖 [2025 LLM Year in Review](https://karpathy.bearblog.dev/year-in-review-2025/)（2025） - 重塑 LLM 发展的六大范式转变。
### 关键推文
- 🪧 [LLM OS](https://x.com/karpathy/status/1723140519554105733)（2023/11）
- 🪧 [Vibe coding](https://x.com/karpathy/status/1886192184808149383)（2025/02）
- 🪧 LLM Wiki / `CLAUDE.md` / AutoResearch 系列（2025/12 → 2026/04） - 见 [@karpathy](https://x.com/karpathy)。
---

## 时间线 2015 → 2026
| 日期 | 事件 | 谱系 |
|---|---|---|
| 2015/05 | The Unreasonable Effectiveness of RNNs | char-rnn |
| 2015/12 | min-char-rnn gist | char-rnn |
| 2016/05 | Pong from Pixels 一文 + pg-pong gist | RL 入门 |
| 2017/11 | Software 2.0 一文 | 世界观 |
| 2019/04 | A Recipe for Training NN | 训练 SOP |
| 2020/08 | minGPT 发布 | GPT 极简 |
| 2022/12 | nanoGPT 发布 | GPT 极简 |
| 2023/02 | Zero-to-Hero 第 1 课（micrograd） | 教育 |
| 2023/04 | llama2.c 发布 | 单文件推理 |
| 2023/11 | Intro to LLMs + LLM OS 推 | LLM OS |
| 2024/02 | minbpe + Tokenizer 视频 | 分词器 |
| 2024/04 | llm.c 公开 | 反 PyTorch 必然性 |
| 2024/06 | 复现 GPT-2 (124M) 4h 视频 | llm.c |
| 2024/07 | Eureka Labs 创办 | AI 原生学校 |
| 2025/02 | Vibe coding 推 + MenuGen | Vibe Coding |
| 2025/06 | YC 「Software is Changing (Again)」演讲 | Software 3.0 |
| 2025/01 | Deep Dive into LLMs like ChatGPT 视频 | 教育 |
| 2025/10 | nanochat 发布 | 全栈 ChatGPT |
| 2025/12 | 2025 LLM Year in Review 博文 | 反思 |
| 2025/12 | 「Never been more behind」反思推 | Agentic Engineering 准备 |
| 2026/01 | Agentic engineering / `CLAUDE.md` 系列 | `CLAUDE.md` |
| 2026/03 | autoresearch + microgpt gist | AutoResearch |
| 2026/04 | LLM Wiki gist + KarpathyTalk + reader3 | LLM Wiki / 阅读 agent |
| 2026/04 | llm-council 发布 | 多模型协作 |
---

## 相关 Awesome Lists
相邻生态中明确出现 Karpathy 思想的列表：
- 📚 [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) - 1000+ agent skills（Claude Code、Codex、Cursor、Gemini CLI…），多数源自 Karpathy 的 `CLAUDE.md` 框架。
- 📚 [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - Claude Code 的 skills、hooks、slash-commands、插件。
- 📚 [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - Claude Skills 精选。
- 📚 [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) - 100+ 专用 Claude Code subagents。
- 📚 [bilalonur/awesome-llm-os](https://github.com/bilalonur/awesome-llm-os) - LLM OS 专题。
- 📚 [filipecalegario/awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding) - Vibe coding 工具 / 项目 / 文章。
- 📚 [alvinreal/awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch) - AutoResearch 专题（★1.7K）。
- 📚 [sindresorhus/awesome](https://github.com/sindresorhus/awesome) - 母列表。
- 📚 [andrew/ultimate-awesome](https://github.com/andrew/ultimate-awesome) - 每日刷新的所有 awesome 列表。
---

## 贡献指南
欢迎贡献。仓库上线后请参考 `CONTRIBUTING.md`，在那之前规则如下：
**收录标准**（A / B / C 满足任意一条）：
- **A — 官方**：由 Karpathy 本人维护或发布。无门槛。
- **B — 直接衍生**：项目自身 README/About 明确写明 *inspired by / port of / based on* 某个 Karpathy 仓库、视频或文章。
- **C — 概念衍生**：项目明确引用 Karpathy 提出的某个具名概念（Software 2.0/3.0、LLM OS、Vibe Coding、LLM Wiki、`CLAUDE.md`、AutoResearch、Recipe for Training NN、Pong from Pixels）并附原始来源链接。
**不收录**：
- 仅在第三方博客或评论里被提及，本身 README 不存在出处的项目。
- 已归档、星标 \< 50 且超过 12 个月无更新的仓库（多语言移植除外）。
- 闭源商业产品，除非它是思想时间线上不可绕过的节点。
**词条格式**：
```javascript
- [author/repo](https://github.com/author/repo) - 一句话描述，以句号结尾。
```
请使用 [图例](#图例) 中的对应前缀 emoji。中文项目加 🇨🇳。多语言移植放在 [多语言移植](#多语言移植)（microgpt / minbpe / llm.c / llama2.c）或 [GPT 极简衍生与跨模态](#gpt-极简衍生与跨模态)（minGPT / nanoGPT）。新派系需要在 [概念与宣言](#概念与宣言) 中有对应思想种子。
**PR 标题**：`Add: author/repo` 或 `Update: author/repo`。
---

## 免责声明
> **警告**：这是一份**精选列表，不是审计报告**。所列项目由各自作者创建并维护。我们不审计、不背书、不保证任何项目的安全性、正确性或许可证合规。
社区 skills、agents、`CLAUDE.md` 文件可能包含 prompt 注入、工具投毒、隐藏 payload、不安全数据处理等风险。在特权环境中安装或运行任何项目（包括其依赖）之前，请自行复查。
星标、fork、许可证、维护状态变化很快。本表数据最后核对于 **2026-05-13**，发布前必须重新核实。
---

## 许可
[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)]([https://creativecommons.org/publicdomain/zero/1.0/](https://creativecommons.org/publicdomain/zero/1.0/))
在法律允许范围内，维护者放弃本作品的全部著作权及邻接权。原始理论与引言著作权 © Andrej Karpathy（[karpathy.ai](http://karpathy.ai)）。
发布到 GitHub 后本列表将以 [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/) 释出。所链接的项目保留各自原许可证（多为 MIT 或 Apache-2.0）。
---
