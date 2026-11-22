# TECHENIGMASTUDIOS — Episode 001
## Narration Script v2: What Actually Happens When You Press Send?

**Status:** Revised draft; fresh technical re-audit pending.  
**Target duration:** 60 seconds  
**Whitespace-delimited word count:** 124 words  
**Format:** English voiceover | 9:16 vertical | 1080 × 1920

### Narration

You press Send. What happens next?

Your app sends a request to an AI service. Relevant conversation context and instructions are assembled and formatted for the model.

A tokenizer splits text into tokens and maps them to integer IDs.

Each ID maps to a learned numerical vector; the architecture also represents token order.

These vectors pass through Transformer layers. Attention combines information from current and earlier positions; feed-forward blocks transform each position's representation.

The model produces raw vocabulary scores called logits. Softmax converts them into probabilities, and a decoding method selects the next token.

That token joins the sequence. Generation repeats one token at a time until a stop condition is met.

Generated token IDs become readable text and are streamed—or returned—to your screen.

**End card (not included in narrated word count):** TECHENIGMASTUDIOS — Decode. Understand. Build.

### Claim and evidence mapping

| Narration section | Research mapping |
|---|---|
| App request and conversation context | C001, C004 |
| Tokenization and integer IDs | C005 |
| Embeddings and sequence order | C008, C009, C010 |
| Transformer attention and causal positions | C011, C012 |
| Position-wise feed-forward blocks | Research Brief Stage 5; Vaswani et al. (2017), Attention Is All You Need |
| Logits, probabilities and next-token selection | C014, C015 |
| Autoregressive generation and stop conditions | C017, C018 |
| Streaming or completed text output | C002, C018 |

### Changes from v1

1. Removed the server-only implication from the context-assembly sentence and added formatting for the model.
2. Clarified that token IDs are integer IDs and embeddings are numerical vectors.
3. Updated the feed-forward description and added a supporting reference outside the Claim–Evidence Matrix because C011 and C012 do not directly cover dense FFN blocks.
4. Added the stop condition to the autoregressive loop.
5. Rephrased final output as conversion to readable text that may be streamed or returned, avoiding the ambiguous repeated use of “decoding”.

### Review status

Argon 4 reviewed v1 and returned “APPROVED WITH MINOR CORRECTIONS”. That verdict applies to v1 only. This v2 draft has not yet received a separate technical approval.