# DCFN Technical Report: Sleep Deprivation × Executive Function × Classroom Behavior

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `ac03edc79bd19094`
**Corpus fingerprint:** `no-corpus`
**Sources:** 410

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
| Run timestamp | `2026-04-11T03:48:20.794877` |
| Run fingerprint | `ac03edc79bd19094` |
| Corpus fingerprint | `no-corpus` |
| Domain | Sleep Deprivation × Executive Function × Classroom Behavior |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 410 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 410 sources encoded |
| Concept graph | 425 nodes / 7965 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 5) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 408 entropy nodes inspected (322 critical, 38 high) |
| CTE branch cataloging | 5 clusters identified (4 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (7 entropy nodes resolved) |
| Apriori pattern mining | 23 1-itemsets, 56 2-itemsets, 22 3-itemsets, 23 rules |
| SVW synchronicity | 3317 candidate pairs scanned, 3 convergence events, 254 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 1m 9.9s |
| concept_graph | 400 ms |
| cte_traversal | 316 ms |
| apriori | 32 ms |
| svw | 243 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 377 ms |
| bridge_detection | 6 ms |
| **Total measured** | **1m 11.3s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 453 | 43 | 410 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 425 |
| Total edges | 7965 |
| Connected components | 18 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 410 |
| CONCEPT | 10 |
| ENTITY | 5 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 6426 |
| BRIDGES | 598 |
| CONTAINS | 513 |
| EXTENDS | 288 |
| ENABLES | 120 |
| DEFENDED_BY | 10 |
| DEPENDS_ON | 10 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Classroom Behavior, Executive Function, Sleep Deprivation, Sleep Deprivation × Executive Function × Classroom Behavior |
| Cross-domain edges | 1584 |
| Bridge nodes | 358 |

### 2.3 Entropy Nodes

**Total:** 408 (critical: 322, high: 38, low: 48)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | School Discipline and Disruptive Classroom Behavior: The Moderating Effects of S | — |
| 2 | Sleep and its relation to cognition and behaviour in preschool-aged children of  | — |
| 3 | Sleep deprivation therapy. | — |
| 4 | Sleep Disorders in Adolescents. | — |
| 5 | Sleep deprivation induces fragmented memory loss. | — |
| 6 | A systematic review of sleep deprivation and technical skill in surgery. | — |
| 7 | [Sleep deprivation and pain: a review of the newest literature]. | — |
| 8 | Sleep Deprivation in the Rat: X. Integration and Discussion of the Findings | — |
| 9 | Energy expenditure during sleep, sleep deprivation and sleep following sleep dep | — |
| 10 | Examining the Effects of Sleep Deprivation on Workplace Deviance: A Self-Regulat | — |
| 11 | Sex differences in network controllability as a predictor of executive function  | — |
| 12 | The central executive network and executive function in healthy and persons with | — |
| 13 | Research Review: Executive function deficits in fetal alcohol spectrum disorders | — |
| 14 | Executive function in children with sickle cell anemia on transfusion: NIH toolb | — |
| 15 | Executive Functions and Developmental Psychopathology | — |
| 16 | Executive Function Deficits in High‐Functioning Autistic Individuals: Relationsh | — |
| 17 | Executive Functioning as a Predictor of Children's Mathematics Ability: Inhibiti | — |
| 18 | Practitioner Review: Do performance‐based measures and ratings of executive func | — |
| 19 | Efficacy of behavioral classroom programs in primary school. A meta-analysis foc | — |
| 20 | Observed classroom behavior of children with ADHD: relationship to gender and co | — |

### 2.4 Branch Clusters

**Total clusters:** 5 (emerging: 0, established: 5)
**Structural mirrors:** 4

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| Sleep deprivation and its association with diseases- a review. | 150 | Established |
| Assessment of executive functions: Review of instruments and identification of c | 250 | Established |
| The Behavioural House Indicator: A faster and real time small-area indicative de | 5 | Established |
| Executive function deficits in congenital heart disease: why is intervention imp | 2 | Established |
| Do actions speak louder than words? Classroom attitudes and behavior in relation | 3 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 3 |
| Convergence anchors | 254 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | SCB-Dataset3: A Benchmark for Detecting Student Classroom Be | 2023 | 23 |
| 2 | TILES-2018 Sleep Benchmark Dataset: A Longitudinal Wearable  | 2025 | 27 |
| 3 | Sleep deprivation and its association with diseases- a revie | 2020 | 20 |
| 4 | Reductions in aggressive behavior within the context of a un | 2018 | 22 |
| 5 | Role of sleep deprivation in immune-related disease risk and | 2021 | 23 |
| 6 | Real-Time Attention Monitoring System for Classroom: A Deep  | 2023 | 22 |
| 7 | Roles of sleep deprivation in cardiovascular dysfunctions | 2019 | 21 |
| 8 | [Executive function deficits following stroke]. | 2013 | 23 |
| 9 | Sleep Deprivation and Activation of Morning Levels of Cellul | 2006 | 24 |
| 10 | Student Classroom Behavior Detection based on Improved YOLOv | 2023 | 19 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 7 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Practitioner Review: Do performance‐based measures and ratings of exec | 2012 | Yes |
| 2 | Sex differences in network controllability as a predictor of executive | 2018 | Yes |
| 3 | The central executive network and executive function in healthy and pe | 2022 | Yes |
| 4 | Association of Sex With Neurobehavioral Markers of Executive Function  | 2023 | — |
| 5 | Executive function in children with sickle cell anemia on transfusion: | 2022 | Yes |
| 6 | The role of prefrontal cortex in cognitive control and executive funct | 2021 | — |
| 7 | Sleep deprivation differentially affects subcomponents of cognitive co | 2019 | — |
| 8 | Examining the Effects of Sleep Deprivation on Workplace Deviance: A Se | 2011 | Yes |
| 9 | Sleep and its relation to cognition and behaviour in preschool-aged ch | 2019 | Yes |
| 10 | [Sleep deprivation and pain: a review of the newest literature]. | 2014 | Yes |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'School Discipline and Disruptive Classroom Behavior: The Moderating...' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: School Discipline and Disruptive Classroom Behavior: The ...
- **Novel because:** absent from 'Behavioral inhibition, sustained attention, and...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** machine learning (co-occurs with similar gaps at 76% confidence in apriori patterns)

**H02** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Sleep and its relation to cognition and behaviour in preschool-aged...' will unlock currently blocked progress toward: Biology
- **Grounded in:** entropy gap node: Sleep and its relation to cognition and behaviour in pres... + included in golden token recommended path
- **Novel because:** not yet connected to 'Biology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 76% confidence in apriori patterns)

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Sleep deprivation therapy.' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Sleep deprivation therapy.
- **Novel because:** not yet connected to 'The prospective association between sleep deprivation and de' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 76% confidence in apriori patterns)

**H04** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Sleep Disorders in Adolescents.' will unlock currently blocked progress toward: Sleep Duration and Executive Function in Adults.
- **Grounded in:** entropy gap node: Sleep Disorders in Adolescents.
- **Novel because:** absent from 'The Cumulative Cost of Additional Wakefulness: ...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** machine learning (co-occurs with similar gaps at 76% confidence in apriori patterns)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Sleep deprivation induces fragmented memory loss.' will unlock currently blocked progress toward: Sleep Duration and Executive Function in Adults.
- **Grounded in:** entropy gap node: Sleep deprivation induces fragmented memory loss.
- **Novel because:** absent from 'The Cumulative Cost of Additional Wakefulness: ...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** machine learning (co-occurs with similar gaps at 76% confidence in apriori patterns)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 3 |
| 2 | Untitled | 3 |
| 3 | Untitled | 2 |
| 4 | Untitled | 3 |
| 5 | Untitled | 2 |
| 6 | Untitled | 3 |
| 7 | Untitled | 3 |
| 8 | Untitled | 3 |
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