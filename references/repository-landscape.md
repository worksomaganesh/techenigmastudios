# External Repository Landscape — TECHENIGMASTUDIOS

**Scope:** The complete set of 22 external GitHub repositories previously supplied for technical review.  
**Purpose:** Preserve the research list in this brand repository and make each project's relevance and adoption decision discoverable.  
**Canonical deep review:** [Creator-OS evaluated repository register](https://github.com/worksomaganesh/Creator-OS/blob/main/references/evaluated-repositories.md). That file contains the detailed architecture, licence/dependency notes, limitations and per-repository rationale. This brand-level register intentionally keeps the full list visible here.

> A repository being listed does not mean it is approved, installed, safe, or licensed for reuse. Re-check its current licence, third-party assets, model terms, security, maintenance, provider costs and platform rules before adopting anything.

## Complete historical list (22 repositories)

| # | Repository | Primary area reviewed | TECHENIGMASTUDIOS decision |
|---:|---|---|---|
| 1 | [wide-trace/open-higgsfield](https://github.com/wide-trace/open-higgsfield) | Multi-provider image/video generation studio; model catalog, provider adapters, run history and asset library | Reference only. Provider-catalog ideas may inform a future multi-provider adapter. No code reuse; licence was not located in the review. It does not replace Google Flow or provide Flow credits. |
| 2 | [debpalash/voicestudio](https://github.com/debpalash/VoiceStudio) | Local-first voice studio; engine adapters, model manager, batch jobs, transcription, voice design/cloning and MCP/API | Optional future voice lab. Application is AGPL-3.0; model/weight licences are separate. Default OmniVoice weights were identified as non-commercial. |
| 3 | [every-app/open-seo](https://github.com/every-app/open-seo) | SEO research through MCP/skills: keywords, competitors, rank tracking, backlinks and AI visibility | Revisit after launch if data costs are justified. DataForSEO or reseller access is a separate dependency. |
| 4 | [Tencent/WeKnora](https://github.com/Tencent/WeKnora) | Knowledge/RAG system with hybrid retrieval, citations, knowledge curation/versioning, MCP and audit patterns | Architecture reference only. Borrow source traceability and knowledge-versioning ideas; full deployment is excessive for the current workflow. |
| 5 | [opf/openproject](https://github.com/opf/openproject) | Enterprise project/portfolio management, roadmaps, Gantt and agile workflows | Do not adopt. Duplicates the current Creator-OS operating workflow; GPLv3 and substantial deployment overhead. |
| 6 | [InstaPy/InstaPy](https://github.com/InstaPy/InstaPy) | Instagram likes, comments and follows automation | Reject. No automated engagement or growth bots. GPLv3; README documents creator account-ban context. |
| 7 | [GramAddict/bot](https://github.com/GramAddict/bot) | Android/ADB Instagram likes, follows, comments, DMs and scraping modes | Reject. No engagement automation, scraping or account-risk patterns. |
| 8 | [karthiktadepalli1/claudegram](https://github.com/karthiktadepalli1/claudegram) | Claude-powered AI-text detection extension | Not relevant. AI-detector outputs are not proof of authorship or quality; also requires a Claude Code workflow not in the current stack. |
| 9 | [drawrowfly/instagram-scraper](https://github.com/drawrowfly/instagram-scraper) | Unofficial Instagram scraping of posts, comments, likers, followers and media (InstaTouch) | Reject for our research pipeline. No private/session data harvesting, rate-limit evasion or third-party media downloading. |
| 10 | [althonos/InstaLooter](https://github.com/althonos/InstaLooter) | Legacy API-less Instagram media downloader | Reject. Legacy downloader, GPLv3+, old Python compatibility targets; no role in original educational production. |
| 11 | [subzeroid/instagrapi](https://github.com/subzeroid/instagrapi) | Unofficial Instagram private/mobile API, sessions, interactions, uploads and insights | Reject for automation/scraping. Do not store session IDs/passwords or use private endpoints; use official APIs for permitted account-owned workflows. |
| 12 | [Alisa0808/vox-director](https://github.com/Alisa0808/vox-director) | Staged media generation, beat maps, keyframes, voice/caption assembly and FFmpeg | Borrow workflow gates and production-manifest ideas only. Atlas Cloud is a separate dependency and not part of Google AI Pro. |
| 13 | [lintsinghua/paint-mv-skills](https://github.com/lintsinghua/paint-mv-skills) | Director/storyboard/animation/render skill separation, chapter parallelism, contact sheets and resumable renders | Borrow generic orchestration and QC patterns only. Music-video format is not our format; do not reuse the downloaded upstream PDoomVideo engine because its licence was not declared. |
| 14 | [Vincentwei1021/anything2explainer](https://github.com/Vincentwei1021/anything2explainer) | Research-to-narration-to-storyboard-to-Remotion scenes and frame-level QC | Architecture reference only. PolyForm Noncommercial; do not reuse its code/templates commercially without prior permission. Build an independent pipeline. |
| 15 | [bangtutorial/bang-motion](https://github.com/bangtutorial/bang-motion) | Continuous motion design, style briefs, HTML/CSS/GSAP and deterministic browser-frame export | Primary motion-design reference. MIT; use general patterns to build original brand-specific scenes. |
| 16 | [kurbaitaev/ghost-editor](https://github.com/kurbaitaev/ghost-editor) | Talking-head short-form editing, captions, B-roll and QA | Do not adopt as a production tool: TECHENIGMASTUDIOS is faceless. Borrow measurable audio/caption/export QA ideas only. |
| 17 | [LPengYang/MotionClone](https://github.com/LPengYang/MotionClone) | Training-free motion transfer with Stable Diffusion 1.5/AnimateDiff | Research reference only. Specialised checkpoints/hardware; no top-level licence was located in the review. Not needed for current Flow + code-motion stack. |
| 18 | [krillinai/OpenCreator](https://github.com/krillinai/OpenCreator) | Codex-native runtime, workspace, shared run state, approvals, skills and MCP | Revisit later as a possible interface/runtime reference. Do not duplicate or replace Creator-OS now. |
| 19 | [fluxcd/flux2](https://github.com/fluxcd/flux2) | Kubernetes GitOps controllers and declarative cluster reconciliation | Not relevant now. No Kubernetes deployment requirement in this creator operation. |
| 20 | [souzatharsis/podcastfy](https://github.com/souzatharsis/podcastfy) | Multimodal source-to-multi-speaker podcast/audio generation | Future repurposing option after a long-form lesson library exists; not the current Reel renderer. |
| 21 | [langchain-ai/social-media-agent](https://github.com/langchain-ai/social-media-agent) | LangGraph URL-to-post workflow with human-in-the-loop edit/accept/reject | Borrow the human approval pattern only. Full dependency stack is unnecessary; publishing remains human-approved. |
| 22 | [cathrynlavery/diagram-design](https://github.com/cathrynlavery/diagram-design) | Semantic-pattern-first diagram selection, brand profiles and HTML/SVG outputs | Primary diagram-design reference. MIT; create original diagrams using the TECHENIGMASTUDIOS black/yellow identity. |

## Patterns carried into our own system

1. **Research-to-production traceability:** source-backed research, claim IDs, narration, storyboard, scene implementation and QA should remain connected.
2. **Code-driven visual production:** use Remotion/React/TypeScript as the main reusable renderer; use original HTML/CSS/GSAP prototypes when appropriate.
3. **Technical diagrams:** create original SVG/HTML diagrams with semantic structure and the brand's black/yellow design system.
4. **Human approval gates:** review research, narration, first visual pilot and final export before publishing or expensive generation.
5. **Deterministic media QA:** use contact sheets, representative frames, FFmpeg/ffprobe, audio/caption checks, safe-area checks and export validation.
6. **Replaceable providers:** voice, image and video generation should sit behind replaceable adapters. Google Flow is optional supporting footage, not a renderer dependency.
7. **Safe platform research:** use public search, native platform tools and permitted official APIs. Do not automate likes/follows/comments/DMs, bypass rate limits, harvest follower/liker lists, use unofficial private endpoints, or download third-party creators' media for reuse.

## Current implementation direction

- Research and script planning: Gemini models; exact prompts and outputs are preserved in each episode journal.
- Code, tests and render tooling: Codex.
- Main renderer: Remotion with React/TypeScript.
- Motion prototypes: original HTML/CSS/GSAP where efficient.
- Diagrams: original SVG/HTML.
- Optional generated clips: Google Flow when a scene benefits from them.
- Media processing and validation: FFmpeg/ffprobe.
- Final finishing: DaVinci Resolve.
- Human review and publishing approval remain mandatory.

## Review limitations

This is a record of the earlier repository review, not a fresh security audit, runtime test, legal opinion or guarantee that upstream state has not changed. Confirm current licences, dependencies, terms and security before installing or reusing any project. A public GitHub repository is not automatically a safe or licensed dependency.

**Last consolidated:** 22 November 2026.
