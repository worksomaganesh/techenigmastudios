# TECHENIGMASTUDIOS Video Engine

## Purpose

Build a reusable, faceless educational-video renderer for TECHENIGMASTUDIOS. The engine should turn an approved, structured episode plan into consistent black-and-yellow educational scenes, then export a reviewable video master.

**The renderer is a production tool, not the editorial brain.** Gemini/Codex help research, draft and structure an episode. The engine renders only an approved production plan.

## Current decisions

- Brand: TECHENIGMASTUDIOS.
- Presentation: faceless, English narration, visual-first.
- Palette: pure black `#000000` and yellow `#FFD400`.
- Primary renderer direction: Remotion (React + TypeScript) for reusable, data-driven scenes.
- Optional quick-motion direction: self-contained HTML/CSS/GSAP for suitable scenes.
- Diagram assets: original SVG/HTML, with a brand-specific diagram design profile.
- Optional generated footage: Google Flow. It is an ingredient, not a required dependency.
- Media processing and validation: FFmpeg + ffprobe.
- Human finishing: DaVinci Resolve remains the final editorial environment.

## Architecture

```text
Approved research + claim/source map
            |
            v
Approved narration and captions
            |
            v
Storyboard + production-plan JSON
            |
            +-------------------------+
            |                         |
            v                         v
Remotion scenes / SVG diagrams   Optional media assets
HTML-GSAP scenes                 Flow clips / screen capture
            |                         |
            +------------+------------+
                         v
               Frame-accurate render
                         |
                         v
                 FFmpeg / ffprobe
                         |
                         v
            Contact sheets + Render QA
                         |
                         v
                DaVinci Resolve
                         |
                         v
             Human-approved platform master
```

## Why code-rendered animation is the default

1. Deterministic diagrams are better for explaining tokenisation, embeddings, attention, model pipelines and technical comparisons than unrelated cinematic footage.
2. A single tested scene component can be reused across many lessons without rewriting the entire video.
3. Captions, typography, timing, colour and safe areas can be validated programmatically.
4. The pipeline is not limited by monthly AI-video credits.
5. Google Flow can still create occasional supporting shots when motion generation genuinely improves the lesson.

## Core scene families

- Hook / question opener.
- Kinetic typography.
- Concept definition / annotated visual.
- Process and architecture diagram.
- Data / token / vector transformation.
- Side-by-side comparison.
- Screen recording with highlighted interface areas.
- Example / demonstration.
- Caveat / limitation.
- Takeaway / end card.

## Production contract

Each scene should declare:

- `scene_id`, order, start/end or duration;
- narration and on-screen/caption text;
- learning beat and visual direction;
- render mode and composition;
- asset IDs and rights/provenance;
- source/claim IDs;
- transitions and continuity notes;
- accessibility and safe-area requirements.

The production JSON must validate against the shared Creator-OS production-plan schema before rendering. A renderer must never infer missing technical facts.

## Quality workflow

1. Validate brief and source/claim references.
2. Approve narration and storyboard.
3. Render the opening 5–10 seconds or first representative scene group.
4. Review a contact sheet and preview for mobile readability, pacing, diagram accuracy and brand consistency.
5. Render the full episode at explicit timestamps/frame numbers.
6. Run FFmpeg/ffprobe checks and inspect scene-boundary/mid-scene frames.
7. Finish in DaVinci Resolve, listen to the full narration, and re-check captions.
8. Human approves the final export and platform package.

## Hardware and cost policy

- Start with 1080×1920 output and modest render concurrency; increase only after tests on the current laptop.
- Prefer SVG/HTML/Remotion for diagrams and text, not large local generative models.
- Use Flow selectively and record estimated/actual credit usage in the asset manifest.
- Keep raw clips, rendered frames, caches and final masters outside Git.
- Keep provider keys in environment/approved secret storage, never in source files.

## External architecture references

- [Bang Motion](https://github.com/bangtutorial/bang-motion) — MIT; motion design rules, continuous visual world, controlled browser timeline and frame export.
- [diagram-design](https://github.com/cathrynlavery/diagram-design) — MIT; semantic diagram selection and brand profiles.
- [anything2explainer](https://github.com/Vincentwei1021/anything2explainer) — research/storyboard/scene/QC architecture reference only. Its PolyForm Noncommercial licence blocks use of its toolkit for commercial work without author permission.
- [Vox Director](https://github.com/Alisa0808/vox-director) — MIT; staged assets and assembly pattern, but its Atlas Cloud API is not a current dependency.

See the [Creator-OS repository evaluation](https://github.com/worksomaganesh/Creator-OS/blob/main/references/evaluated-repositories.md) for all reviewed projects, licence notes and adoption decisions.

## Status

Architecture approved for implementation planning. Renderer source code, scene components, automated tests and the Episode 001 media render have not yet been built. Do not describe the engine as operational until a pilot render and QA run have passed.