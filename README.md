# Awesome Andrej Karpathy [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**Language / 语言**：[English](#about-andrej-karpathy) · [简体中文 / Chinese](./README.zh-CN.md)
> A curated map of Andrej Karpathy's open-source legacy and the 200+ community projects built on his ideas — from `micrograd` to `LLM Wiki`, from `Software 2.0` to `Vibe Coding`.
> **Note**: This is a curated awesome-list following `awesome-*` conventions.

## Legend
- ⭐ Official Karpathy repository or gist
- 🌟 De-facto standard / flagship of its sub-lineage
- 🇨🇳 Chinese-language project
- 📺 Video or talk
- 📖 Blog post or essay
- 🪧 X / Twitter thread (idea seed)
- 🎓 Course / lecture series
- ⚙️ Framework / library
- 📚 Awesome-list / curation

## Contents
- [About Andrej Karpathy](#about-andrej-karpathy)
- [Foundational Repos](#foundational-repos)
  - [Educational primitives](#educational-primitives)
  - [Minimal GPT implementations](#minimal-gpt-implementations)
  - [Full-stack ChatGPT speedrun](#full-stack-chatgpt-speedrun)
  - [Reject the inevitability of PyTorch](#reject-the-inevitability-of-pytorch)
  - [Single-file inference](#single-file-inference)
  - [Tokenizer from scratch](#tokenizer-from-scratch)
  - [RNN era](#rnn-era)
  - [Browser-side deep learning](#browser-side-deep-learning)
  - [Reinforcement learning intro](#reinforcement-learning-intro)
- [Concepts & Manifestos](#concepts--manifestos)
- [Community Implementations](#community-implementations)
  - [LLM Wiki](#llm-wiki)
  - [`CLAUDE.md` / Karpathy Skills](#claudemd-karpathy-skills)
  - [AutoResearch](#autoresearch)
  - [NanoGPT speedrun](#nanogpt-speedrun)
  - [Recipe for Training NN](#recipe-for-training-nn)
  - [LLM OS](#llm-os)
  - [Vibe Coding](#vibe-coding)
  - [Pong from Pixels reproductions](#pong-from-pixels-reproductions)
  - [nn-zero-to-hero workbooks](#nn-zero-to-hero-workbooks)
  - [nanochat reproductions](#nanochat-reproductions)
  - [LLM Council forks](#llm-council-forks)
  - [reader3 forks](#reader3-forks)
  - [Multi-language ports (microgpt / minbpe / llm.c / llama2.c)](#multi-language-ports)
  - [GPT minimal derivatives & cross-modal](#gpt-minimal-derivatives-cross-modal)
  - [Graphify / Raw-folder-first](#graphify-raw-folder-first)
  - [Agentic Engineering](#agentic-engineering)
  - [HN Time Capsule](#hn-time-capsule)
  - [AI Job Exposure](#ai-job-exposure)
  - [Idea File](#idea-file)
  - [Micro seeds](#micro-seeds)
  - [Concept citations layer](#concept-citations-layer)
- [Talks & Writings](#talks--writings)
- [Timeline 2015 → 2026](#timeline-2015--2026)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
- [Disclaimer](#disclaimer)
- [License](#license)

## About Andrej Karpathy
**Andrej Karpathy** is one of the few researchers who consistently ships *and* explains: stripping complex systems down to their algorithmic core, then publishing both the code and the lecture. Founding member of OpenAI (2015–2017, 2023–2024), former Sr. Director of AI at Tesla (Autopilot vision stack, 2017–2022), Stanford CS231n co-instructor, and PhD with Fei-Fei Li. In 2024 he founded [Eureka Labs](http://eurekalabs.ai), an AI-native school.
- 🏠 [karpathy.ai](http://karpathy.ai)
- 🐙 [github.com/karpathy](http://github.com/karpathy)
- 🐦 [x.com/karpathy](http://x.com/karpathy)
- 🎓 [Neural Networks: Zero to Hero](http://karpathy.ai/zero-to-hero.html)
---

## Foundational Repos
### Educational primitives
- ⭐ [karpathy/micrograd](https://github.com/karpathy/micrograd) - ~100 lines of autograd + ~50 lines of NN with a PyTorch-like API. Companion to Zero-to-Hero lecture 1.
- ⭐ [karpathy/makemore](https://github.com/karpathy/makemore) - Character-level language model that walks bigram → MLP → RNN → Transformer in 5 stages.
- ⭐ [karpathy/nn-zero-to-hero](https://github.com/karpathy/nn-zero-to-hero) - The canonical Zero-to-Hero notebook bundle covering every lecture.
### Minimal GPT implementations
- ⭐ [karpathy/minGPT](https://github.com/karpathy/minGPT) - ~300-line PyTorch GPT with a teaching-grade addition demo (99.9% accuracy).
- ⭐ [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) - The simplest, fastest repo for training/finetuning medium-sized GPTs (★57K+).
### Full-stack ChatGPT speedrun
- ⭐ [karpathy/nanochat](https://github.com/karpathy/nanochat) - "The best ChatGPT \$100 can buy": single-node full-stack training + chat UI in ~8000 hand-written lines.
- ⭐ [karpathy/microgpt](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95) - 200-line dependency-free Python: dataset, tokenizer, autograd, GPT, Adam, train, infer.
- ⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch) - 630-line single-GPU training core that lets an agent edit `program.md` and run 5-minute experiment loops (★66K+, 9.6K forks).
- ⭐ [karpathy/llm-council](https://github.com/karpathy/llm-council) - Multi-LLM "council": parallel answers, mutual scoring, Chairman LLM synthesizes the final reply.
- ⭐ [karpathy/reader3](https://github.com/karpathy/reader3) - EPUB chapter reader purpose-built for "reading books with an LLM". Hit 1.5K★ in 2 days.
- ⭐ [karpathy/KarpathyTalk](https://github.com/karpathy/KarpathyTalk) (2026/04) - Experimental builders+agents shared platform built around the talks.
### Reject the inevitability of PyTorch
- ⭐ [karpathy/llm.c](https://github.com/karpathy/llm.c) - Pure C/CUDA training of GPT-2/3 with a ~1000-line CPU reference. Karpathy explicitly invites ports to live as external repos.
### Single-file inference
- ⭐ [karpathy/llama2.c](https://github.com/karpathy/llama2.c) - Single-file C inference for Llama 2, plus PyTorch training scripts. The Karpathy repo with **the most multi-language ports**.
### Tokenizer from scratch
- ⭐ [karpathy/minbpe](https://github.com/karpathy/minbpe) - Three-tier teaching implementation (Basic / Regex / GPT4 tokenizers) paired with the *Let's build the GPT Tokenizer* video.
### RNN era
- ⭐ [karpathy/char-rnn](https://github.com/karpathy/char-rnn) - The Torch/Lua multi-layer RNN/LSTM/GRU char-level LM that powered the *Unreasonable Effectiveness of RNNs* essay.
- ⭐ [karpathy/min-char-rnn](https://gist.github.com/karpathy/d4dee566867f8291f086) - Vanilla RNN in 100 lines of pure NumPy (★4K+).
### Browser-side deep learning
- ⭐ [karpathy/convnetjs](https://github.com/karpathy/convnetjs) - JS CNN/RL training library; for many learners this was the first place backprop was *visible*.
- ⭐ [karpathy/reinforcejs](https://github.com/karpathy/reinforcejs) - JS implementations of DP / SARSA / Q-learning / DQN / Policy Gradient with web demos.
### Reinforcement learning intro
- ⭐ [karpathy/pg-pong](https://gist.github.com/karpathy/a4166c7fe253700972fcbc77e4ea32c5) - 130-line NumPy policy-gradient agent for ATARI Pong. Companion to the *Pong from Pixels* essay.
---

## Concepts & Manifestos
> Idea seeds for everything in [Community Implementations](#community-implementations) below.
- 📖 [Software 2.0](https://karpathy.medium.com/software-2-0-a64152b37c35) (2017) - "Neural networks are a new kind of code; weights are the program."
- 📺 [Software is Changing (Again)](https://www.ycombinator.com/library/MW-andrej-karpathy-software-is-changing-again) (YC 2025) - English as the new programming language; Software 3.0 eats 1.0/2.0. [Annotated transcript](https://www.latent.space/p/s3).
- 📺 [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) + 🪧 [LLM OS tweet](https://x.com/karpathy/status/1723140519554105733) (2023/11) - LLM as CPU, context as RAM, vector store as FS, tools as peripherals.
- 🪧 [Vibe coding tweet](https://x.com/karpathy/status/1886192184808149383) + 📖 [MenuGen blog](https://karpathy.bearblog.dev/vibe-coding-menugen/) (2025/02) - "Fully give in to the vibes and forget the code even exists."
- 🪧 [Agentic engineering / `CLAUDE.md` series](https://x.com/karpathy) (2025/12 → 2026/01) - `CLAUDE.md` is the new system prompt; *skills* are the new function library.
- ⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch) (2026/03) - Software 3.0 applied to research: agent rewrites `program.md`, runs experiments, repeats.
- 🪧 [LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) (2026/04) - Pre-compiled knowledge base + LLM renderer; an anti-RAG manifesto.
- 📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/) (2019) - The "overfit a single batch first, then generalize" SOP.
- 📖 [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) (2015) - The most-shared blog post of the RNN era; spawned char-rnn ports in every language.
---

## Community Implementations
> Each subsection lists projects whose README/About explicitly cites a Karpathy repo, essay, or tweet. Stars/forks change fast — verify before publishing.
### LLM Wiki
> Seed: 🪧 [LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) (2026/04, the gist alone has ★28K+, 6,188 forks). The single largest sub-ecosystem in this list — **30+ implementations across 6 form factors**, each with explicit Karpathy attribution in their README/About.
**Web app / desktop product**
- 🌟 [lucasastorian/llmwiki](https://github.com/lucasastorian/llmwiki) - Strict gist-spec implementation. Web app + MCP + Claude account integration, hosted at [llmwiki.app](http://llmwiki.app). Apache-2.0.
- [nashsu/llm_wiki](https://github.com/nashsu/llm_wiki) - Cross-platform desktop app; Obsidian-compatible storage, explicit "anti-RAG" framing.
**Claude Code skill / plugin / Agent Skills**
- [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki) - Agent Skills-compatible (Claude Code / Cursor / Codex / OpenCode) packaged skill.
- [kfchou/wiki-skills](https://github.com/kfchou/wiki-skills) - Lightweight Claude Code skill; persistent compounding knowledge base.
- [ussumant/llm-wiki-compiler](https://github.com/ussumant/llm-wiki-compiler) - Claude Code plugin that compiles markdown into a topic-based wiki.
- [praneybehl/llm-wiki-plugin](https://github.com/praneybehl/llm-wiki-plugin) - Claude Code plugin; cross-references vanillaflava, OmegaWiki, Synthadoc.
- [atomicmemory/llm-wiki-compiler](https://github.com/atomicmemory/llm-wiki-compiler) - CLI knowledge compiler ("raw sources in, interlinked wiki out").
- [micuintus/llm-wiki](https://github.com/micuintus/llm-wiki) - Agent-agnostic minimal skill; "razor-sharp" reference implementation.
- [charlie947/ai-second-brain](https://github.com/charlie947/ai-second-brain) - Builds a searchable second brain from ChatGPT/Claude/research history.
- [coleam00/claude-memory-compiler](https://github.com/coleam00/claude-memory-compiler) - "Memory school": compiles chat history into a wiki.
**Obsidian (append vs rewrite schools)**
- 🌟 [Ar9av/obsidian-wiki](https://github.com/Ar9av/obsidian-wiki) - The Obsidian × multi-agent shared Wiki Skills framework; "Obsidian is viewer, LLM is maintainer" reference (★933).
- 🌟 [eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain) - "Rewrite school" representative; 31 commands + 4 scheduled agents that re-edit the vault.
- [NicholasSpisak/second-brain](https://github.com/NicholasSpisak/second-brain) - Classic raw-folder → compiled-wiki → Obsidian browse pipeline.
- [AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian) - Claude + Obsidian companion with `/wiki` `/save` `/autoresearch` slash commands.
- [MehmetGoekce/llm-wiki](https://github.com/MehmetGoekce/llm-wiki) - Claude Code + Logseq/Obsidian; L1/L2 cache architecture.
- [balukosuri/llm-wiki-karpathy](https://github.com/balukosuri/llm-wiki-karpathy) - Lightweight Cursor / Obsidian personal-KB recipe.
- [kytmanov/obsidian-llm-wiki-local](https://github.com/kytmanov/obsidian-llm-wiki-local) - 100% local, Ollama-driven Obsidian wiki.
- [green-dalii/obsidian-llm-wiki](https://github.com/green-dalii/obsidian-llm-wiki) - Obsidian plugin with multi-page entity/concept generation + conversational query.
- [2233admin/obsidian-llm-wiki](https://github.com/2233admin/obsidian-llm-wiki) - Minimal Obsidian fork.
**Multi-agent / production-grade extensions**
- [nvk/llm-wiki](https://github.com/nvk/llm-wiki) - Parallel multi-agent research compiler; thesis-driven investigation + artifact generation.
- [redmizt/multi-agent-wiki-toolkit](https://github.com/redmizt/multi-agent-wiki-toolkit) - Identity tokens, security hooks, dispatch, contamination firewalls, active learning.
- [skyllwt/OmegaWiki](https://github.com/skyllwt/OmegaWiki) - Full research platform: papers → KG → gap detection → idea gen → experiment design → paper writing → review reply.
- [yologdev/karpathy-llm-wiki](https://github.com/yologdev/karpathy-llm-wiki) - Self-growing full-stack app born from feeding Karpathy's founding prompt to an agent.
- [cablate/llm-atomic-wiki](https://github.com/cablate/llm-atomic-wiki) - Atomic wiki extension: atom layer + topic branches + two-layer lint.
**Chinese-language**
- 🇨🇳 [zhurudong/andrej-karpathy-llm-wiki](https://github.com/zhurudong/andrej-karpathy-llm-wiki) - Gist translation + implementation notes.
- 🇨🇳 [gatelynch/llm-knowledge-base](https://github.com/gatelynch) - Traditional-Chinese practice.
- 🇨🇳 [chengjialu8888/LLM-Wiki-KB](https://github.com/chengjialu8888) - Simplified-Chinese implementation.
### `CLAUDE.md` / Karpathy Skills
> Seed: 🪧 Agentic engineering tweet series (2025/12 → 2026/01) + 📺 [Sequoia AI Ascent: From Vibe Coding to Agentic Engineering](https://www.youtube.com/watch?v=96jN2OCOfLs) (2026/04).
- 🌟 [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) - Compresses Karpathy's scattered X observations into a single `CLAUDE.md` (4 behavioral rules). **★119K**, 11.9K forks; the de-facto standard of this lineage.
- [renezander030 / Karpathy-skills `CLAUDE.md` v2 (gist)](https://gist.github.com/renezander030/2898eb5f0100688f4197b5e493e156a2)(https://gist.github.com/renezander030/2898eb5f0100688f4197b5e493e156a2) - Extends forrestchang with 6 runtime rules from shipping `fixclaw`; covers prompt-injection and budget guards.
- [K-Dense-AI/karpathy](https://github.com/K-Dense-AI/karpathy) - Agentic ML Engineer built on Claude Agent SDK + Google ADK; "Scientific Agent Skills" framing.
- [Smithbox-ai/ControlFlow](https://github.com/Smithbox-ai/ControlFlow) - Karpathy-skills idea forked into a more structured ControlFlow agent.
- [PBNZ/newton-skill](https://github.com/PBNZ/newton-skill) - Single "Newton-style first-principles" skill derived from the series.
- 📚 [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - Curated list of 235 Claude skills with sources tracing back to forrestchang.
- [mattpocock/skills](https://github.com/mattpocock/skills) - Matt Pocock's TypeScript-flavored skills collection.
- [karpathy/llm-council · `CLAUDE.md` (canonical example)](https://github.com/karpathy/llm-council/blob/master/CLAUDE.md) - Karpathy's own per-project `CLAUDE.md` (166 lines, technical notes for LLM Council).
### AutoResearch
> Seed: ⭐ [karpathy/autoresearch](https://github.com/karpathy/autoresearch) (2026/03).
**Domain transfers**
- [RightNow-AI/autokernel](https://github.com/RightNow-AI/autokernel) - autoresearch loop applied to GPU kernel auto-tuning.
- [saikatkumardey/autoresearch-tabular](https://github.com/saikatkumardey/autoresearch-tabular) - Tabular ML research agent.
- [trantrikien239/autoresearch-tabular](https://github.com/trantrikien239/autoresearch-tabular) - Alternative tabular implementation.
- [jhamandeep/autoresearch-tabular-case-study](https://github.com/jhamandeep/autoresearch-tabular-case-study) - Tabular case study with ablations.
- [monk1337/Bio-Autoresearch](https://github.com/monk1337/Bio-Autoresearch) - Bioinformatics adaptation.
- [aiming-lab/AutoResearchClaw](https://github.com/aiming-lab/AutoResearchClaw) - AI-safety / red-team angle.
- [ArchishmanSengupta/autovoiceevals](https://github.com/ArchishmanSengupta/autovoiceevals) - Voice eval automation.
- [dorringel/epsiclaw](https://github.com/dorringel/epsiclaw) - Operations research direction.
**Multi-LLM backends**
- [ajzhanghk/autoresearch-glm](https://github.com/ajzhanghk/autoresearch-glm) - GLM backend.
- [supratikpm/autoresearch-gemini](https://github.com/supratikpm) - Gemini CLI backend.
- [romovpa/Claudini](https://github.com/romovpa/Claudini) - Claude / multi-model hybrid.
- [Entrpi/autoresearch-everywhere](https://github.com/Entrpi/autoresearch-everywhere) - Cross-cloud loop.
- [abcdedf/autoresearch-anycloud](https://github.com/abcdedf/autoresearch-anycloud) - Cross-vendor loop.
**Agent-flavor adaptations**
- [hwchase17/autoresearch-agents](https://github.com/hwchase17/autoresearch-agents) - LangChain CTO's port: instead of optimizing ML training, it auto-improves **agents** using LangSmith evals.
- [uditgoenka/autoresearch](https://github.com/uditgoenka/autoresearch) - Adds an `AGENTS.md` shim so any coding agent can drive the loop.
**Frameworks & curations**
- ⚙️ [VectorInstitute/helix](https://github.com/VectorInstitute/helix) + [helix-examples](https://github.com/VectorInstitute/helix-examples) - Vector Institute autoresearch framework with reproducible Karpathy + inference-TPS examples.
- ⚙️ [agentsmd/](https://github.com/agentsmd/agents.md)`agents.md` - Open `AGENTS.md` standard (★21K) that the autoresearch ecosystem largely adopted.
- 📚 [GitHub topic: karpathy-inspired](https://github.com/topics/karpathy-inspired) - Community topic collecting autoresearch-style autonomous improvement loops.
- 📚 [WecoAI/awesome-autoresearch](https://github.com/WecoAI/awesome-autoresearch) - Early collection.
- 📚 [alvinreal/awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch) - Mainstream awesome-list (★1.7K).
- 📚 🇨🇳 [yibie/awesome-autoresearch](https://github.com/yibie/awesome-autoresearch) - Chinese curation.
**Industrial integrations**
- ⚙️ [Red Hat OpenShift AI · autoresearch integration](https://www.redhat.com/en/blog) - 198-experiment showcase running the autoresearch loop on OpenShift AI.
- 🎓 [Lightning AI · autoresearch tutorial track](https://lightning.ai/) - Tutorial-platform integration that walks through the full loop.
- [revis · multi-agent autoresearch fork](https://www.reddit.com/r/LocalLLaMA/) - Reddit-discussed fork that adds multi-agent collaboration on top of the canonical loop.
- Ascend/CANN fork - Huawei Ascend NPU adaptation ([Discussion #519](https://github.com/karpathy/autoresearch/issues/519)).
- Colab/Kaggle T4 fork - Free T4 GPU port, zero cost and zero local setup ([Discussion #208](https://github.com/karpathy/autoresearch/issues/208)).
### NanoGPT speedrun
> Seed: ⭐ [karpathy/nanoGPT](https://github.com/karpathy/nanoGPT) + ⭐ [llm.c](https://github.com/karpathy/llm.c) training baselines.
- 🌟 [KellerJordan/modded-nanogpt](https://github.com/KellerJordan/modded-nanogpt) - 8×H100 training-time speedrun, currently **127.7s** (down from 8.2 min one year prior). Standard of this lineage.
- ⚙️ [KellerJordan/Muon](https://kellerjordan.github.io/posts/muon/) - Derived optimizer; spawned MARS / SWAN / AdaMuon variants.
- [tyler-romero/nanogpt-speedrun](https://github.com/tyler-romero/nanogpt-speedrun) - Reproduces modded-nanoGPT on 2×RTX 4090, logs every gain.
- [alexjc/nanogpt-speedrun](https://github.com/alexjc/nanogpt-speedrun) - Consumer-grade speedrun.
- [VatsaDev/NanoPoor](https://github.com/VatsaDev/NanoPoor) - "NanoGPT speedrun for the poor T4 enjoyers" — Colab T4 / A100 unofficial leaderboard.
- [cat-state/modded-nanogpt-moe](https://github.com/cat-state/modded-nanogpt-moe) - MoE variant forked at the 10.8 min record.
- [BlinkDL/modded-nanogpt-rwkv](https://github.com/BlinkDL/modded-nanogpt-rwkv) - RWKV-flavored speedrun fork.
- [nikhilvyas/modded-nanogpt-SOAP](https://github.com/nikhilvyas/modded-nanogpt-SOAP) - SOAP optimizer variant.
- [Faster-nanoGPT](https://github.com/Faster-nanoGPT) - Multi-node speedrun experiments.
- [Marin Speedrun](https://www.marin.community/) - Industrial speedrun leaderboard.
- [Prime Intellect leaderboard](https://www.primeintellect.ai/) - Industrial speedrun leaderboard.
- 📖 [Automated LLM Speedrunning Benchmark](https://openreview.net/) - OpenReview paper turning speedruns into a benchmark.
### Recipe for Training NN
> Seed: 📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/) (2019).
- ⚙️ [BlackHC/neural_net_checklist](https://github.com/BlackHC/neural_net_checklist) - Karpathy's training SOP packaged as a callable PyPI library.
- [chicobentojr's NN training checklist gist](https://gist.github.com/chicobentojr) - Personal checklist implementation.
### LLM OS
> Seed: 🪧 [LLM OS tweet](https://x.com/karpathy/status/1723140519554105733) (2023/11).
- [victor-iyi/llm-os](https://github.com/victor-iyi/llm-os) - Explicitly "inspired by Andrej Karpathy".
- 📚 [bilalonur/awesome-llm-os](https://github.com/bilalonur/awesome-llm-os) - Dedicated awesome-list of LLM OS projects, papers, and discussions.
- ⚙️ [agno-agi/agno](https://github.com/agno-agi/agno) (formerly phidata) - LLMOS Cookbook; commercial-grade LLM OS framework.
- ⚙️ [microsoft/JARVIS](https://github.com/microsoft/JARVIS) - Multi-model OS-like agent.
- 📖 [agiresearch/AIOS](https://github.com/agiresearch/AIOS) - Rutgers academic "LLM Agent OS".
- ⚙️ [letta-ai/letta](https://github.com/letta-ai/letta) (formerly MemGPT) - OS-style memory tiering for long context.
- 📖 [HuggingFace shivance/illustrated-llm-os](https://huggingface.co/blog/shivance/illustrated-llm-os) - Visual long-form explainer.
### Vibe Coding
> Seed: 🪧 [Vibe coding tweet](https://x.com/karpathy/status/1886192184808149383) (2025/02).
**Awesome lists**
- 📚 [filipecalegario/awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding) - Tools / projects / essays; opens by citing Karpathy.
- 📚 [taskade/awesome-vibe-coding](https://github.com/taskade/awesome-vibe-coding) - Taskade-curated list.
- 📚 [ai-for-developers/awesome-vibe-coding](https://github.com/ai-for-developers/awesome-vibe-coding) - Developer-focused curation.
- 📚 [0xWelt/Awesome-Vibe-Coding](https://github.com/0xWelt/Awesome-Vibe-Coding) - Open-source-tools-leaning curation.
- 📚 [levz0r/awesome-vibecoded-apps](https://github.com/levz0r/awesome-vibecoded-apps) - Apps actually built via vibe coding.
**Tutorials & Chinese**
- 🎓 [goker/vibe-coding-101](https://github.com/goker/vibe-coding-101) - Vibe Coding 101 course.
- 🇨🇳 🎓 [datawhalechina/easy-vibe](https://github.com/datawhalechina/easy-vibe) - Datawhale Chinese tutorial.
- 🇨🇳 [EnzeD/vibe-coding](https://github.com/EnzeD/vibe-coding) - Chinese collection (★1.3K+).
- [JasonRobertDestiny/VibeDoc](https://github.com/JasonRobertDestiny/VibeDoc) - Vibe-doc generator.
- [DeadWaveWave/demo2apk](https://github.com/DeadWaveWave/demo2apk) - Demo→APK vibe pipeline.
- [cporter202/lovable-for-beginners](https://github.com/cporter202/lovable-for-beginners) - Lovable beginner's guide.
- [Zentrun](https://github.com/Zentrun) - Multi-experiment vibe coding collection.
### Pong from Pixels reproductions
> Seed: ⭐ [karpathy/pg-pong](https://gist.github.com/karpathy/a4166c7fe253700972fcbc77e4ea32c5) + 📖 [Pong from Pixels](http://karpathy.github.io/2016/05/31/rl/) (2016).
- 🌟 [omkarv/pong-from-pixels](https://github.com/omkarv/pong-from-pixels) - Annotated, fixed, and extended into a full RL onboarding curriculum.
- [johnrobinsn/pongfrompixels](https://github.com/johnrobinsn/pongfrompixels) - Modernized to Python 3 + Tensorboard.
- [gameofdimension/policy-gradient-pong](https://github.com/gameofdimension/policy-gradient-pong) - TensorFlow implementation explicitly based on the blog post.
- [omerbsezer/PolicyGradient_PongGame](https://github.com/omerbsezer/PolicyGradient_PongGame) - Variant implementation.
- [stewy33/pong-with-policy-gradients](https://github.com/stewy33/pong-with-policy-gradients) - Variant implementation.
- [julian-q/policy-gradient](https://github.com/julian-q/policy-gradient) - Pure NumPy policy gradient on Pong.
- [xanderex-sid / pg-pong PyTorch](https://gist.github.com/xanderex-sid/ae6cd3ea0c3759c1e3f92835ebd6e158) - PyTorch CNN/MLP rewrite tested on Colab; published as a comment on the original gist.
- [washburn125/Atari-Pong](https://github.com/washburn125/Atari-Pong) - OpenAI Gym RL project explicitly building on the post.
- [8bitmp3/NumPy-org-Tutorial-Policy-Gradients-Deep-RL-with-Pong-from-Scratch](https://github.com/8bitmp3/NumPy-org-Tutorial-Policy-Gradients-Deep-RL-with-Pong-from-Scratch) - Official [NumPy.org](https://numpy.org) tutorial (Google Season of Docs 2020).
- [mlitb/pong](https://github.com/mlitb/pong) - DQN / DDQN three-person student reproduction.
- [shehio/Karpathy-Pong](https://github.com/shehio/Karpathy-Pong) - "One algorithm at a time" reproduction with derivatives.
- 📖 [Ian McKenzie — Pong from pixels without reading "Pong from Pixels"](https://www.lesswrong.com/posts/ipxmEgNeqFkjJAmx3) - LessWrong post implementing DQN from the original DeepMind paper as a comparison.
### nn-zero-to-hero workbooks
> Seed: ⭐ [karpathy/nn-zero-to-hero](https://github.com/karpathy/nn-zero-to-hero) (★20.3K) + 🎓 [Zero-to-Hero series](http://karpathy.ai/zero-to-hero.html).
**Annotated lecture notes**
- 🌟 [chizkidd/Karpathy-Neural-Networks-Zero-to-Hero](https://github.com/chizkidd/Karpathy-Neural-Networks-Zero-to-Hero) - Lecture-by-lecture annotated notebooks; ideal second pass.
- [MK2112/nn-zero-to-hero-notes](https://github.com/MK2112/nn-zero-to-hero-notes) - Detailed Markdown + Jupyter notes covering every video.
- [ryankillian/karpathy-lectures-workbooks](https://github.com/ryankillian/karpathy-lectures-workbooks) - Companion exercises with Colab links.
- [0ssamaak0/Karpathy-Neural-Networks-Zero-to-Hero](https://github.com/0ssamaak0/Karpathy-Neural-Networks-Zero-to-Hero) - Full lecture playthrough (micrograd + makemore + minBPE + nanoGPT + GPT2).
**Rewrites in other languages**
- [Anri-Lombard/micrograd](https://github.com/Anri-Lombard/micrograd) - Step-by-step rewrite (publicly upvoted by Karpathy on X).
- [Anri-Lombard/makemore](https://github.com/Anri-Lombard/makemore) - Same author's makemore rewrite.
- [shoestringinc/microgradr](https://github.com/shoestringinc/microgradr) - Rust rewrite of micrograd.
- [shoestringinc/makemore-rs](https://github.com/shoestringinc/makemore-rs) - Rust rewrite of makemore.
- [danielway/micrograd-rs](https://github.com/danielway/micrograd-rs) - Scalar-valued autograd engine in Rust.
- [msminhas93/ferric-micrograd](https://github.com/msminhas93/ferric-micrograd) - Rust implementation supporting batched reverse-mode autodiff with full NN functionality.
- [AlphaGit/alpha-micrograd-rust](https://github.com/AlphaGit/alpha-micrograd-rust) - Active Rust port (v0.4.0) with companion blog.
- [kfish/micrograd-cpp-2023](https://github.com/kfish/micrograd-cpp-2023) - C++ port of micrograd, tracks the YouTube tutorial.
- [kfish/makemore-cpp-2023](https://github.com/kfish/makemore-cpp-2023) - C++ port of makemore (ZTH lectures 2-5).
- [turingcompl33t/makemore-and-friends](https://github.com/turingcompl33t/makemore-and-friends) - Companion micrograd + makemore demo notebooks.
**Curriculum-extension projects**
- [niloydebbarma-code/Learn-nanoGPT](https://github.com/niloydebbarma-code/Learn-nanoGPT) - Hardware-adaptive training config for low-end GPU learners.
### nanochat reproductions
> Seed: ⭐ [karpathy/nanochat](https://github.com/karpathy/nanochat) (★44K, 7.1K forks; current leaderboard record Run 6: 1.65h, CORE 0.263, Mar 14 2026).
**Apple Silicon / MLX**
- 🌟 [scasella/nanochat-mlx](https://github.com/scasella/nanochat-mlx) - Self-contained MLX port; one `--depth` dial controls everything. No PyTorch.
- [ettrickshepherd/mlx_nanochat](https://github.com/tkwn2080/mlx_nanochat) - Alternative full-stack MLX implementation (tokenizer + pretrain + SFT + chat + eval).
- [vithursant/nanoGPT_mlx](https://github.com/vithursant/nanoGPT_mlx) - Earlier nanoGPT → MLX port that paved the way; M3 Pro 0.37 it/s on Shakespeare.
- [zsiegel/mlx-gpt](https://github.com/zsiegel/mlx-gpt) - GPT-from-scratch alongside the Karpathy video, trained on M4 Max in ~30 min.
- [ediestel/picochat-mlx](https://github.com/ediestel/picochat-mlx) - Minimalist Apple Silicon MLX port.
**Homelab / consumer GPU**
- 🌟 [matt-langston/nanochat-dgx-spark](https://github.com/matt-langston/nanochat-dgx-spark) - 2× Blackwell desktop GPUs running the full pipeline; 62.6h training log finding 17 bugs ([discussion #710](https://github.com/karpathy/nanochat/discussions/710)).
- Trelis nanochat-fork - 4-hour / \$100 training to a 500M-param LLM with HuggingFace push scripts.
- *Reproducing nanochat in Colab Single GPU* - DeepWiki + Gemini compresses nanochat onto a single Colab GPU ([Reddit](https://www.reddit.com/r/LocalLLaMA/comments/1o76ev6)).
- [saranormous/supa-beginna-nanochat](https://github.com/karpathy/nanochat/discussions/677) - Pre-cloud laptop walkthrough so every stage is understood before renting a GPU.
**Adjacent / faster minimal cores**
- [Entrpi/EEmicroGPT](https://github.com/Entrpi/EEmicroGPT) - ~10× speedup over microgpt (also listed under autoresearch).
- [webml-community/nanochat-webgpu](https://huggingface.co/spaces/webml-community/nanochat-webgpu) - WebGPU port by Xenova; nanochat models run 100% locally in browser, no server.
- [chrisjmccormick / Exploring Nanochat](https://github.com/KellerJordan/modded-nanogpt/discussions/206) - Cross-pollination notes between modded-nanogpt and nanochat code bases.
### LLM Council forks
> Seed: ⭐ [karpathy/llm-council](https://github.com/karpathy/llm-council) (★18.5K, 3.6K forks; 3-stage council: collect → anonymized peer rank → Chairman synth).
**Multi-LLM councils**
- [am-will/llm-council](https://github.com/am-will/llm-council) - Multi-agent orchestration for Claude Code; OpenCode/Claude Code/Gemini-CLI/Codex agent kinds, judge-merge.
- [hideki5123/multi-agent-council](https://github.com/hideki5123/multi-agent-council) - Claude + OpenAI + Gemini 3-round protocol (Independent → Cross Review → Chair Synthesis).
- [Sentry01/AgentCouncil](https://github.com/Sentry01/AgentCouncil) - Collaborative/adversarial multi-agent on top of GitHub Copilot CLI.
- [andrewvaughan/agent-council](https://github.com/andrewvaughan/agent-council) - 13 agent personas across 6 councils; SAST scanning + 4-member security/quality/testing/docs review.
- [MrLesk/agents-council](https://github.com/MrLesk/agents-council) - Bridge across Claude Code, Codex, Gemini, and Cursor agent sessions.
- [danielrosehill/LLM-Council-V3](https://github.com/danielrosehill/LLM-Council-V3) - Adds context-prompt separation and prompt actuation.
- KobyStam *LLM Council Plus* - Modern UI + settings page + multi-API + web search + Ollama support ([video](https://www.youtube.com/watch?v=HOdyIyccOCE)).
**Claude Code skills / plugins**
- [valorisa/llm-council-skill](https://github.com/valorisa/llm-council-skill) - 5 advisor roles (Contrarian / First Principles / Expansionist / Outsider / Executor) wrapped as a Claude skill.
- [ngmeyer/council-review](https://github.com/topics/llm-council) - Claude Code skill: decisions/code/plans through 5-advisor council with anonymous peer review.
- [Zandereins/hydra](https://github.com/topics/llm-council) - Multi-perspective code review council; 3 advisors / 10 agents in deep mode (Opus + Codex), evidence chains.
- [valpere/chorus](https://github.com/topics/llm-council) - Cross-agent plugin for Claude Code / OpenCode / Gemini CLI / Codex (council, parallel review, debug patterns).
- [looptroop-ai/LoopTroop](https://github.com/topics/llm-council) - LLM councils plan, Ralph loops recover, OpenCode worktrees ship.
- [tenfoldmarc/llm-council-skill](https://github.com/tenfoldmarc/llm-council-skill) - 5 advisor roles as a Claude Code skill with anonymous peer review.
- [gcpdev/llm-council-skill](https://github.com/gcpdev/llm-council-skill) - Collaborative brainstorming with ChatGPT and Gemini as a Claude Code skill.
- [aiwithremy/claude-skills-llm-council](https://github.com/aiwithremy/claude-skills-llm-council) - Teaches Claude to spin up 5 advisors to debate and deliver verdicts.
- [shuntacurosu/llm_council_skill](https://github.com/shuntacurosu/llm_council_skill) - Orchestrating multiple LLMs with peer review and chairman synthesis.
- [dair-ai/dair-academy-plugins](https://github.com/dair-ai/dair-academy-plugins) - LLM Council skill plugin powered by Fireworks AI multi-phase deliberation.
**Variants & integrations**
- [malik-builds/better-llm-council](https://github.com/malik-builds/better-llm-council) - Improved scoring pipeline.
- [YonasValentin/llm-council](https://github.com/YonasValentin/llm-council) - Early fork with web UI.
- [sjsreehari/debate-engine](https://github.com/topics/llm-council) - Pro/Con/Judge agents with memory + uncertainty signals; OpenRouter + Ollama.
- [microsoft/hve-core](https://github.com/microsoft/hve-core/issues/1326) - Microsoft proposal to add an LLM Council orchestrator (GPT-5.4 / Opus 4.6 / Gemini 3.1 Pro).
- [sherifkozman/the-llm-council](https://github.com/sherifkozman/the-llm-council) - Claude Code framework wrapping the 3-stage council pattern (collect → anonymized peer rank → Chairman synth).
- [jacob-bd/llm-council-plus](https://github.com/jacob-bd/llm-council-plus) - Modern UI fork with multi-API + web search + Ollama support.
- 📚 [danielrosehill/Awesome-LLM-Council-Projects](https://github.com/danielrosehill/Awesome-LLM-Council-Projects) - Curated list of multi-model deliberation systems.
### reader3 forks
> Seed: ⭐ [karpathy/reader3](https://github.com/karpathy/reader3) (★3.4K, 456+ forks; "90% vibe-coded just to illustrate how to read books with LLMs").
**Standalone re-implementations**
- [yongkangc/llmreader](https://github.com/yongkangc/llmreader) - Adds PDF support on top of EPUB; reframes as "LLMReader" with quote-driven landing.
**Pull requests on the original repo (canonical forks)**
- [sharathdoes/reader3](https://github.com/sharathdoes) - ChatGroq LLM chat integration + HTML UI ([PR](https://github.com/karpathy/reader3/pulls)).
- [jerithlawrence/reader3](https://github.com/jerithlawrence) - Text-copy buttons (paragraph / section / chapter).
- [HenokB/reader3](https://github.com/HenokB) - Keyboard arrow keys for prev/next.
- [andrestobelem/reader3](https://github.com/andrestobelem) - Spanish translation + TAR.
### Multi-language ports
> Seeds: ⭐ [microgpt gist](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95) · ⭐ [minbpe](https://github.com/karpathy/minbpe) · ⭐ [llm.c](https://github.com/karpathy/llm.c) · ⭐ [llama2.c](https://github.com/karpathy/llama2.c).
**microgpt ports**
- [mplekh/rust-microgpt](https://github.com/mplekh/rust-microgpt) - Single-file Rust port.
- [Entrpi/EEmicroGPT](https://github.com/Entrpi/EEmicroGPT) - ~10× faster, also listed under nanochat.
**minbpe ports**
- [justinhj/minbpe-cc](https://github.com/justinhj/minbpe-cc) - C++ port (~50× faster training).
- [dorjeduck/minbpe.mojo](https://github.com/dorjeduck/minbpe.mojo) - Mojo port.
- [kuprel/minbpe-pytorch](https://github.com/kuprel/minbpe-pytorch) - PyTorch / CUDA acceleration (~120× faster).
- [gnp/minbpe-rs](https://github.com/gnp/minbpe-rs) - Rust port.
- [Jaward/mlx-minbpe](https://github.com/Jaward/mlx-minbpe) - MLX port for Apple Silicon.
- [minbpe-hs](https://www.reddit.com/r/haskell/comments/1czkpk5/) - Haskell port.
- ⚙️ [atsentia/mojo-tokenizer](https://github.com/atsentia/mojo-tokenizer) - Pure Mojo BPE tokenizer; 144M tok/s on M3 Ultra (3.1× faster than tiktoken).
- ⚙️ [swaits/bpe-tokenizer](https://github.com/swaits/bpe-tokenizer) - Rust BPE library with multilingual BPEmb vocabularies (275 languages).
- ⚙️ [sweepai/bpe-qwen](https://github.com/sweepai/bpe-qwen) - Rust BPE specialised for Qwen (6× / 12× faster than HF tokenizers).
**llm.c ports**
- [gevtushenko/llm.c](https://github.com/gevtushenko/llm.c) - CUDA C++ Core Libraries rewrite; CUDA MODE case study.
- [GaoYusong/llm.cpp](https://github.com/GaoYusong/llm.cpp) - C++ port shipping its own `tinytorch.hpp`.
- [joshcarp/llm.go](https://github.com/joshcarp/llm.go) - Go port.
- [Saimirbaci/llm.zig](https://github.com/Saimirbaci/llm.zig) - Zig port.
- [rbitr/llm.f90](https://github.com/rbitr/llm.f90) - Fortran port.
- [nietras/Llm.cs](https://github.com/nietras/Llm.cs) - C# port; auto-downloads from Hugging Face, clone-and-run on any platform.
- [azret/llm.cs](https://github.com/azret/llm.cs) - C# port; CPU complete, CUDA in progress.
- [otabuzzman/llm.java](https://github.com/otabuzzman/llm.java) - Java port with Stream parallelization and TornadoVM GPU acceleration.
- [otabuzzman/llm.swift](https://github.com/otabuzzman/llm.swift) - Swift port of llm.c.
**llama2.c ports** (the largest port family — Karpathy maintains a "notable forks" PR thread)
- [`srush/llama2.rs`](https://github.com/srush/llama2.rs) - Rust port extended to 70B + 4-bit GPT-Q quantization, batched prefill, SIMD.
- [`gaxler/llama2.rs`](https://github.com/gaxler/llama2.rs) - Alternative Rust port.
- [`leo-du/llama2.rs`](https://github.com/leo-du/llama2.rs) - Alternative Rust port.
- [`ademyanchuk/llama2-rs`](https://github.com/ademyanchuk/llama2-rs) - Rust learning rewrite, multi-file.
- [`danielgrittner/llama2-rs`](https://github.com/danielgrittner/llama2-rs) - Alternative Rust port.
- [`rhlbhatnagar/llama2.rs`](https://github.com/rhlbhatnagar/llama2.rs) - Minimal Rust port using the 15M model from llama2.c.
- [`mukel/llama2.java`](https://github.com/mukel/llama2.java) - Java single-file port (Llama 2 7B at 1.6 tok/s).
- [`mukel/llama3.java`](https://github.com/mukel/llama3.java) - Successor for Llama 3 with `--chat`.
- [`neoremind/llama2.java`](https://github.com/neoremind/llama2.java) - Alternative Java port; matches C performance on fp32 7B.
- [`cgbur/llama2.zig`](https://github.com/cgbur/llama2.zig) - Zig SIMD ~5× speedup.
- [`thxcode/llm-box`](https://pkg.go.dev/github.com/thxcode/llm-box/port/llama2.c) - Go port (`port/llama2.c`).
- ⚙️ [huggingface/candle](https://github.com/huggingface/candle) - HuggingFace Rust framework; `candle-llama` evolved from llama2.c.
### GPT minimal derivatives & cross-modal
> Seeds: ⭐ [minGPT](https://github.com/karpathy/minGPT) + ⭐ [nanoGPT](https://github.com/karpathy/nanoGPT).
**Pure ports**
- [akanyaani/minGPTF](https://github.com/akanyaani/minGPTF) - TensorFlow port of minGPT.
- [mgrankin/minGPT](https://github.com/mgrankin/minGPT) - JAX port of minGPT.
- [pytorch/examples · minGPT-ddp](https://github.com/pytorch/examples/blob/main/distributed/minGPT-ddp/mingpt/model.py) - Official PyTorch DDP teaching sample.
- ⚙️ [Lightning-AI/lit-llama](https://github.com/Lightning-AI/lit-llama) - PyTorch Lightning team's training framework on top of nanoGPT.
- [EleutherAI/nanoGPT-mup](https://github.com/EleutherAI/nanoGPT-mup) - nanoGPT fork incorporating Maximal Update Parameterization (μP) for scaling hyperparameters.
- ⚙️ [stanford-crfm/levanter](https://github.com/stanford-crfm/levanter) - JAX-based large-model trainer with clear nanoGPT lineage.
**MoE / sparse**
- [wolfecameron/nanoMoE](https://github.com/wolfecameron/nanoMoE) - MoE layer + auxiliary losses + stability tricks added to nanoGPT ([blog](https://cameronrwolfe.substack.com/nano-moe)).
- [Antlera/nanoGPT-moe](https://github.com/Antlera/nanoGPT-moe) - Drop-in `use_moe = True` switch on nanoGPT.
- [plugyawn/NanoGPT-MoE](https://github.com/plugyawn/NanoGPT-MoE) - Compact char-level Transformer with MoE + Rotary attention + F-gram contextual augmentation.
**Cross-modal**
- [johnnygreco/midiGPT](https://github.com/johnnygreco/midiGPT) - minGPT applied to MIDI music generation.
- [deepanwadhwa/nanogpt-Audio](https://github.com/deepanwadhwa/nanogpt-Audio) - nanoGPT consuming EnCodec audio tokens.
- [sugiv/nanochat-audio](https://blog.sugiv.fyi/nanochat-audio) - \$5 multimodal extension of nanochat using Kyutai neural audio codecs.
**Walk-through reproductions**
- [EdIzaguirre/ChatGPT-from-Scratch](https://github.com/EdIzaguirre/ChatGPT-from-Scratch) - minGPT-driven walk through the original GPT papers.
### Graphify / Raw-folder-first
> Seed: 🪧 [raw/ folder tweet](https://x.com/karpathy/status/2039805659) (2026/04) - Treat the LLM Wiki's input as a graph of raw files first; compile last. Anti-RAG taken one step further.
- 🌟 [safishamsi/graphify](https://github.com/safishamsi/graphify) - Flagship graph-first compiler for raw markdown folders; **~40K★ in 26 days, 450K+ downloads**.
- [lucasrosati/claude-code-memory-setup](https://github.com/lucasrosati/claude-code-memory-setup) - Graph-based Claude Code memory layout; reports **71.5× token savings** on agent recall.
- [amarodeabreu/claude-graph-memory](https://github.com/amarodeabreu/claude-graph-memory) - Claude-side graph memory store; minimal companion to graphify.
- [memory-graph/memory-graph](https://github.com/memory-graph/memory-graph) - General-purpose memory-graph library reused by several forks.
- 📖 [Medium — LLM Wiki Codes: Graphify](https://medium.com/) - Companion explainer comparing graphify against MindStudio and [ai-chain.tw](http://ai-chain.tw).
### Agentic Engineering
> Seeds: 🪧 [Agentic Engineering inflection tweet](https://x.com/karpathy) (2026/02/25) + 📺 [Sequoia AI Ascent: From Vibe Coding to Agentic Engineering](https://www.youtube.com/watch?v=96jN2OCOfLs) (2026/04). The disciplined sibling of Vibe Coding — specs, evals, skills, and agent fleets instead of pure vibes.
- 📚 [jordimas/awesome-agentic-engineering](https://github.com/jordimas/awesome-agentic-engineering) - Curated list of Agentic Engineering tools, talks, and case studies.
- [software-mansion/agentic-engineering](https://github.com/software-mansion/agentic-engineering) - Production-grade Agentic Engineering scaffolding (skills + evals + safety).
- 📚 [EthicalML/awesome-agentic-engineering-resources](https://github.com/EthicalML/awesome-agentic-engineering-resources) - Ethical-ML community curation.
- [DimitriGeelen/agentic-engineering-framework](https://github.com/DimitriGeelen/agentic-engineering-framework) - Governance framework for AI coding agents; task traceability, structural gates, session continuity.
- [K-Dense-AI/karpathy](https://github.com/K-Dense-AI/karpathy) - Agentic ML Engineer scaffold (also cross-listed under [`CLAUDE.md` / Karpathy Skills](#claudemd--karpathy-skills)).
### HN Time Capsule
> Seed: 📖 [Auto-grading decade-old HN](http://karpathy.github.io/) (2025/12/10) + ⭐ [karpathy/hn-time-capsule](https://github.com/karpathy/hn-time-capsule). LLM-jury retrospective on old predictions.
- ⭐ [karpathy/hn-time-capsule](https://github.com/karpathy/hn-time-capsule) - Auto-grades 10-year-old Hacker News predictions with an LLM jury.
- [knowtrend.ai](http://knowtrend.ai) - Earnings-call retrospective grader; HN thread explicitly cites the Karpathy template.
### AI Job Exposure
> Seed: 🪧 AI Automation Risk Table tweet (deleted then restored, 2026) + ⭐ [karpathy/jobs](https://github.com/karpathy/jobs) ([live](http://karpathy.ai/jobs)). Per-occupation AI exposure scoring.
- ⭐ [karpathy/jobs](https://github.com/karpathy/jobs) - Karpathy's automation-risk-by-occupation table; live at [karpathy.ai/jobs](http://karpathy.ai/jobs).
- [JoshKale/jobs](https://github.com/JoshKale/jobs) - First public mirror captured before re-publication.
- [0xtreme/aus-jobs](https://github.com/0xtreme/aus-jobs) - Australia-specific fork with localized occupation taxonomy.
### Idea File
> Seed: 🪧 [`IDEA.md`](https://x.com/karpathy/status/2040470801506541998)[ tweet](https://x.com/karpathy/status/2040470801506541998) (2026/04/04). A per-repo idea log, sibling to `README.md` and `AGENTS.md`.
- [pithpusher/IDEA.md](https://github.com/pithpusher/IDEA.md) - CC0 standardization proposal for `IDEA.md`.
- 📚 [GitHub topic: idea-file](https://github.com/topics/idea-file) - Topic created post-tweet; collects early `IDEA.md` adopters.
### Micro seeds
> Single-project seeds kept together so they don't get lost.
- 🪧 [`HELLO.md` gist](https://gist.github.com/karpathy/) (2026/04/21) - "Agent free time" concept (27★ / 3 forks). No mature derivatives yet, but heavy discussion.
- [ranton256/microgpt_jl](https://github.com/ranton256/microgpt_jl) - Julia port of the [microgpt gist](https://gist.github.com/karpathy/8627fe009c40f57531cb18360106ce95).
- 📖 [Deep Neural Nets: 33 years ago](http://karpathy.github.io/2022/03/14/lecun1989/) (2022/03) → [teaching-on-testbeds/deep-nets-reproducing](https://github.com/teaching-on-testbeds/deep-nets-reproducing) - Classroom reproduction of LeCun 1989, plus Chameleon Cloud Trovi reproducible artifact.
### Concept citations layer
> Karpathy thought-pieces that mostly live as in-README citations rather than spawning their own sub-lineage. Listed here so contributors don't go looking for a missing subsection.
- 🪧 [The Space of Minds](https://x.com/karpathy) (2025/11/29) - Referenced in skills/wiki READMEs.
- 🪧 Animals vs Ghosts ([Dwarkesh Podcast 2025/10](https://www.dwarkeshpatel.com/)) - Referenced in agentic-engineering READMEs.
- 🪧 Verifiability tweet - Cited verbatim by [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills).
- 🪧 [LLM GUI / Generative UI tweet](https://x.com/karpathy/status/1917920257) (2025/04) - Later echoed by Google DeepMind's Gemini 3 generative UI work; no dedicated OSS faction yet.
- 📖 Power to the people (2025/04) - Commentary-heavy seed; no code projects.
- 📖 2025 LLM Year in Review - Anchor essay; widely cited.
- 📄 [arXiv:2601.07573 — A Model of Artificial Jagged Intelligence](https://arxiv.org/abs/2601.07573) - Academic operationalization of "jagged intelligence".
---

## Talks & Writings
### Long-form talks
- 📺 [Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g) (2023/11, 1h) - First systematic LLM-OS framing.
- 📺 [State of GPT](https://www.youtube.com/watch?v=bZQun8Y4L2A) (Microsoft Build 2023) - GPT training pipeline panorama.
- 📺 [Software is Changing (Again)](https://www.ycombinator.com/library/MW-andrej-karpathy-software-is-changing-again) (YC AI Startup School 2025) - Software 3.0 thesis.
- 📺 [Let's build GPT: from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY) (2023) - Companion to nanoGPT.
- 📺 [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI) (2025, 3.5h) - General-audience deep dive; no programming experience required.
- 📺 [Let's build the GPT Tokenizer](https://www.youtube.com/watch?v=zduSFxRajkE) (2024) - Companion to minbpe.
- 📺 [Let's reproduce GPT-2 (124M)](https://www.youtube.com/watch?v=l8pRSuU81PU) (2024, 4h) - Companion to llm.c.
### Blog posts
- 📖 [The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) (2015)
- 📖 [Deep Reinforcement Learning: Pong from Pixels](http://karpathy.github.io/2016/05/31/rl/) (2016)
- 📖 [Software 2.0](https://karpathy.medium.com/software-2-0-a64152b37c35) (2017)
- 📖 [A Recipe for Training Neural Networks](http://karpathy.github.io/2019/04/25/recipe/) (2019)
- 📖 [Vibe Coding MenuGen](https://karpathy.bearblog.dev/vibe-coding-menugen/) (2025)
- 📖 [2025 LLM Year in Review](https://karpathy.bearblog.dev/year-in-review-2025/) (2025) - Six paradigm shifts that reshaped LLM development.
### Key tweets
- 🪧 [LLM OS](https://x.com/karpathy/status/1723140519554105733) (2023/11)
- 🪧 [Vibe coding](https://x.com/karpathy/status/1886192184808149383) (2025/02)
- 🪧 LLM Wiki / `CLAUDE.md` / AutoResearch series (2025/12 → 2026/04) - see [@karpathy](https://x.com/karpathy).
---

## Timeline 2015 → 2026
| Date | Event | Lineage |
|---|---|---|
| 2015/05 | The Unreasonable Effectiveness of RNNs | char-rnn |
| 2015/12 | min-char-rnn gist | char-rnn |
| 2016/05 | Pong from Pixels essay + pg-pong gist | RL intro |
| 2017/11 | Software 2.0 essay | worldview |
| 2019/04 | A Recipe for Training NN | training SOP |
| 2020/08 | minGPT released | GPT minimal |
| 2022/12 | nanoGPT released | GPT minimal |
| 2023/02 | Zero-to-Hero lecture 1 (micrograd) | education |
| 2023/04 | llama2.c released | single-file inference |
| 2023/11 | Intro to LLMs + LLM OS tweet | LLM OS |
| 2024/02 | minbpe + Tokenizer video | tokenizer |
| 2024/04 | llm.c public | anti-PyTorch-necessity |
| 2024/06 | Reproduce GPT-2 (124M) 4h video | llm.c |
| 2024/07 | Eureka Labs founded | AI-native school |
| 2025/02 | Vibe coding tweet + MenuGen | Vibe Coding |
| 2025/06 | YC "Software is Changing (Again)" talk | Software 3.0 |
| 2025/01 | Deep Dive into LLMs like ChatGPT video | education |
| 2025/10 | nanochat released | full-stack ChatGPT |
| 2025/12 | 2025 LLM Year in Review blog post | reflection |
| 2025/12 | "Never been more behind" reflection tweet | Agentic Engineering setup |
| 2026/01 | Agentic engineering / `CLAUDE.md` series | `CLAUDE.md` |
| 2026/03 | autoresearch + microgpt gist | AutoResearch |
| 2026/04 | LLM Wiki gist + KarpathyTalk + reader3 | LLM Wiki / reading agent |
| 2026/04 | llm-council released | multi-model collaboration |
---

## Related Awesome Lists
Lists in adjacent ecosystems where Karpathy's ideas show up explicitly:
- 📚 [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) - 1000+ agent skills (Claude Code, Codex, Cursor, Gemini CLI, …) — many derive from Karpathy's `CLAUDE.md` framing.
- 📚 [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - Skills, hooks, slash-commands, plugins for Claude Code.
- 📚 [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - Claude Skills curation.
- 📚 [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) - 100+ specialized Claude Code subagents.
- 📚 [bilalonur/awesome-llm-os](https://github.com/bilalonur/awesome-llm-os) - LLM OS dedicated.
- 📚 [filipecalegario/awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding) - Vibe coding tools / projects / essays.
- 📚 [alvinreal/awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch) - AutoResearch dedicated (★1.7K).
- 📚 [sindresorhus/awesome](https://github.com/sindresorhus/awesome) - The mother list.
- 📚 [andrew/ultimate-awesome](https://github.com/andrew/ultimate-awesome) - Every awesome list, refreshed daily.
---

## Contributing
Contributions are welcome. Once this list lives on GitHub, see `CONTRIBUTING.md`. Until then the rules are:
**Inclusion criteria** (one of A / B / C must be satisfied):
- **A — Official**: maintained or published by Karpathy himself. No bar.
- **B — Direct derivative**: the project's own README/About explicitly says *inspired by / port of / based on* a Karpathy repo, video, or essay.
- **C — Concept derivative**: the project explicitly cites one of Karpathy's named concepts (Software 2.0/3.0, LLM OS, Vibe Coding, LLM Wiki, `CLAUDE.md`, AutoResearch, Recipe for Training NN, Pong from Pixels) with a link to the original source.
**Out of scope**:
- Projects only mentioned in third-party blog posts or comment threads, with no provenance in their own README.
- Archived repos with \<50 stars and no activity for 12+ months (multi-language ports excepted).
- Closed-source commercial products, unless they are an unavoidable node in the idea timeline.
**Entry format**:
```javascript
- [author/repo](https://github.com/author/repo) - One-line description ending with a period.
```
Use the appropriate prefix emoji from the [Legend](#legend). Add 🇨🇳 for Chinese-language projects. Multi-language ports go under [Multi-language ports](#multi-language-ports) (microgpt / minbpe / llm.c / llama2.c) or [GPT minimal derivatives](#gpt-minimal-derivatives--cross-modal) (minGPT / nanoGPT). New lineage require a matching idea seed in [Concepts & Manifestos](#concepts--manifestos).
**PR title**: `Add: author/repo` or `Update: author/repo`.
---

## Disclaimer
> **Warning**: This is a **curated list, not an audit**. Listed projects are created and maintained by their respective authors. We do not audit, endorse, or guarantee the security, correctness, or licensing of any listed project.
Community skills, agents, and `CLAUDE.md` files can contain prompt injections, tool poisoning, hidden payloads, or unsafe data-handling. Review every project (including its dependencies) yourself before installing or running it in a privileged environment.
Stars, forks, license, and maintenance status drift quickly. The data here was last reconciled on **2026-05-13** and must be re-verified before publishing.
---

## License
[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)]([https://creativecommons.org/publicdomain/zero/1.0/](https://creativecommons.org/publicdomain/zero/1.0/))
To the extent possible under law, the maintainer has waived all copyright and related or neighboring rights to this work. Original theory and quotations remain © Andrej Karpathy ([karpathy.ai](http://karpathy.ai)).
Upon publication to GitHub, this list will be released under [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/). Linked projects retain their own licenses (typically MIT or Apache-2.0).
---
