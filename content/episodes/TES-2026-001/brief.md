# TES-2026-001 — Episode 001 Brief

## Status

- Editorial status: active pre-production.
- Research status: reviewed; seven-stage brief, 18 Claim IDs and 22-entry source register documented.
- Narration v1: reviewed by Argon 4; verdict was APPROVED WITH MINOR CORRECTIONS.
- Narration v2: mandatory corrections applied; fresh technical re-audit pending.
- Storyboard v1: provisional; scene timings require validation against the actual voiceover.
- Animation/pilot status: not started.
- Full production/render status: not started.
- Publishing status: not scheduled.
- Priority: first production pilot; opportunity score remains provisional.

## Working title

**What Actually Happens When You Press Send? — Inside the Journey of a Prompt Through an LLM**

## Brand and audience

- Brand: TECHENIGMASTUDIOS.
- Pillar: Generative AI.
- Format: faceless, narration-led, visual-first explainer.
- Audience: AI beginners, students and aspiring AI/ML engineers.
- Language: English.
- Locked planning target: 60 seconds; final runtime must be measured against the selected voiceover and visual holds.

## Audience question

When I submit a prompt to an LLM, what happens between pressing Send and seeing the answer?

## Learning outcome

The viewer should understand a simplified inference path for a typical text-generating LLM: input text and conversation context are prepared, tokenised, mapped to model representations, processed through a transformer, used to produce next-token scores/selections, and decoded into readable output.

## Technical scope and caveats

Teach a simplified text-generation path, not claim that every deployed assistant uses exactly the same internals. Real products may add system instructions, conversation history, safety filters, routing, tool calls, retrieval, post-processing and other orchestration. Tokenisation and token IDs are model/tokeniser-specific. Do not imply that embeddings are a separate compulsory stage in every implementation; explain the relationship accurately. Next-token generation is iterative, and decoding/sampling choices affect the result.

## Candidate visual sequence

1. **The prompt arrives:** a message enters the system.
2. **Input preparation:** show conversation/context joining the current message, while marking that product pipelines differ.
3. **Tokenisation:** visually split text into token pieces.
4. **Numerical representation:** show token IDs and learned embeddings without implying a universal visual one-to-one mapping.
5. **Transformer processing:** show attention and repeated model layers processing contextual representations.
6. **Output generation:** show a probability/logit distribution and one selected next token, then repeat the generation loop.
7. **Decoding:** token IDs become readable output text.
8. **Reality check:** a deployed assistant may add tools, safety and orchestration around the model.

## Opening hook direction

“You press Send. What actually happens next?”

Do not use the hook “AI doesn't read words the way you do” unless the script immediately clarifies the analogy and avoids implying human-like reading. The question-led hook is more precise.

## Visual direction

- Pure black `#000000` background.
- Signal yellow `#FFD400` for text, token blocks, arrows and focus states.
- No generic robot/brain stock footage.
- Use one coherent animated visual world: prompt panel → token blocks → model layers → output sequence.
- Use original diagrams and deterministic motion as the default; Google Flow is optional and should only be used for a short supporting visual if it adds explanatory value.
- Keep text sparse and legible in 9:16 safe areas.

## Research evidence and gaps

- Google documentation explains that LLM inputs/outputs are processed as tokens: https://ai.google.dev/gemini-api/docs/tokens
- Primary architecture reference: Vaswani et al., “Attention Is All You Need”: https://arxiv.org/abs/1706.03762
- Competitor reference: https://www.youtube.com/watch?v=tAhmBB_LSsc
- Competitor reference: https://www.youtube.com/watch?v=MjCJIJ4PuSw
- Competitor reference: https://www.youtube.com/watch?v=Y3zHPQ0Ir3k
- A previous exploratory review found existing coverage, so do not claim that the subject is underserved. The opportunity hypothesis is visual clarity, a compact learning sequence and accurate connection to the inference pipeline.
- Google Trends quantitative comparison and first-party YouTube Studio evidence are still outstanding. Update the opportunity score only when evidence is recorded.

## Provisional opportunity score

Exploratory score: **83/100**, not a validated market score. Demand and relevance were provisionally high; the supply-gap score was deliberately conservative because established explanations already exist. Reassess against the canonical Creator-OS opportunity rubric and record evidence before moving to `validated`.

## Current production state

- Research dossier: complete and reviewed.
- Narration v1: reviewed with minor mandatory corrections.
- Narration v2: revised draft, pending fresh technical review.
- Storyboard v1: provisional scene plan.
- Current next gate: obtain an independent Argon 4 review of narration v2 before locking the script.

See the [production journey log](production-log.md), [revised research dossier](research/dossier-revised-clean.html), [narration v1](scripts/narration-v1.md), [narration v2](scripts/narration-v2.md), and [storyboard v1](storyboard/storyboard-v1.md).

## Required production outputs

- Research brief and claim/source map.
- Approved narration.
- Storyboard and production-plan JSON.
- Voiceover and timed captions.
- Branded motion scenes.
- Contact sheet and render QA report.
- Final 9:16 master and platform-specific publishing package.

## Explicit non-goals

- Do not generate the video from an unreviewed paragraph.
- Do not copy another creator's script, diagrams or footage.
- Do not assume all LLM products have identical internal request paths.
- Do not generate the final MP4 in this brief step.
- Do not publish or schedule until a human approves the finished export.