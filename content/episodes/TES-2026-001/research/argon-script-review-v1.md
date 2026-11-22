## Sentence-by-Sentence Verification Overview

| # | Original Sentence | Script Claim Mapping | Dossier Verification Status |
| --- | --- | --- | --- |
| 1–2 | *"You press Send. What happens next?"*

 | None (hook)

 | **Pass** — Framing hook; no technical claim made.

 |
| 3 | *"Your app sends a request to an AI service."*

 | C001, C004

 | **Pass** — Matches generic client-to-backend flow without generalizing transport protocols.

 |
| 4 | *"There, relevant conversation context and instructions are assembled."*

 | C001, C004

 | **Mandatory correction** — *"There"* overgeneralizes server-side state assembly; omits C004 formatting.

 |
| 5 | *"A tokenizer splits the text into pieces called tokens and maps each piece to an ID."*

 | C005

 | **Pass (optional tweak)** — Accurately avoids the "one token = one word" myth.

 |
| 6 | *"Each ID looks up a learned vector; the architecture also represents token order."*

 | C008, C009

 | **Pass (optional tweak)** — Correctly avoids generalizing additive-only positional embeddings.

 |
| 7–8 | *"These vectors pass through Transformer layers. Attention combines information from the current and earlier positions; feed-forward blocks transform each representation."*

 | C011, C012

 | **Mandatory mapping fix** — Scientifically accurate per Stage 5, but feed-forward blocks are not covered by C011 or C012 in the Claim–Evidence Matrix.

 |
| 9–10 | *"The model produces scores called logits. Softmax converts them into probabilities, and a decoding method selects the next token."*

 | C014, C015

 | **Pass (optional tweak)** — Matches the dossier's prioritized 60-second sequence and avoids generalizing sampling defaults.

 |
| 11 | *"That token joins the sequence, and the process repeats—one token at a time."*

 | C017

 | **Mandatory correction** — Omits any stop condition, leaving the autoregressive loop unbounded.

 |
| 12 | *"Finally, token IDs are decoded into readable text and returned to your screen."*

 | C018

 | **Mandatory correction** — *"Finally"* misrepresents sequence by implying post-loop batch delivery only; *"decoded"* collides with *"decoding method"*.

 |

---

## Mandatory Factual & Technical Corrections

### Issue 1: Provider-specific overgeneralization of where context is assembled

1. **Original sentence:** *"There, relevant conversation context and instructions are assembled."*


2. **Technical issue:** The word *"There"* ties assembly strictly to the remote AI service. Under the dossier, base LLM APIs are stateless—meaning the client application often assembles and resends relevant conversation history and instructions in the request payload—while server-managed thread or conversation APIs reconstruct context on the backend. In addition, the sentence is mapped to C004, which specifically concerns formatting role-based messages into a single flat sequence via a chat template, yet the line mentions only assembly and omits formatting.


3. **Relevant Claim ID:** `C001`, `C004`.


4. **Mandatory correction:** Replace *"There, relevant conversation context and instructions are assembled."* with:


> *"Relevant conversation context and instructions are assembled and formatted for the model."* (+3 words over original sentence; removes the server-only location claim and aligns with C004 formatting.)
> 
> 



### Issue 2: Unmapped feed-forward block claim in Claim Mapping table

1. **Original sentence:** *"Attention combines information from the current and earlier positions; feed-forward blocks transform each representation."*


2. **Technical issue:** The spoken sentence is technically accurate and supported by Stage 5 of the Research Brief (citing Vaswani et al., 2017). However, the script maps this section solely to `C011, C012`. In the Claim–Evidence Matrix, `C011` covers only Scaled Dot-Product Attention and Multi-Head Attention, and `C012` covers only causal masking—neither claim mentions position-wise feed-forward blocks (and `C013` covers only Sparse MoE FFN routing, not dense FFN blocks in general). Because every claim in the script must be defensible via the mapped Claim IDs, this creates a traceability gap in the claim mapping.


3. **Relevant Claim ID:** `C011`, `C012` (gap relative to Research Brief Stage 5 / Vaswani et al., 2017).


4. **Mandatory correction:** No change to the narration text is required; update the script's **Claim mapping** table note for *"Transformer, attention and feed-forward blocks"* to state `C011, C012 (plus Research Brief Stage 5 / Vaswani et al., 2017 for position-wise FFN blocks)`—or add an explicit FFN note to the matrix before lock.



### Issue 3: Missing stop condition for the autoregressive loop

1. **Original sentence:** *"That token joins the sequence, and the process repeats—one token at a time."*


2. **Technical issue:** The narration omits how the autoregressive loop terminates. Both the dossier's Core Technical Thesis (*"until a stop condition is met"*) and `C018` (*"Generation halts upon emitting an End-of-Sequence (EOS) token, matching a stop sequence, or hitting max token limits"*) treat stopping criteria as an essential part of Stage 7. Without a stop condition, beginners are left with an open-ended loop that abruptly jumps to *"Finally"*. (Note: Omitting per-layer KV caching from `C017` is an acceptable 60-second simplification explicitly permitted by the dossier's Accuracy and Risk Report.)


3. **Relevant Claim ID:** `C017`, `C018`.


4. **Mandatory correction:** Replace *"That token joins the sequence, and the process repeats—one token at a time."* with:


> *"That token joins the sequence, repeating—one token at a time—until a stop condition is met."* (+2 spoken words; adds termination mechanics without breaking pacing, and updates mapping for this beat to `C017, C018`.)
> 
> 



### Issue 4: Misleading post-loop batch delivery and overloaded "decoded" terminology

1. **Original sentence:** *"Finally, token IDs are decoded into readable text and returned to your screen."*


2. **Technical issue:** Placing *"Finally"* immediately after the repeating loop misleads beginners into thinking detokenization and screen delivery happen only after the entire response finishes generating. Per Stage 1 (`C002`), Stage 7, and the `C018` caveat, while non-streaming endpoints return a completed payload, many LLM APIs and chat interfaces detokenize and stream text incrementally as token IDs are produced. Additionally, using *"decoded"* here (`C018` detokenization) just 15 words after *"decoding method"* (`C015` next-token selection) overloads one technical word for two unrelated operations, which can confuse beginners.


3. **Relevant Claim ID:** `C002`, `C015`, `C018`.


4. **Mandatory correction:** Replace *"Finally, token IDs are decoded into readable text and returned to your screen."* with:


> *"Generated token IDs are converted back into readable text and streamed—or returned—to your screen."* (+1 whitespace word / +2 spoken words; accurately accommodates both streaming and non-streaming delivery and eliminates the "decoding" vs. "decoded" collision. Add `C002` alongside `C018` in the Claim Mapping table.)
> 
> 



---

## Optional Editorial Suggestions (Non-Blocking)

### Suggestion 1: Make the text-to-numbers bridge explicit in tokenization

1. **Original sentence:** *"A tokenizer splits the text into pieces called tokens and maps each piece to an ID."*


2. **Technical issue:** Accurate as written, because *"pieces"* already avoids the "one token equals one word" myth. However, Stage 3 opens with *"Neural networks operate on numbers, not raw text,"* and `C005` specifies *"integer IDs"*; beginners may not immediately realize *"an ID"* is a number.


3. **Relevant Claim ID:** `C005`.


4. **Optional suggestion:** Change *"an ID"* to *"a number ID"* or *"an integer ID"* (+1 word).



### Suggestion 2: Clarify vector lookup phrasing and add secondary claim reference

1. **Original sentence:** *"Each ID looks up a learned vector; the architecture also represents token order."*


2. **Technical issue:** Technically defensible and commendably careful not to imply additive-only positional embeddings. Strictly speaking, an integer ID is an index used *to look up* a vector rather than an agent doing the lookup, and *"learned vector"* omits that embeddings are numerical.


3. **Relevant Claim ID:** `C008`, `C009` (and `C010` as supporting rationale for generic order wording).


4. **Optional suggestion:** *"Each ID maps to a learned number vector; the architecture also represents token order."* (+2 words) and optionally cite `C010` alongside `C008, C009` in the mapping table.



### Suggestion 3: Specify what logits score and that they are raw scores

1. **Original sentence:** *"The model produces scores called logits."*


2. **Technical issue:** Factually correct, and the next sentence distinguishes logits from probabilities via softmax. Still, beginners may not realize logits score *every possible next token in the vocabulary* (rather than scoring the input tokens) and are *raw, unnormalized* values.


3. **Relevant Claim ID:** `C014`.


4. **Optional suggestion:** *"The model produces raw scores—called logits—for every token in its vocabulary."* (+5 words, or tighter: *"The model produces raw vocabulary scores called logits."* +2 words).

### Suggestion 4: Clarify position-wise independence in feed-forward blocks

1. **Original sentence:** *"Attention combines information from the current and earlier positions; feed-forward blocks transform each representation."*


2. **Technical issue:** Accurate, though *"each representation"* could be slightly clearer for beginners by explicitly echoing *"each position's"* to contrast with attention combining across positions.


3. **Relevant Claim ID:** `C011`, `C012` (Stage 5).


4. **Optional suggestion:** *"Attention combines information from the current and earlier positions; feed-forward blocks transform each position's representation."* (+1 word).

---

## Conceptual Sequence & 60-Second Pacing Check

* **Conceptual sequence:** Stages 1 through 6 follow the exact pipeline order established in the dossier: user request $\rightarrow$ context and instruction assembly $\rightarrow$ subword tokenization and IDs $\rightarrow$ embeddings and sequence order $\rightarrow$ Transformer layers (causal attention and feed-forward blocks) $\rightarrow$ logits, softmax probabilities, and next-token selection. The only sequence defect is at Stage 7, where placing *"Finally"* after the loop without a stop condition implies strictly post-loop detokenization and return; applying Mandatory Corrections 3 and 4 resolves this completely.


* **Word count & 60-second fit:** The current narration contains **117 whitespace-delimited words** (118–119 spoken words when splitting *"repeats—one"* and *"feed-forward"*). Applying all mandatory narration fixes brings the script to approximately **122–123 whitespace words** (~124–126 spoken words). For a beginner technical explainer, 117–126 spoken words delivered at a clear, measured pace of ~135–145 WPM takes roughly **51–55 seconds of speech**, leaving **5–9 seconds** for natural pauses after the opening hook, between pipeline stages, and ahead of the end card. As noted in the script's timing note, final runtime must still be verified against actual voiceover/TTS delivery and visual holds.



---

APPROVED WITH MINOR CORRECTIONS