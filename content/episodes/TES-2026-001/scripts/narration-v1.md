# TECHENIGMASTUDIOS — Episode 001
## Narration Script v1: What Actually Happens When You Press Send?

**Target duration:** 60 seconds  
**Narrated word count:** 117 words  
**Format:** English voiceover | 9:16 vertical | 1080 × 1920

### Narration

You press Send. What happens next?

Your app sends a request to an AI service. There, relevant conversation context and instructions are assembled.

A tokenizer splits the text into pieces called tokens and maps each piece to an ID.

Each ID looks up a learned vector; the architecture also represents token order.

These vectors pass through Transformer layers. Attention combines information from the current and earlier positions; feed-forward blocks transform each representation.

The model produces scores called logits. Softmax converts them into probabilities, and a decoding method selects the next token.

That token joins the sequence, and the process repeats—one token at a time.

Finally, token IDs are decoded into readable text and returned to your screen.

**End card (not included in narrated word count):** TECHENIGMASTUDIOS — Decode. Understand. Build.

### Claim mapping

| Narration section | Research Claim IDs |
|---|---|
| App request and conversation context | C001, C004 |
| Tokenization and token IDs | C005 |
| Embeddings and sequence order | C008, C009 |
| Transformer, attention and feed-forward blocks | C011, C012 |
| Logits, probabilities and next-token selection | C014, C015 |
| Autoregressive repetition | C017 |
| Final decoding to readable text | C018 |

### Timing note

117 words is approximately 117 words per minute over 60 seconds. Actual runtime must be checked against the selected voice, pauses and visual holds. The timing is a target, not a measured TTS duration.