# DCFN Technical Report: Neuroplasticity × music cognition × language acquisition

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `f4dac3ab23cf0d21`
**Corpus fingerprint:** `no-corpus`
**Sources:** 442

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
| Run timestamp | `2026-04-11T01:30:23.053955` |
| Run fingerprint | `f4dac3ab23cf0d21` |
| Corpus fingerprint | `no-corpus` |
| Domain | Neuroplasticity × music cognition × language acquisition |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 442 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 442 sources encoded |
| Concept graph | 468 nodes / 9536 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 6) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 426 entropy nodes inspected (344 critical, 47 high) |
| CTE branch cataloging | 4 clusters identified (2 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (8 entropy nodes resolved) |
| Apriori pattern mining | 20 1-itemsets, 40 2-itemsets, 16 3-itemsets, 20 rules |
| SVW synchronicity | 3236 candidate pairs scanned, 1 convergence events, 284 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 1m 45.0s |
| concept_graph | 705 ms |
| cte_traversal | 339 ms |
| apriori | 29 ms |
| svw | 535 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 472 ms |
| bridge_detection | 5 ms |
| **Total measured** | **1m 47.1s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 462 | 20 | 442 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 468 |
| Total edges | 9536 |
| Connected components | 17 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 442 |
| ENTITY | 14 |
| CONCEPT | 12 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 7705 |
| BRIDGES | 688 |
| CONTAINS | 590 |
| EXTENDS | 479 |
| ENABLES | 40 |
| DEFENDED_BY | 29 |
| DEPENDS_ON | 5 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Neuroplasticity, Neuroplasticity × music cognition × language acquisition, language acquisition, music cognition |
| Cross-domain edges | 1944 |
| Bridge nodes | 385 |

### 2.3 Entropy Nodes

**Total:** 426 (critical: 344, high: 47, low: 35)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Differential Background Music as Attentional Resources Interacting with Cognitiv | — |
| 2 | Hebbian Plasticity for Improving Perceptual Decisions | — |
| 3 | Sketch of a novel approach to a neural model | — |
| 4 | Lifelong Learning Starting From Zero | — |
| 5 | Molecular Mechanisms of Neuroplasticity: An Expanding Universe. | — |
| 6 | Acute and Chronic Craniofacial Pain: Brainstem Mechanisms of Nociceptive Transmi | — |
| 7 | Central Neuroplasticity and Pathological Pain | — |
| 8 | Miscommunication of science: music cognition research in the popular press | — |
| 9 | Models of Music Cognition and Composition | — |
| 10 | Music SketchNet: Controllable Music Generation via Factorized Representations of | — |
| 11 | Mozart Effect, Cognitive Dissonance, and the Pleasure of Music | — |
| 12 | Musical emotions: functions, origins, evolution. | — |
| 13 | Random Feedback Makes Listeners Tone-Deaf. | — |
| 14 | The sound symbolism bootstrapping hypothesis for language acquisition and langua | — |
| 15 | Motivational variables in second-language acquisition. | — |
| 16 | Chaos/Complexity Science and Second Language Acquisition | — |
| 17 | Alternative Approaches to Second Language Acquisition | — |
| 18 | Second Language Acquisition and Task-Based Language Teaching | — |
| 19 | Handbook of Cognitive Linguistics and Second Language Acquisition | — |
| 20 | Awareness and Second Language Acquisition | — |

### 2.4 Branch Clusters

**Total clusters:** 4 (emerging: 0, established: 4)
**Structural mirrors:** 2

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| A survey on large language model based autonomous agents | 348 | Established |
| The neurorehabilitation of post-stroke dysphagia: Physiology and pathophysiology | 2 | Established |
| Principles and Practice in Second Language Acquisition | 99 | Established |
| Continuity, discontinuity, and atypicality in early language acquisition. | 4 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 1 |
| Convergence anchors | 284 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | No Encore: Unlearning as Opt-Out in Music Generation | 2025 | 31 |
| 2 | Second Language Acquisition and Universal Grammar | 2003 | 28 |
| 3 | Handbook of Second Language Acquisition | 1998 | 30 |
| 4 | Modeling Musical Context with Word2vec | 2017 | 28 |
| 5 | An Introduction to Second Language Acquisition Research | 2014 | 23 |
| 6 | Language acquisition: the acquisition of linguistic structur | 1997 | 25 |
| 7 | The Handbook of Second Language Acquisition | 2005 | 25 |
| 8 | Unsupervised Language Acquisition | 1996 | 31 |
| 9 | Exploring the Role of Neuroplasticity in Development, Aging, | 2023 | 26 |
| 10 | SLABERT Talk Pretty One Day: Modeling Second Language Acquis | 2023 | 30 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 8 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Second Language Acquisition and Task-Based Language Teaching | 2014 | Yes |
| 2 | Individual Differences in Language Acquisition and Processing. | 2018 | — |
| 3 | Random Feedback Makes Listeners Tone-Deaf. | 2018 | Yes |
| 4 | Models of Music Cognition and Composition | 2022 | Yes |
| 5 | Differential Background Music as Attentional Resources Interacting wit | 2022 | Yes |
| 6 | Miscommunication of science: music cognition research in the popular p | 2015 | Yes |
| 7 | Mozart Effect, Cognitive Dissonance, and the Pleasure of Music | 2012 | Yes |
| 8 | Cross-Cultural Work in Music Cognition: Challenges, Insights, and Reco | 2020 | — |
| 9 | Musical emotions: functions, origins, evolution. | 2010 | Yes |
| 10 | Music SketchNet: Controllable Music Generation via Factorized Represen | 2020 | Yes |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Differential Background Music as Attentional Resources Interacting ...' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Differential Background Music as Attentional Resources In... + included in golden token recommended path
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 92% confidence in apriori patterns)

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Hebbian Plasticity for Improving Perceptual Decisions' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Hebbian Plasticity for Improving Perceptual Decisions
- **Novel because:** not yet connected to 'Biology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 92% confidence in apriori patterns)

**H03** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Sketch of a novel approach to a neural model' will unlock currently blocked progress toward: Biology
- **Grounded in:** entropy gap node: Sketch of a novel approach to a neural model
- **Novel because:** not yet connected to 'Biology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 92% confidence in apriori patterns)

**H04** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Lifelong Learning Starting From Zero' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Lifelong Learning Starting From Zero
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 92% confidence in apriori patterns)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Molecular Mechanisms of Neuroplasticity: An Expanding Universe.' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Molecular Mechanisms of Neuroplasticity: An Expanding Uni...
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 92% confidence in apriori patterns)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 4 |
| 2 | Untitled | 4 |
| 3 | Untitled | 3 |
| 4 | Untitled | 4 |
| 5 | Untitled | 3 |
| 6 | Untitled | 3 |
| 7 | Untitled | 3 |
| 8 | Untitled | 3 |
| 9 | Untitled | 3 |
| 10 | Untitled | 4 |

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