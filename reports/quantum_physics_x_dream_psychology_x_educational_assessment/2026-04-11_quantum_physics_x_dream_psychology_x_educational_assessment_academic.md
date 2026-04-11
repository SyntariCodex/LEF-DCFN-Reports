# DCFN Technical Report: quantum physics × dream psychology × educational assessment

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `07d266d13e5b24a6`
**Corpus fingerprint:** `no-corpus`
**Sources:** 387

---

*This document is the proof-of-receipt for a single DCFN run. It records what executed, what was produced, and which components governed the work. Internal calibration (weights, thresholds, formulas) is intentionally omitted — that is engine IP. For findings and gap-bridging proposals, see the accompanying Article.*

## Capability Envelope — Read First

DCFN is a structural literature mapper. It is strong at the jobs
below and explicit about the jobs it does not currently do. These
three boundaries are the most load-bearing for interpreting anything
in this report — treat them as preconditions, not footnotes.

**1. CONTRADICTS edges are inferred from structural patterns, not
content reading.** DCFN does not read two abstracts and decide one
contradicts the other. It infers contradiction from citation topology
and embedding geometry. When this report names a contradiction, it
is naming a structural tension in how the field is organized — not
a propositional disagreement between authors. Use the finding as a
signal to investigate, not as a verdict.

**2. Semantic encoding uses sentence-level embeddings (Sentence-BERT
all-MiniLM-L6-v2) or a TF-IDF fallback.** Both capture distributional
similarity across titles and abstracts. Neither captures deep domain
nuance, multi-hop reasoning, or the qualitative dimensions of human
practice. A paper whose contribution lives in its methodology section
rather than its abstract will be underweighted. A field whose
vocabulary has drifted will show phantom gaps. The embedding layer
is a coarse instrument with known blind spots, not a reading layer.

**3. The staleness signal measures citation recency, not practice
maturation.** When DCFN flags a paper as an "untested foundation,"
it means the paper is not actively reappearing in current citation
loops. It does NOT mean the paper's content is obsolete or unvalidated.
Clinical intervention literature, community-practice disciplines, and
applied fields mature through decades of real-world use that citation
counts do not register. The report filters known practice-validated
fields from staleness rendering, but the filter is not exhaustive —
if a paper you know to be foundational-and-actively-practiced is
flagged as stale, the engine is reading the citation graph correctly
and the interpretation layer is wrong.

The rest of this report operates inside this envelope. Findings
outside it are not claims the engine is capable of making.

---



## Band 1 — What Ran

*Proof of life. Every entry below is mechanically derived from the run that produced this document.*

### 1.1 Run Identity

| Field | Value |
|-------|-------|
| Engine version | `0.3.0-prototype` |
| Run timestamp | `2026-04-11T00:31:16.901139` |
| Run fingerprint | `07d266d13e5b24a6` |
| Corpus fingerprint | `no-corpus` |
| Domain | quantum physics × dream psychology × educational assessment |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 387 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 387 sources encoded |
| Concept graph | 420 nodes / 3966 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 5) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 377 entropy nodes inspected (251 critical, 33 high) |
| CTE branch cataloging | 7 clusters identified (9 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (6 entropy nodes resolved) |
| Apriori pattern mining | 20 1-itemsets, 31 2-itemsets, 6 3-itemsets, 3 rules |
| SVW synchronicity | 1994 candidate pairs scanned, 2 convergence events, 216 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 56.85 s |
| concept_graph | 332 ms |
| cte_traversal | 168 ms |
| apriori | 23 ms |
| svw | 196 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 222 ms |
| bridge_detection | 3 ms |
| **Total measured** | **57.79 s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 412 | 25 | 387 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 420 |
| Total edges | 3966 |
| Connected components | 15 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 387 |
| ENTITY | 18 |
| CONCEPT | 15 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 2937 |
| CONTAINS | 520 |
| EXTENDS | 304 |
| BRIDGES | 141 |
| DEFENDED_BY | 37 |
| ENABLES | 20 |
| DEPENDS_ON | 7 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | dream psychology, educational assessment, quantum physics, quantum physics × dream psychology × educational assessment |
| Cross-domain edges | 613 |
| Bridge nodes | 270 |

### 2.3 Entropy Nodes

**Total:** 377 (critical: 251, high: 33, low: 93)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Searching for Coherent States: From Origins to Quantum Gravity | — |
| 2 | Quantum simulation and computing with Rydberg-interacting qubits | — |
| 3 | Consciousness as an Inhibited Manifestation and Quantum Physics. | — |
| 4 | Do animals dream? | — |
| 5 | How bizarre? A pluralist approach to dream content. | — |
| 6 | EEG microstates of dreams. | — |
| 7 | Anticipations of dream psychology in the Talmud | — |
| 8 | Best practices in summative assessment. | — |
| 9 | A history of assessment in medical education. | — |
| 10 | Quantum Physics Education Research over the Last Two Decades: A Bibliometric Ana | — |
| 11 | The Dream of God: How Do Religion and Science See Lucid Dreaming and Other Consc | — |
| 12 | Validation of educational assessments: a primer for simulation and beyond | — |
| 13 | Fairness in Educational Assessment and Measurement | — |
| 14 | Design and Discovery in Educational Assessment: Evidence-Centered Design, Psycho | — |
| 15 | When Assessment Data Are Words: Validity Evidence for Qualitative Educational As | — |
| 16 | Bayesian Networks in Educational Assessment | — |
| 17 | Review of Alyssa Ney’s The World in the Wave Function: A Metaphysics for Quantum | — |
| 18 | Towards a better understanding of conceptual difficulties in introductory quantu | — |
| 19 | Quantum Computing in the NISQ era and beyond | — |
| 20 | Quantum physics in space | — |

### 2.4 Branch Clusters

**Total clusters:** 7 (emerging: 0, established: 7)
**Structural mirrors:** 9

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| Quantum Computation and Quantum Information | 135 | Established |
| Quantum physics in space | 9 | Established |
| Investigating teachers’ and students’ experiences of quantum physics lessons: op | 3 | Established |
| Memories, Dreams, Reflections | 121 | Established |
| Knowing What Students Know: The Science and Design of Educational Assessment | 130 | Established |
| Recent Advances on Graphene Quantum Dots: From Chemistry and Physics to Applicat | 2 | Established |
| Exponential Operators and Parameter Differentiation in Quantum Physics | 6 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 2 |
| Convergence anchors | 216 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Quantum physics meets biology | 2009 | 53 |
| 2 | Quantum Computing for High-Energy Physics: State of the Art  | 2023 | 33 |
| 3 | The Physics of Quantum Information | 2022 | 34 |
| 4 | Quantum Chemistry in the Age of Quantum Computing. | 2019 | 32 |
| 5 | Monitoring Quantum Simulators via Quantum Non-Demolition Cou | 2020 | 40 |
| 6 | Quantum Computation and Quantum Information | 2012 | 32 |
| 7 | What is quantum biology? | 2026 | 34 |
| 8 | Quantum reference frame transformations as symmetries and th | 2020 | 31 |
| 9 | A general quantum algorithm for open quantum dynamics demons | 2021 | 32 |
| 10 | Searching for Coherent States: From Origins to Quantum Gravi | 2020 | 34 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 6 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Validation of educational assessments: a primer for simulation and bey | 2016 | Yes |
| 2 | When Assessment Data Are Words: Validity Evidence for Qualitative Educ | 2016 | Yes |
| 3 | A history of assessment in medical education. | 2020 | Yes |
| 4 | Fairness in Educational Assessment and Measurement | 2016 | Yes |
| 5 | Best practices in summative assessment. | 2017 | Yes |
| 6 | Design and Discovery in Educational Assessment: Evidence-Centered Desi | 2012 | Yes |
| 7 | Leveraging Digital Twin for Sustainability Assessment of an Educationa | 2021 | — |
| 8 | The Artificial Intelligence Assessment Scale (AIAS): A Framework for E | 2023 | — |
| 9 | Exploring the potential of artificial intelligence tools in educationa | 2023 | — |
| 10 | The Rise of Artificial Intelligence in Educational Measurement: Opport | 2024 | — |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Searching for Coherent States: From Origins to Quantum Gravity' will unlock currently blocked progress toward: Physics
- **Grounded in:** entropy gap node: Searching for Coherent States: From Origins to Quantum Gr...
- **Novel because:** not yet connected to 'Physics' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H02** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Quantum simulation and computing with Rydberg-interacting qubits' will unlock currently blocked progress toward: Physics
- **Grounded in:** entropy gap node: Quantum simulation and computing with Rydberg-interacting...
- **Novel because:** not yet connected to 'Physics' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H03** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Consciousness as an Inhibited Manifestation and Quantum Physics.' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Consciousness as an Inhibited Manifestation and Quantum P...
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H04** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Do animals dream?' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Do animals dream?
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'How bizarre? A pluralist approach to dream content.' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: How bizarre? A pluralist approach to dream content.
- **Novel because:** absent from 'Memories, Dreams, Reflections' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 3 |
| 2 | Untitled | 3 |
| 3 | Untitled | 3 |
| 4 | Untitled | 3 |
| 5 | Untitled | 3 |
| 6 | Untitled | 3 |
| 7 | Untitled | 3 |
| 8 | Untitled | 2 |
| 9 | Untitled | 3 |
| 10 | Untitled | 3 |

## Band 3 — How It Knows

*Mechanism claims at the component level. Each subsystem below describes what work it performs and which patent governs it. Internal calibration — weights, thresholds, formulas, learning rates — is intentionally omitted.*

### 3.1 Qualitative Bridge (QEB) — Source Encoding

Source text is encoded into dense semantic vectors using **Sentence-BERT (all-MiniLM-L6-v2)**. Each source receives a confidence signal derived from multiple structural properties of its vector representation, and an epistemic grounding score derived from its evidentiary footprint in the corpus. The three-signal adaptive confidence layer is governed by **QECO Patent #74668095** (*Hybrid AI-Human Optimization System with Qualitative Input Perturbation*).

### 3.2 Concept Graph

Sources, fields of study, venues, and authors are placed into a typed concept graph. Edges encode citation lineage, semantic similarity, structural mirroring, and cross-domain bridging. Edge confidence carries a temporal-decay component calibrated to research-literature time scales — older edges decay, but never fall to zero. The graph governs everything downstream and is the substrate for the CTE patent claims.

### 3.3 CTE — Cognitive Traversal Engine (Five Operations)

**CTE Patent #74802827** (*Computer-Implemented Method and System for Cognitive Graph Traversal with Self-Reflective Optimization*) governs the five traversal operations DCFN executes against the concept graph:

1. **Backward traversal** — recovers ancestor chains and surfaces forgotten predecessors that have decayed out of active research conversations.
2. **Forward cascade** — projects implications outward, tracking confidence decay and recording paths the cascade could not advance through (blocked paths).
3. **Entropy detection** — identifies structurally weak regions of the graph: orphans, contradictions, gaps, and stale convergence points.
4. **Branch cataloging** — discovers research clusters (emerging vs. established) and detects structural mirrors between clusters that have evolved in parallel.
5. **Golden-token pathfinding** — produces a recommended trajectory through the graph that resolves the highest-value entropy nodes given the current evidence base.

### 3.4 Apriori Co-Occurrence Pattern Discovery

An apriori miner runs over the corpus's combined attribute space to surface frequent itemsets and association rules — the structural side of pattern recognition that complements CTE's cognitive traversal. The miner contributes evidence to hypothesis generation and is referenced in **QECO Patent #74668095, Module 2**.

### 3.5 SVW — Synchronicity Weaver (Social Cognition)

The Synchronicity Weaver detects parallel discovery: groups of researchers who arrive at structurally similar findings without citing each other. SVW produces both convergence events (pairwise convergence clusters) and convergence anchors (hub papers with multiple independent orbiting groups). This is DCFN's social-cognition layer and feeds the Adaptive Learning claim under **Patent #74663931** (*Adaptive Learning Layer with Cross-Platform Network Effect*).

### 3.6 Hypothesis Generation

Hypotheses are produced structurally — not by free-form language generation. Each hypothesis is constructed from an entropy gap, the upstream chains feeding that gap, the blocked cascades downstream of it, and any apriori patterns that intersect it. Every generated hypothesis carries a traceable provenance back to specific graph nodes and specific structural conditions that triggered it.

### 3.7 Post-Traversal Calibration

After traversal, the engine compares the QEB confidence signals against the structural outcomes that traversal produced (which sources actually anchored chains, which produced cascades, which sat on the golden trajectory). The QEB is then re-tuned for the next run. This is the self-optimization claim under **Patent #74667530** (*Unified Multi-Phase Diagnostic Reasoning Engine and Autonomous AI Self-Optimization Ecosystem*). The adjustment is intentionally small per run — the engine learns over many runs, not one.

### 3.8 Diagnostic Reasoning

The end-to-end pipeline — encoding, graph construction, five-operation traversal, and gap surfacing — falls under **Diagnostic Engine Patent #74663354** (*Multi-Phase Diagnostic Reasoning Engine for Competency-Based Education Systems*). DCFN is one form of this engine; the underlying diagnostic reasoning loop is shared across all forms LEF Ai ships.

### 3.9 Contradiction Target Resolution (Go Deeper)

Free Article runs flag papers whose abstracts contain refutation language and surface those flags as CONTRADICTS issues during traversal. Go Deeper closes the loop: each flagged paper's contested-claim context is re-encoded into the same vector space as the rest of the corpus, then compared against every prior paper in the graph to identify the structural target(s) of the contradiction. CONTRADICTS edges are added between source and target, with cosine similarity carried as edge weight. The new edges feed back into entropy detection (CONTRADICTS issue), severity scoring (blockage signal), and confidence (penalty applied to the contested target). Resolution is deterministic and uses no external LLM calls — the same QEB embedding model that encoded the corpus encodes the contradiction context. This completes the contradiction-detection claim under **Diagnostic Engine Patent #74663354** by also identifying what is being contradicted, and adds typed CONTRADICTS edges to the concept graph governed by **CTE Patent #74802827**.

## Limitations

1. **QEB encoding**: When using TF-IDF + SVD fallback, semantic nuance may be lost for polysemous terms and domain-specific jargon. Sentence-BERT (all-MiniLM-L6-v2) mitigates this but is limited to 384-dimensional embeddings.

2. **Source coverage**: The Semantic Scholar API provides a subset of published research. Important works outside this index, preprints on non-indexed platforms, and unpublished research are not captured.

3. **Temporal decay calibration**: Parameters (λ=0.005, floor=0.15) are calibrated for research literature on year-scale decay. Domains with different publication rhythms (e.g., fast-moving ML vs. slow clinical trials) may need domain-specific calibration.

4. **Golden pathfinding**: The golden token algorithm uses greedy selection with backtracking. This produces robust paths but does not guarantee globally optimal trajectories.

5. **Abstract-only synthesis**: Gap-bridging proposals are synthesized from abstract text only. Full-text access would enable deeper, more specific synthesis.

6. **Citation completeness**: Citation edges depend on reference list coverage in the Semantic Scholar graph. Missing citations can create false ORPHAN detections.

7. **CONTRADICTS edges**: Cosine similarity (whether from TF-IDF or Sentence-BERT) cannot detect semantic contradiction directly. CONTRADICTS edges are inferred from structural patterns, not content analysis.