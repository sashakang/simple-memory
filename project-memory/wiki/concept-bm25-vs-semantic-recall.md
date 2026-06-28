# concept: BM25 (keyword) vs semantic recall

The retrieval axis of [[concept-six-levels-of-memory]], and **doubt #1** driving the
[[candidate-observational-memory]] decision: *is BM25 keyword recall good enough, or do we need to climb to
semantic/hybrid — and is that climb worth what it costs?*

## The two ends

- **BM25 / keyword** (OM's choice, L2-ish): lexical match, no embeddings, no vector index, no model. Cheap,
  local, deterministic, zero infra. **Failure mode — vocabulary drift:** misses when the query and the stored
  note phrase the same concept differently. Partly mitigated by reflection/canonicalization that normalizes
  terms at write time.
- **Semantic / vector** (L3+, e.g. [[candidate-memsearch]]): embeds chunks, matches by meaning, robust to
  paraphrase. **Cost:** an embedding model + a vector index — the exact spend against constraint (b)
  "simplistic." L4 ([[candidate-mempalace]]) and L6 ([[candidate-openbrain]]) push further into multi-DB / hosted.
- **Hybrid / graph retrieval:** combines lexical, semantic, reranking, evidence grounding, and sometimes graph
  propagation. [[source-best-claude-memory-system]] argues for hybrid search + cited answers; [[source-memorygraphrag]]
  shows the research end of that climb with ontology/fact/passage memory and PageRank. This is capability-rich
  but far beyond the "simplest viable" bar unless a concrete failure forces it.

## Where this nets out (current view, from research + this source)

- The L2→L3 jump exists precisely because "keyword search starts falling apart as you scale" — the source's
  own words. So the doubt is **real**, not imagined.
- But prior deep-research found the *measured* gain modest: hybrid buys only ~**+5pp Recall@5** over keyword
  baselines in the relevant regime, and lexical/grep-style matching is competitive for code-shaped memory.
  That gain doesn't obviously clear the "complexity must earn its place" bar.
- **memsearch is the escape valve:** if BM25 ever bites in practice, it's the *least-invasive* way to add
  semantic recall (still plain markdown, 2-line install) — at the cost of constraint (a), since it's
  Claude-Code-only.
- **Vectors have their own failure modes:** [[source-claude-second-brain-levels]] warns that chunk retrieval
  can miss full-context tasks, such as summarizing an entire meeting or computing over a whole table. Semantic
  recall is not a blanket upgrade over reading the right markdown file.

**Implication for OM:** keep BM25 now; treat [[candidate-memsearch]] as the named, pre-vetted upgrade if a
concrete recall miss is ever observed. Decision deferred per standing instruction.

[[concept-six-levels-of-memory]] · [[candidate-observational-memory]] · [[candidate-memsearch]] ·
[[source-memorygraphrag]]
