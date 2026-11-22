# TECHENIGMASTUDIOS — Project Handoff

**Last updated:** 22 November 2026  
**Repository:** https://github.com/worksomaganesh/techenigmastudios  
**Brand promise:** Decode. Understand. Build.

## 1. What this repository is

TECHENIGMASTUDIOS is an English-language, faceless technology education brand. Its visual identity is pure black (#000000) and yellow (#FFD400). Content is narration-led and visual-first: original diagrams, motion graphics, kinetic typography, screen recordings and practical demonstrations. No human on-camera presenter.

Nine content pillars:
1. Artificial Intelligence
2. Machine Learning
3. Generative AI
4. Data Science
5. Cybersecurity
6. Technology career roadmaps
7. Deep Learning
8. Fine-Tuning
9. Feature Engineering

This repository owns this brand's strategy, curriculum, episode content and production artifacts. [Creator-OS](https://github.com/worksomaganesh/Creator-OS) owns shared cross-brand workflows, reusable skills, schemas and operating practices.

## 2. External repository research

The complete historical list of 22 repositories and the brand-specific decisions are documented in [references/repository-landscape.md](references/repository-landscape.md). The detailed technical/licence evaluation remains canonical in [Creator-OS — evaluated repositories](https://github.com/worksomaganesh/Creator-OS/blob/main/references/evaluated-repositories.md).

Primary design references:
- [Bang Motion](https://github.com/bangtutorial/bang-motion): continuous motion-design patterns and deterministic frame rendering ideas (MIT).
- [diagram-design](https://github.com/cathrynlavery/diagram-design): semantic diagram selection and HTML/SVG output patterns (MIT).

Architecture/workflow references only:
- [anything2explainer](https://github.com/Vincentwei1021/anything2explainer): research-to-Remotion explainer pipeline. PolyForm Noncommercial; no commercial code/template reuse without permission.
- [Vox Director](https://github.com/Alisa0808/vox-director): staged media workflow; Atlas Cloud is a separate dependency.
- [VoiceStudio](https://github.com/debpalash/VoiceStudio): optional future voice lab; AGPL-3.0 and per-model licence checks required.
- [OpenCreator](https://github.com/krillinai/OpenCreator): revisit later; not a current dependency.

Do not adopt Instagram engagement bots, unofficial private APIs, scraping workflows, follower/liker harvesting, proxy/rate-limit evasion or third-party creator-media downloading. The public repository list is not an installation list.

## 3. Current production stack and constraints

- Research/script planning: Gemini models available in the user's Google AI Pro workflow; do not assume subscription includes unlimited API usage.
- Coding, tests and deterministic automation: Codex.
- Main code renderer: Remotion + React + TypeScript.
- Optional quick motion prototypes: original HTML/CSS/GSAP.
- Technical diagrams: original SVG/HTML.
- Generated footage: Google Flow only where a scene genuinely benefits; not required for every scene.
- Media processing/validation: FFmpeg and ffprobe.
- Final finishing: DaVinci Resolve.
- Publishing: human-approved; use native platform tools or permitted official APIs.
- Do not copy code/assets/models/templates without checking licences and terms. In particular, anything2explainer's PolyForm Noncommercial toolkit must not be reused commercially without author permission.

## 4. Episode 001 — current state

**Title:** What Actually Happens When You Press Send? — Inside the Journey of a Prompt Through an LLM.  
**Target:** 60 seconds, 9:16 vertical, 1080 × 1920, English narration, black/yellow visual identity.

Research is documented in:
- `content/episodes/TES-2026-001/research/dossier-revised-clean.html`
- `content/episodes/TES-2026-001/research/argon-script-review-v1.md`

The research dossier covers seven stages and Claim IDs C001–C018. The Argon review of narration v1 returned **APPROVED WITH MINOR CORRECTIONS**. That verdict applies to v1 only.

Narration files:
- `scripts/narration-v1.md`: reviewed 117-word draft.
- `scripts/narration-v2.md`: revised draft with mandatory corrections; **fresh technical re-audit pending**. Do not mark v2 approved until Argon reviews the exact v2 file alongside the complete dossier.

Storyboard:
- `storyboard/storyboard-v1.md`: provisional; must be reconciled with the finally approved narration and actual measured voiceover timing.
- `storyboard/visual-reference-queries.md`: inspiration queries only, not approved footage/assets.

No animation source, voiceover recording, final MP4 or final QA report has been produced yet. Do not claim rendering has started or that the pilot is complete.

## 5. Immediate next actions

1. Upload the clean revised research dossier and exact `narration-v2.md` to Gemini Argon 4.
2. Ask for a fresh sentence-by-sentence audit against C001–C018 and Research Brief Stage 5; require a clear verdict for v2.
3. Preserve Argon's exact prompt and complete output in the episode's `prompts/` and `research/` folders. Update `production-log.md` with the date, model, input files, output, verdict and decision.
4. If approved, lock the narration version and update the episode brief.
5. Revise storyboard timings to the locked narration; estimate first, then measure using the actual voice recording/TTS.
6. Build a 5–10 second visual pilot before the full minute. Initial pilot scenes: hook and tokenization, to test two different animation styles.
7. Review typography, composition, motion, lighting, brand palette, narration sync, safe areas and rendering quality. Record feedback and revisions.
8. Only after pilot approval, build the remaining scenes and render the full episode.
9. Run technical/content QA, finish in DaVinci Resolve, and record final export metadata and approval before publishing.

## 6. Production journal rule

This repository preserves the journey, not only final deliverables. For every episode, retain:
- exact prompts sent to each model/agent;
- original model outputs (do not silently overwrite);
- source documents, URLs, dates and claim mappings;
- review reports and model verdicts;
- corrections, alternatives and reasons for decisions;
- script/storyboard/production-plan versions;
- code changes, test output, render logs, contact sheets and QA evidence;
- final assets and publishing approval metadata.

Keep secrets, API keys, passwords, session cookies, private account data and unnecessary personal data out of Git. Large binary media should be managed outside normal Git history or through an intentionally chosen asset-storage/LFS strategy.

Use the [Episode Production Journal Standard](docs/production-journal-standard.md) for every new episode. Use [content/episodes/TES-2026-001/production-log.md](content/episodes/TES-2026-001/production-log.md) as the current chronological record.

## 7. Key repository entry points

- [README](README.md)
- [Brand guide](brand/brand-guide.md)
- [Video engine architecture](video-engine/README.md)
- [External repository landscape](references/repository-landscape.md)
- [External tool review](references/external-tool-review.md)
- [Production journal standard](docs/production-journal-standard.md)
- [Episode 001 brief](content/episodes/TES-2026-001/brief.md)
- [Episode 001 production log](content/episodes/TES-2026-001/production-log.md)

## 8. Handoff rule

When work is handed to another model, agent or human, provide the exact repository paths, current version/status, source files to read, allowed scope, acceptance criteria and files that must be updated. The receiving agent must inspect the repository state before editing and must not assume an earlier chat summary overrides committed artifacts.
