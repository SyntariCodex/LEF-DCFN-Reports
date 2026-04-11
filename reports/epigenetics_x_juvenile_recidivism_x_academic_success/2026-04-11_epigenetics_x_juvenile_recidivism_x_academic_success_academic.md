# Technical Report: Epigenetics × juvenile recidivism × academic success

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `3745ae2702869264`
**Corpus fingerprint:** `no-corpus`
**Sources:** 425

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
| Run timestamp | `2026-04-11T20:32:52.145563` |
| Run fingerprint | `3745ae2702869264` |
| Corpus fingerprint | `no-corpus` |
| Domain | Epigenetics × juvenile recidivism × academic success |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 425 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 425 sources encoded |
| Concept graph | 441 nodes / 5970 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 5) |
| CTE forward cascade | 5 cascades (1 implications, 0 blocked paths) |
| CTE entropy detection | 421 entropy nodes inspected (303 critical, 51 high) |
| CTE branch cataloging | 5 clusters identified (1 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (5 entropy nodes resolved) |
| Apriori pattern mining | 21 1-itemsets, 45 2-itemsets, 8 3-itemsets, 8 rules |
| SVW synchronicity | 4003 candidate pairs scanned, 2 convergence events, 265 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 1m 16.0s |
| concept_graph | 489 ms |
| cte_traversal | 270 ms |
| apriori | 29 ms |
| svw | 371 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 340 ms |
| bridge_detection | 4 ms |
| **Total measured** | **1m 17.5s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 457 | 32 | 425 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 441 |
| Total edges | 5970 |
| Connected components | 25 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 425 |
| CONCEPT | 11 |
| ENTITY | 5 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 4759 |
| EXTENDS | 619 |
| CONTAINS | 516 |
| ENABLES | 38 |
| BRIDGES | 20 |
| DEFENDED_BY | 13 |
| DEPENDS_ON | 5 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Epigenetics, Epigenetics × juvenile recidivism × academic success, academic success, juvenile recidivism |
| Cross-domain edges | 427 |
| Bridge nodes | 220 |

### 2.3 Entropy Nodes

**Total:** 421 (critical: 303, high: 51, low: 67)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Decriminalizing Delinquency: The Effect of Raising the Age of Majority on Juveni | — |
| 2 | Motivation as an Enabler for Academic Success | — |
| 3 | Does Emotional Intelligence Assist in the Prediction of Academic Success? | — |
| 4 | Magnetic Polymer Models for Epigenetics-Driven Chromosome Folding | — |
| 5 | Epigenetic Transitions and Knotted Solitons in Stretched Chromatin | — |
| 6 | Epigenetic factor competition reshapes the EMT landscape | — |
| 7 | Shaping Epigenetic Memory via Genomic Bookmarking | — |
| 8 | The Effect of Epigenetic Blocking on Dynamic Multi-Objective Optimisation Proble | — |
| 9 | Update on the genetic and epigenetic etiology of gestational diabetes mellitus:  | — |
| 10 | The epigenetics of perinatal stress . | — |
| 11 | Sirtuins, epigenetics and longevity. | — |
| 12 | Leveraging epigenetics to enhance the efficacy of immunotherapy. | — |
| 13 | Environmental epigenetics of sex differences in the brain. | — |
| 14 | Epigenetic Reprogramming in Mammalian Development | — |
| 15 | DNA methylation and epigenetic inheritance | — |
| 16 | An operational definition of epigenetics: Figure 1. | — |
| 17 | Epigenetic Reprogramming in Plant and Animal Development | — |
| 18 | Effectiveness of social-therapeutic treatment for serious offenders in juvenile  | — |
| 19 | Accuracy, Fairness, and Interpretability of Machine Learning Criminal Recidivism | — |
| 20 | A Decision Tree Approach to Predicting Recidivism in Domestic Violence | — |

### 2.4 Branch Clusters

**Total clusters:** 5 (emerging: 2, established: 3)
**Structural mirrors:** 1

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| An operational definition of epigenetics: Figure 1. | 151 | Established |
| Variables Related to Recidivism among Juvenile Offenders | 257 | Established |
| Effect of juvenile justice financial sanctions on youths' recidivism. | 5 | Emerging |
| Lower Limb Rehabilitation in Juvenile Idiopathic Arthritis using Serious Games | 2 | Established |
| Juvenile Justice-Based Interdisciplinary Collective Care: An Innovative Approach | 2 | Emerging |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 2 |
| Convergence anchors | 265 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Cancer epigenetics: an introduction. | 2015 | 49 |
| 2 | The Development of Epigenetics in the Study of Disease Patho | 2020 | 48 |
| 3 | Cancer epigenetics: from mechanism to therapy. | 2012 | 47 |
| 4 | Cancer Epigenetics: An Overview. | 2022 | 47 |
| 5 | Epigenetics: What it is about? | 2015 | 47 |
| 6 | Epigenetics in Health and Disease. | 2020 | 48 |
| 7 | Role of epigenetics in carcinogenesis: Recent advancements i | 2022 | 45 |
| 8 | Advances in epigenetics link genetics to the environment and | 2019 | 43 |
| 9 | Epigenetics: Regulation Through Repression | 1999 | 45 |
| 10 | Targeting Epigenetics in Lung Cancer. | 2021 | 46 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 5 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Epigenetics-targeted drugs: current paradigms and future challenges | 2024 | — |
| 2 | Environmental epigenetics of sex differences in the brain. | 2020 | Yes |
| 3 | Cancer epigenetics in clinical practice | 2022 | — |
| 4 | Cancer epigenetics: from laboratory studies and clinical trials to pre | 2024 | — |
| 5 | An operational definition of epigenetics: Figure 1. | 2009 | Yes |
| 6 | Magnetic Polymer Models for Epigenetics-Driven Chromosome Folding | 2019 | Yes |
| 7 | Epigenetic factor competition reshapes the EMT landscape | 2022 | Yes |
| 8 | Machine learning and clinical epigenetics: a review of challenges for  | 2020 | — |
| 9 | Leveraging epigenetics to enhance the efficacy of immunotherapy. | 2021 | Yes |
| 10 | Epigenetics in hepatocellular carcinoma. | 2021 | — |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Decriminalizing Delinquency: The Effect of Raising the Age of Major...' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Decriminalizing Delinquency: The Effect of Raising the Ag...
- **Novel because:** absent from 'Building academic success on social and emotion...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Motivation as an Enabler for Academic Success' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Motivation as an Enabler for Academic Success
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Does Emotional Intelligence Assist in the Prediction of Academic Su...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Does Emotional Intelligence Assist in the Prediction of A...
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H04** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Magnetic Polymer Models for Epigenetics-Driven Chromosome Folding' will unlock currently blocked progress toward: Physics
- **Grounded in:** entropy gap node: Magnetic Polymer Models for Epigenetics-Driven Chromosome... + included in golden token recommended path
- **Novel because:** not yet connected to 'Physics' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Epigenetic Transitions and Knotted Solitons in Stretched Chromatin' will unlock currently blocked progress toward: Physics
- **Grounded in:** entropy gap node: Epigenetic Transitions and Knotted Solitons in Stretched ...
- **Novel because:** absent from 'Epigenetic Regulations of GABAergic Neurotransm...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 2 |
| 2 | Untitled | 2 |
| 3 | Untitled | 2 |
| 4 | Untitled | 3 |
| 5 | Untitled | 3 |
| 6 | Untitled | 2 |
| 7 | Untitled | 3 |
| 8 | Untitled | 2 |
| 9 | Untitled | 3 |
| 10 | Untitled | 2 |

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