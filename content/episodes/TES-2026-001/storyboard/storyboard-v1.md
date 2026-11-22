# Episode 001 — Storyboard v1
## What Actually Happens When You Press Send?

**Status:** Provisional storyboard draft; not yet reviewed against a locked voiceover.
**Target runtime:** 60 seconds
**Canvas:** 1080 × 1920, 9:16 vertical
**Language:** English
**Brand:** TECHENIGMASTUDIOS
**Palette:** Pure black (#000000), signal yellow (#FFD400), white
**Format:** Faceless, narration-led, premium technical motion graphics

## Scene timing overview

| Timecode | Duration | Scene | Purpose |
|---|---:|---|---|
| 00:00–00:04 | 4s | Hook | Create curiosity around the Send action |
| 00:04–00:14 | 10s | Request and context | Show application request and context preparation |
| 00:14–00:20 | 6s | Tokenization | Show text splitting into tokens and integer IDs |
| 00:20–00:26 | 6s | Embeddings | Show numerical vectors and sequence-position markers |
| 00:26–00:34 | 8s | Transformer | Show attention and feed-forward processing |
| 00:34–00:44 | 10s | Logits and selection | Show logits, probability distribution and token selection |
| 00:44–00:52 | 8s | Generation loop | Show token append, repetition and stop condition |
| 00:52–00:57 | 5s | Readable output | Show token IDs becoming readable text |
| 00:57–01:00 | 3s | Brand outro | Resolve the visual journey and brand signature |

## Detailed scene direction

### Scene 01 — Hook (00:00–00:04)
**Narration:** “You press Send. What happens next?”
**Visual:** A dark phone interface. The Send button is pressed; a signal-yellow pulse travels from the interface into a digital environment.
**Motion:** Tight camera push-in, tap ripple, fast transition into the request path.
**On-screen text:** “You press SEND.”
**Accuracy note:** Treat the phone as a generic interface, not a screenshot of a specific provider.

### Scene 02 — Request and context (00:04–00:14)
**Narration:** “Your app sends a request to an AI service. Relevant conversation context and instructions are assembled and formatted for the model.”
**Visual:** A request packet travels from a generic app/client towards a backend. Previous conversation turns and instructions converge with the current message; role labels appear on a formatted sequence.
**Motion:** Separate elements converge into one structured model input.
**On-screen labels:** “Current prompt”, “Relevant context”, “Instructions”, “Formatted input”.
**Accuracy note:** The client may assemble/resend history or the service may reference server-managed conversation state. Do not imply one universal backend architecture or transport.

### Scene 03 — Tokenization (00:14–00:20)
**Narration:** “A tokenizer splits text into tokens and maps them to integer IDs.”
**Visual:** A sentence separates into unequal token blocks. Each block flips to reveal an illustrative integer ID.
**Motion:** Scanner/slicer reveals token boundaries; blocks settle into a sequence.
**On-screen labels:** “Tokens” and “Integer IDs”.
**Accuracy note:** Do not imply one token equals one word. Any displayed token IDs are illustrative, not universal model IDs.

### Scene 04 — Embeddings (00:20–00:26)
**Narration:** “Each ID maps to a learned numerical vector; the architecture also represents token order.”
**Visual:** Integer ID tiles transform into abstract vector columns. Neutral position markers appear under the sequence.
**Motion:** IDs morph into numerical bars; markers attach to sequence positions.
**On-screen labels:** “Embedding vectors” and “Position”.
**Accuracy note:** Do not show a fixed embedding dimension or imply all models use one positional encoding mechanism.

### Scene 05 — Transformer (00:26–00:34)
**Narration:** “These vectors pass through Transformer layers. Attention combines information from current and earlier positions; feed-forward blocks transform each position's representation.”
**Visual:** A stack of conceptual Transformer layers. Attention arcs connect the active position to itself and earlier positions. A separate feed-forward block transforms each position's representation.
**Motion:** Camera moves through layers; attention weights appear as conceptual arcs; each representation passes through an FFN block.
**On-screen labels:** “Self-attention”, “Causal mask”, “Feed-forward”.
**Accuracy note:** Attention arcs are an explanatory representation of weights and causal access, not a visualisation of the model's thoughts. Avoid claims that attention weights prove semantic relevance.

### Scene 06 — Logits and selection (00:34–00:44)
**Narration:** “The model produces raw vocabulary scores called logits. Softmax converts them into probabilities, and a decoding method selects the next token.”
**Visual:** A vocabulary score distribution appears as raw bars. A Softmax transition normalises them into a probability distribution; a selector highlights one token.
**Motion:** Raw bars transform into a normalised probability view; one candidate is selected.
**On-screen labels:** “Logits”, “Softmax”, “Probabilities”, “Next token”.
**Accuracy note:** Do not label logits as probabilities. Do not imply every model uses the same sampling settings or decoding method.

### Scene 07 — Generation loop (00:44–00:52)
**Narration:** “That token joins the sequence. Generation repeats one token at a time until a stop condition is met.”
**Visual:** The chosen token joins the sequence and the sequence returns through the generation path. A stop gate appears at the end.
**Motion:** Show two rapid generation cycles, then an EOS/stop signal closes the loop.
**On-screen labels:** “Append token”, “Repeat”, “Stop condition”.
**Accuracy note:** Stop conditions may include EOS, a configured stop sequence or a generation limit. Do not imply a single universal stop mechanism.

### Scene 08 — Readable output (00:52–00:57)
**Narration:** “Generated token IDs become readable text and are streamed—or returned—to your screen.”
**Visual:** A token sequence transforms into readable text. Show progressive delivery as the primary visual, with a compact label indicating that complete-response return is also possible.
**Motion:** Text appears progressively and resolves into the final sentence.
**On-screen labels:** “Generated text”, “Streaming / completed response”.
**Accuracy note:** Support both streaming and non-streaming response delivery.

### Scene 09 — Brand outro (00:57–01:00)
**Narration:** None; music resolves.
**Visual:** TECHENIGMASTUDIOS wordmark and tagline.
**Motion:** Subtle yellow line draw, logo settles, clean cut/fade.
**On-screen text:** “TECHENIGMASTUDIOS” / “Decode. Understand. Build.”

## Global visual and motion rules

- Use one continuous visual world: phone prompt → request/context stream → tokens → vectors → Transformer layers → probability distribution → output.
- Primary background: #000000.
- Signal yellow: #FFD400 for focal elements, data flow and key terms.
- White for supporting labels; avoid low-contrast grey for essential information.
- Keep all text inside 9:16 platform safe areas.
- Use smooth, purposeful camera movement; avoid decorative trails and excessive glow.
- Use precise timing and consistent easing; no random particles unless they communicate data flow.
- Prefer original diagrams and deterministic code animation for technical elements.
- Google Flow footage is optional, not a dependency.
- Do not present generic illustrative visuals as screenshots or verified internals of ChatGPT, Gemini or another closed assistant.

## Timing and approval caveat

The scene durations are a planning allocation that totals 60 seconds. They are not measured against an actual voice recording. Retiming is required after narration/TTS selection. This storyboard is provisional until narration v2 receives a fresh technical review and the voiceover timing is measured.