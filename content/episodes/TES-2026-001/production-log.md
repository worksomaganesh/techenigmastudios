# TES-2026-001 — Production Journey Log

This is the chronological record for Episode 001. It records source artifacts, prompts, generated drafts, review findings, corrections and production decisions. A later version must not overwrite an earlier version.

## Project constants

- Working title: What Actually Happens When You Press Send? — Inside the Journey of a Prompt Through an LLM.
- Target duration: 60 seconds.
- Format: 9:16 vertical, 1080 × 1920.
- Language: English.
- Presentation: faceless, narration-led, visual-first.
- Brand palette: black (#000000) and yellow (#FFD400), with white supporting text.
- Audience: AI beginners, students and aspiring AI/ML engineers.
- Topic scope: simplified inference path through a typical text-generating LLM; not a verified internal diagram of any closed consumer assistant.

## 2026-11-22 — Research and evidence

1. A seven-stage technical research dossier was prepared with a Claim–Evidence Matrix (C001–C018), seven visualisation opportunities, an accuracy/risk report and a source register.
2. The initial dossier was delivered as HTML with two embedded base64 image data URIs. Gemini attachment handling reported truncation inside the embedded image data, so the research sections and tables were not available to the reviewer.
3. A text-safe copy was prepared by removing the two embedded base64 image payloads while retaining the dossier's textual sections, tables, claims and exact source URLs. The cleaned HTML is stored in research/dossier-revised-clean.html.
4. The revised dossier was checked for the seven research stages, all 18 claim IDs, the seven visualisation opportunities, the accuracy report and the 22-row source register. The research review was marked complete.
5. Editorial note: the dossier hero's phrase “22 distinct primary papers and official engineering documentation pages” is slightly too narrow because the register also includes a GitHub repository. Preferred wording for a future editorial export: “22 distinct research and technical sources.” The source dossier is preserved as received (apart from the image-payload removal); this wording has not been silently edited.

### Research prompt and revision history

- Prompt sent to Gemini Neon: prompts/neon-research-prompt.md.
- Accuracy-revision prompt sent to Gemini Neon: prompts/neon-dossier-revision-prompt.md.
- Output: research/dossier-revised-clean.html.
- Research verification/access date recorded in the dossier: 22 November 2026.

## 2026-11-22 — Narration drafting and technical review

1. Narration Script v1 was drafted from the research dossier and targeted a 60-second English voiceover.
2. The exact v1 draft is preserved at scripts/narration-v1.md.
3. Argon 4 was given the revised dossier and v1 script for sentence-by-sentence fact checking against C001–C018.
4. Argon 4 returned the verdict: **APPROVED WITH MINOR CORRECTIONS**. This verdict applies to v1 only.
5. The audit identified four required corrections:
   - Remove the implication that context is always assembled on the remote server; add formatting for the model.
   - Correct the feed-forward-block claim traceability: C011/C012 do not directly cover dense FFN blocks. Keep the narration but map it to Research Brief Stage 5 / Vaswani et al. (2017).
   - Add the generation stop condition to the autoregressive loop.
   - Avoid implying that readable text is returned only after the whole generation loop; account for streaming and completed-response delivery.
6. Optional improvements were adopted where useful: explicitly say integer IDs, learned numerical vectors and raw vocabulary logits; clarify the per-position feed-forward transformation.
7. The full review output is preserved unchanged at research/argon-script-review-v1.md.
8. Narration Script v2 was drafted with the required changes and updated claim/evidence mapping. It contains 124 whitespace-delimited words.
9. **Important status:** v2 has not yet been independently reviewed by Argon 4. Do not transfer the v1 verdict to v2.

### Prompt used for the Argon 4 audit

See prompts/argon-script-audit-prompt.md. The prompt instructed Argon 4 to check accuracy, claim support, provider generalisation, sequence and 60-second pacing, and to separate mandatory corrections from optional improvements.

## 2026-11-22 — Storyboard planning

1. A nine-scene storyboard v1 was drafted from narration v2, with planned timings that total 60 seconds.
2. Scene sequence: hook; request/context; tokenization; embeddings; Transformer; logits/selection; generation loop; readable output; brand outro.
3. Scene timing is provisional. Final timing must be measured against the actual recorded or generated voiceover, pauses and visual holds.
4. Visual-reference search phrases are recorded in storyboard/visual-reference-queries.md. These references are inspiration only, not production assets.
5. No narration audio, motion-graphics source code, rendered pilot, final MP4, contact sheet or QA report has been produced yet.

## Current state at this commit

- Research dossier: reviewed and recorded.
- Narration v1: Argon 4 verdict APPROVED WITH MINOR CORRECTIONS.
- Narration v2: corrections applied; re-audit pending.
- Storyboard v1: provisional; dependent on final narration and actual voice timing.
- Animation pilot: not started.
- Full render: not started.
- Publishing: not scheduled.

## Next production gates

1. Send narration v2 with the clean research dossier to Argon 4 for a fresh audit.
2. Lock narration only after the v2 audit and word/pacing review.
3. Refine the storyboard against the locked narration and measured voiceover duration.
4. Create a 5–10-second visual pilot before full production.
5. Review typography, motion, brand consistency, technical diagrams and audio.
6. Only then proceed to full rendering, frame/contact-sheet review, technical QA and final export.