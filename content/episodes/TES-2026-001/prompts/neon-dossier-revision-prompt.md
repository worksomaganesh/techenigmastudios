# Episode 001 — Technical Research Dossier: Accuracy Revision

Revise the existing technical research dossier. Do not rewrite the entire document unnecessarily. Preserve valid research, the seven-stage structure, existing Claim IDs, and useful visualisation concepts.

Make the following corrections:

1. Request handling and streaming
- Avoid implying that every AI chat application uses SSE.
- Explain that many APIs support incremental streaming, commonly through SSE, while transport and implementation vary.
- Clarify that the described request path is a generic architecture, not a verified internal diagram of ChatGPT or Gemini.

2. Conversation state
- Distinguish the model's lack of persistent conversational memory from application-managed conversation state.
- Explain that applications may resend relevant history or reference server-managed threads/conversation IDs.
- Do not state that every provider resends the full conversation on every request.

3. Positional information
- Explain that positional information can be represented through different architectural mechanisms, including additive positional encodings, RoPE and attention biases such as ALiBi.
- Do not imply that every model uses a separate positional embedding vector.
- Replace the Stage 4 rotating phase-dial visual with neutral sequence-position markers unless RoPE is explicitly being demonstrated.

4. Attention visualisation
- Revise language suggesting attention arcs identify semantically relevant words.
- Describe arcs as a conceptual representation of attention weights and causal masking.
- Clarify that this visual is explanatory, not an interpretation of model reasoning.

5. KV cache
- Make the animation show per-layer cached Key and Value tensors.
- Do not represent the cache as simply storing old token tiles.
- Preserve the distinction between computing new K/V states and attending to previously cached K/V states.

6. Decoding
- Avoid claiming that all chat assistants typically use controlled sampling.
- Explain that decoding may use greedy selection or sampling depending on the model and generation configuration.
- For the 60-second episode, prioritise: logits → probability distribution → next-token selection. Treat temperature, top-k and top-p as optional deeper details.

7. Claim–Evidence Matrix
- Reassess confidence ratings individually. Do not automatically mark every claim High.
- Ensure every important claim has evidence that directly supports it.
- Clearly mark provider-dependent and architecture-dependent claims.

8. Source Register
- Give every distinct source its own row.
- Replace abbreviated or ellipsis-based URLs with complete, exact URLs.
- The current register combines multiple Hugging Face documentation pages into one row. Split them into separate entries.
- Reconcile the total source count with the number of distinct URLs.
- Include publication dates or document update dates only when verifiable. Otherwise state that the source is live documentation with no displayed publication date.
- Add a research verification/access date of 22 November 2026.

## Output requirements

Return the complete revised HTML dossier.

Keep all seven stages, the original Claim IDs wherever their meaning remains unchanged, all useful research, the seven visualisation opportunities, the accuracy report and the source register.

Do not generate the narration script or storyboard yet.

The revised dossier must be technically accurate, properly sourced, internally consistent, and ready to serve as the factual foundation for Episode 001.