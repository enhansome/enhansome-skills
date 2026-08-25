# Awesome skills with stars

<div align="center">

<img src="https://img.alicdn.com/imgextra/i4/O1CN01VWH9Nq1SfXnTTVTCw_!!6000000002274-2-tps-1915-821.png" alt="Aliyun Model Studio AI Skills"  />

**The official Agent Skills collection for Aliyun Model Studio (DashScope) AI Platform**

[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-compatible-brightgreen.svg)](https://agentskills.io)
[![Node.js](https://img.shields.io/badge/node-%3E%3D18-brightgreen)](https://nodejs.org)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](LICENSE)

[Aliyun Model Studio CLI Site](https://bailian.console.aliyun.com/cli?source_channel=cli_github&) · [中文](./README.zh.md) · [API Documentation](https://help.aliyun.com/zh/model-studio/) · [Get API Key](https://bailian.console.aliyun.com/cn-beijing/?source_channel=key_github\&tab=app#/api-key)

***

*1st-party skills: core `bailian-cli` skill lives in [`modelstudioai/cli`](https://github.com/modelstudioai/cli) ⭐ 316 | 🐛 5 | 🌐 TypeScript | 📅 2026-08-25; this repo adds optional extensions. Pair with `bl` for Bailian's full-modal capabilities,*
*curated 3rd-party skills cover creation, dev, design, docs, and testing — pick and go.*

*Empowering AI Agents with a Skills collection curated and verified by the ModelStudio team.*

</div>

ModelStudio Skills is the official AI Agent Skills repository from ModelStudio, containing two categories:

* **1st-party skills** — Developed by the ModelStudio team. Install the core **`bailian-cli` skill** from [`modelstudioai/cli`](https://github.com/modelstudioai/cli) ⭐ 316 | 🐛 5 | 🌐 TypeScript | 📅 2026-08-25 (`npx skills add modelstudioai/cli --all -g`), then add optional extensions from this repo. Use with the [`bailian-cli`](https://www.npmjs.com/package/bailian-cli) npm package (`bl`; binary install: [bailian.aliyun.com/cli/install.md](https://bailian.aliyun.com/cli/install.md)), covering chat, multimodal, image/video, speech, vision, apps, memory, RAG, and web search on the Bailian platform.
* **Curated 3rd-party skills** — Continuously tracked from GitHub, Anthropic, Vercel, Google Labs, and other communities. Each Claude Code / Agent Skill is verified in real-world scenarios by the ModelStudio team; only those marked "usable" are included, grouped by use case for direct integration.

Each skill is an independent, composable workflow unit. The 3rd-party set spans **skill management, code development, design & creativity, documentation, video production, and testing** — six major scenarios.

***

## Quick Start

### Prerequisites

You need an **Aliyun Model Studio API Key** to run any skill that calls `bl` commands.

👉 [Get your free API Key](https://bailian.console.aliyun.com/cn-beijing/?source_channel=key_github\&tab=app#/api-key)

### Manual Install

```bash
npx skills add modelstudioai/skills
```

When prompted, select the skills you want to install, then press Enter to confirm.

### Install via Your Agent (Recommended)

Paste the following into your AI Agent:

```
Please install Bailian AI Skills for me:
1. Check if Node.js is installed (>= 18), install it if not
2. Run: npx skills add modelstudioai/skills
3. Once installed, start with "Bailian Skills installed", then list the installed skills and what I can do
```

***

## First-party skills in this repo

These skills ship with this repository and are maintained by the ModelStudio team. Install `modelstudioai/skills`, then let your Agent activate them as needed (unlike the **community index** in the next section).

| Skill                                                            | What it does                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`bailian-docs-llm-wiki`](./skills/bailian-docs-llm-wiki/)       | Routes the Agent through the in-repo **Bailian docs library** for model specs and pricing, API/error codes, agents/RAG/knowledge base, SDKs and multimodal, billing, etc. Start from `models/index.md` and `wiki/index.md`, then drill down.                                                                                                                                                                                                                           |
| [`bailian-model-recommend`](./skills/bailian-model-recommend/)   | **Model selection & recommendation**: given a scenario or feature need, picks the best-fit Bailian model and hands back ready-to-run sample code. Activates on "recommend / which model / compare." Reads the `models/` data from `bailian-docs-llm-wiki`.                                                                                                                                                                                                             |
| [`financial-expert`](./skills/financial-expert/)                 | **Financial data analysis** via `bl mcp` (`market-cmapi00073529`) for China and Hong Kong securities, funds, bonds, indices, global macro and industry series, broker research, company and fund announcements, financial news, and enterprise risk. Live tools include `NewsDataQuery` and `IcEnterpriseDataQuery`.                                                                                                                                                   |
| [`happyhorse-prompt-studio`](./skills/happyhorse-prompt-studio/) | **Interactive prompt studio for HappyHorse 1.0 video**: guides scenario discovery with vivid examples, then assembles production-ready prompts in JP/CN/EN. Covers manga drama, character PV, manga motion, virtual idol MV, and free-form scenarios.                                                                                                                                                                                                                  |
| [`spark-video`](./skills/spark-video/)                           | **End-to-end short-film production**: screenwriter ↔ director (per scene) → parallel render DAG → per-clip QA → stitch. Best for “make me an episode / a product ad in one go.” The entry skill registers as **`spark-video-episode`** (see [`SKILL.md`](./skills/spark-video/SKILL.md)).                                                                                                                                                                              |
| [`novel-game`](./skills/novel-game/)                             | **Novel-to-interactive-fiction game (React SPA)**: branching story engine + AI-generated character portraits & cutscenes (video or image) + optional TTS narration + procedural Web Audio music & SFX + localStorage save slots + multiple UI themes (pixel / cyberpunk / ink / minimalist). Activates on "interactive fiction / text adventure / visual novel / novel-to-game". Assets are generated offline via `bl video / image / speech`; runtime is fully local. |
| [`vox-video-director`](./skills/vox-video-director/)             | **End-to-end Vox-style paper-collage video production**: topic, talking-head video, or anchored photo → beat map → content-driven 5–10s segments → collage keyframes → motion → narration → captions and local ffmpeg assembly. Uses `bl image / video / speech` and pauses at approval gates before billable generation.                                                                                                                                              |

***

## Aliyun Bailian Curated Skills

The table below is an index of **curated community** projects verified by the Bailian team. Use the example prompts with your Agent, or install individually. The section above lists **first-party** skills bundled in this repository.

> See [`AWESOME_SKILLS.md`](./AWESOME_SKILLS.md) for detailed descriptions and category overviews.

| Category               | Skill                                                                            | Example Prompt                                                                             | Source                                                                                                                                      |
| ---------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 🛠️ Skill Management   | [skill-creator](./AWESOME_SKILLS.md#skill-creator)                               | Write me a Claude Code skill that analyzes why pet videos go viral on Xiaohongshu          | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 🛠️ Skill Management   | [find-skills](./AWESOME_SKILLS.md#find-skills)                                   | Find me a skill for making PPTs                                                            | [vercel-labs/skills](https://github.com/vercel-labs/skills) ⭐ 29,652 \| 🐛 1,119 \| 🌐 TypeScript \| 📅 2026-08-18                          |
| 🛠️ Skill Management   | [skills-mcp](./AWESOME_SKILLS.md#skills-mcp)                                     | Find me the latest AI skills                                                               | [skills-mcp/skills-mcp](https://github.com/skills-mcp/skills-mcp) ⭐ 27 \| 🐛 2 \| 🌐 TypeScript \| 📅 2025-10-20                            |
| 🛠️ Skill Management   | [skill-atlas](./AWESOME_SKILLS.md#skill-atlas)                                   | Run a competitive analysis between iPhone and Xiaomi phones                                | [GPTtang/skill-atlas](https://github.com/GPTtang/skill-atlas) ⭐ 4 \| 🐛 2 \| 🌐 TypeScript \| 📅 2026-03-22                                 |
| 🛠️ Skill Management   | [skills\_repository](./AWESOME_SKILLS.md#skills_repository)                      | Find me a skill for project planning                                                       | [diao10/skills\_repository](https://github.com/diao10/skills_repository) ⭐ 0 \| 🐛 0 \| 📅 2026-04-09                                       |
| 🛠️ Skill Management   | [ai-toolkit](./AWESOME_SKILLS.md#ai-toolkit)                                     | Create a Feishu learning doc on Cocos Creator development                                  | [mwpgxl/ai-toolkit](https://github.com/mwpgxl/ai-toolkit)                                                                                   |
| 🛠️ Skill Management   | [shaoqi-marketplace](./AWESOME_SKILLS.md#shaoqi-marketplace)                     | Do market analysis and pricing strategy for ergonomic chairs                               | [ceoniuer/shaoqi-marketplace](https://github.com/ceoniuer/shaoqi-marketplace) ⭐ 0 \| 🐛 0 \| 📅 2026-03-10                                  |
| 🛠️ Skill Management   | [servasyy\_skills](./AWESOME_SKILLS.md#servasyy_skills)                          | Write and lay out a WeChat article for our school anniversary                              | [huangserva/servasyy\_skills](https://github.com/huangserva/servasyy_skills) ⭐ 161 \| 🐛 1 \| 🌐 Python \| 📅 2026-02-05                    |
| 🛠️ Skill Management   | [AI-Vibe-Writing-Skills](./AWESOME_SKILLS.md#ai-vibe-writing-skills)             | Rewrite this copy to remove the AI feel                                                    | [donghuixin/AI-Vibe-Writing-Skills](https://github.com/donghuixin/AI-Vibe-Writing-Skills) ⭐ 487 \| 🐛 0 \| 🌐 Python \| 📅 2026-06-02       |
| 🛠️ Skill Management   | [marketing-writer](./AWESOME_SKILLS.md#marketing-writer)                         | Write marketing copy for the Laifen hair dryer                                             | [gushuaialan1/marketing-writer](https://github.com/gushuaialan1/marketing-writer) ⭐ 0 \| 🐛 0 \| 🌐 Python \| 📅 2026-03-20                 |
| 🛠️ Skill Management   | [social-media-skills](./AWESOME_SKILLS.md#social-media-skills)                   | Plan a social media content strategy                                                       | [blacktwist/social-media-skills](https://github.com/blacktwist/social-media-skills) ⭐ 437 \| 🐛 5 \| 🌐 Shell \| 📅 2026-05-01              |
| 🛠️ Skill Management   | [multi-agent-content](./AWESOME_SKILLS.md#multi-agent-content)                   | Use multi-agent collaboration to write a long essay on "missing home"                      | [gonelake/multi-agent](https://github.com/gonelake/multi-agent) ⭐ 4 \| 🐛 0 \| 🌐 Python \| 📅 2026-03-30                                   |
| 🛠️ Skill Management   | [finance-skills](./AWESOME_SKILLS.md#finance-skills)                             | Write a viral finance article on recent fund gains                                         | [digoal/blog](https://github.com/digoal/blog/tree/master/skills) ⭐ 8,564 \| 🐛 123 \| 🌐 HTML \| 📅 2026-08-25                              |
| 🛠️ Skill Management   | [gptzero-mcp](./AWESOME_SKILLS.md#gptzero-mcp)                                   | Check whether this text is AI-generated                                                    | [louis030195/gptzero-mcp](https://github.com/louis030195/gptzero-mcp) ⭐ 1 \| 🐛 0 \| 🌐 JavaScript \| 📅 2025-10-06                         |
| 💻 Code Development    | [mcp-builder](./AWESOME_SKILLS.md#mcp-builder)                                   | Build me an MCP Server so Claude can call weather-related services                         | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 💻 Code Development    | [goframe-v2](./AWESOME_SKILLS.md#goframe-v2)                                     | Write a login API in GoFrame v2                                                            | [gogf/skills](https://github.com/gogf/skills) ⭐ 78 \| 🐛 2 \| 🌐 Go \| 📅 2026-06-05                                                        |
| 🎨 Design & Creativity | [shadcn-ui](./AWESOME_SKILLS.md#shadcn-ui)                                       | Build a chat room page with the shadcn-ui component library                                | [google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills) ⭐ 8,177 \| 🐛 16 \| 🌐 TypeScript \| 📅 2026-08-17      |
| 🎨 Design & Creativity | [ui-ux-pro-max](./AWESOME_SKILLS.md#ui-ux-pro-max)                               | Design a personal blog UI in one of 50 styles                                              | [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) ⭐ 30,390 \| 🐛 235 \| 🌐 Python \| 📅 2026-08-25          |
| 🎨 Design & Creativity | [canvas-design](./AWESOME_SKILLS.md#canvas-design)                               | Design a visual poster themed around freedom and butterflies                               | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 🎨 Design & Creativity | [frontend-design](./AWESOME_SKILLS.md#frontend-design)                           | Design a high-quality promotional page for a Xiaomi phone                                  | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 📝 Documentation       | [internal-comms](./AWESOME_SKILLS.md#internal-comms)                             | Write a team weekly report for the first week of May 2026                                  | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 📝 Documentation       | [xlsx/docx/pdf/pptx](./AWESOME_SKILLS.md#office-suite-xlsx--docx--pdf--pptx)     | Make a PPT on domestic indie cosmetics sales for the full year 2025                        | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 📝 Documentation       | [doc-coauthoring](./AWESOME_SKILLS.md#doc-coauthoring)                           | Write a technical design doc — structured, produced in three stages                        | [anthropics/skills](https://github.com/anthropics/skills) ⭐ 171,520 \| 🐛 1,152 \| 🌐 Python \| 📅 2026-08-21                               |
| 🎬 Video Production    | [spark-video](./AWESOME_SKILLS.md#spark-video)                                   | Make a product ad video — here's the product image, with the selling point in one sentence | [JohnKeating1997/spark-video](https://github.com/JohnKeating1997/spark-video) ⭐ 32 \| 🐛 1 \| 🌐 Python \| 📅 2026-07-17                    |
| 🎬 Video Production    | [shanyin-screenwriting-master](./AWESOME_SKILLS.md#shanyin-screenwriting-master) | Make a live-action video of the Little Red Riding Hood story                               | [Shanyin-ai/shanyin-screenwriting-master](https://github.com/Shanyin-ai/shanyin-screenwriting-master) ⭐ 1,001 \| 🐛 2 \| 📅 2026-04-01      |
| 🧪 Testing & Quality   | [e2e-testing](./AWESOME_SKILLS.md#e2e-testing)                                   | Write e2e tests covering signup → login → browsing → cart → checkout                       | [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) ⭐ 243,117 \| 🐛 182 \| 🌐 JavaScript \| 📅 2026-08-25 |

***

## License

This repository's code is released under the [Apache-2.0](./LICENSE) license.

## 📖 Full Tutorial

Step-by-step setup, hands-on walkthroughs, and end-to-end examples are on our docs site:

**[modelstudioai.github.io/guide/](https://modelstudioai.github.io/guide/)**

***

> **Disclaimer** — These skills instruct your Agent to call DashScope / Bailian APIs via `bl` on your behalf, billed to your Alibaba Cloud account. Generated content may be inaccurate — review before use. Keep your API key secure. This project is provided as-is, without warranties.

*Maintained by the Aliyun Bailian team. We respect the copyrights and licenses of each Skill's upstream author; all references retain the original License and Attribution. If you find any content infringing or inappropriate, please file an Issue to contact us.*

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-25._
