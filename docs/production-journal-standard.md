# TECHENIGMASTUDIOS — Episode Production Journal Standard

## Purpose

This repository is the brand's source of truth for both the finished content and the process used to create it. Preserve the production journey, not only the final export.

For every episode, commit the important working artifacts: research, source maps, prompts, model outputs, review feedback, corrections, scripts, storyboard revisions, production decisions, assets manifests, render logs and QA reports.

## Required principles

1. **Preserve versions.** Never overwrite an earlier script, prompt, storyboard or review output when a material revision is made. Use v1, v2, v3 and keep the chronology in the production log.
2. **Keep raw outputs distinct.** Save a model's returned review/output unchanged where practical. Put corrected or editorially cleaned documents in separate files and record what changed.
3. **Record provenance.** For each prompt/output, record the date, tool/model label as actually shown, purpose, input artifact versions and resulting file. Do not invent an exact model identifier if the UI did not expose one.
4. **Maintain evidence traceability.** Technical scripts must map factual narration claims to Claim IDs or explicitly cited research-brief sources. Record unresolved mapping gaps.
5. **Separate status states.** Use clear labels such as Draft, Reviewed, Approved, Superseded and Pending re-review. An approval for one version never automatically applies to its successor.
6. **Record decisions and reasons.** Include duration, aspect ratio, dimensions, audience, language, visual identity, production-stack choices and scope changes.
7. **Record production evidence.** Preserve asset prompts, asset references/rights, code commits, render settings, render logs, contact sheets, QA reports and the final publishing package when those stages happen.
8. **Protect secrets and rights.** Never commit API keys, cookies, session tokens, private user data or confidential account material. Record asset licences, attributions and permissions; do not place unlicensed third-party media in production.
9. **Keep large media separate from prose.** Store actual approved assets under the episode's assets directory with a manifest. Do not embed large base64 media inside HTML research documents; this can cause truncation when the document is passed between tools.
10. **Do not fabricate evidence.** If an audio render, animation, test or export has not been produced and checked, mark it Not started or Pending.

## Suggested episode structure

- content/episodes/TES-YYYY-NNN/brief.md
- content/episodes/TES-YYYY-NNN/production-log.md
- content/episodes/TES-YYYY-NNN/research/
  - dossier-revised-clean.html or research-brief.md
  - claim-evidence-matrix.md
  - source-register.md
  - review-output-v1.md
- content/episodes/TES-YYYY-NNN/prompts/
  - research-prompt.md
  - research-revision-prompt.md
  - script-review-prompt.md
  - visual-generation-prompts.md
- content/episodes/TES-YYYY-NNN/scripts/
  - narration-v1.md
  - narration-v2.md
  - final-locked.md
- content/episodes/TES-YYYY-NNN/storyboard/
  - storyboard-v1.md
  - storyboard-v2.md
  - shot-list.csv
- content/episodes/TES-YYYY-NNN/assets/
  - asset-manifest.md
  - generated/original assets
- content/episodes/TES-YYYY-NNN/production/
  - production-plan.json
  - voiceover-notes.md
  - render-log.md
  - contact-sheets/
  - qa-report.md
- content/episodes/TES-YYYY-NNN/publishing/
  - title-description.md
  - captions.srt
  - platform-copy.md

Create only the files relevant to the current stage; do not add empty placeholder assets.

## Suggested production-log entry format

For each material event, record:

- Date and time (with timezone if available).
- Stage and artifact version.
- Tool/model label, as reported by the interface.
- Prompt path or prompt identifier.
- Input artifacts.
- Output artifact path.
- Review status and findings.
- Decision, owner and next gate.

## Version and approval vocabulary

- **Draft:** created, not yet reviewed.
- **Reviewed:** a reviewer has examined it; corrections may remain.
- **Approved:** the exact version was approved against its stated criteria.
- **Approved with minor corrections:** review verdict permits use after identified corrections; record whether they were applied.
- **Pending re-review:** changed after review and needs a fresh verdict.
- **Superseded:** replaced by a later version but retained for provenance.

The status must always be attached to an exact version. Do not call v2 approved because v1 was approved with corrections.

## Minimum episode close-out

An episode is not marked production-complete until the repository contains the locked script, final storyboard/shot list, final asset manifest, source/rights record, rendered master, render metadata, contact sheet, completed QA report and publishing package. Human approval is required before scheduling or publishing.