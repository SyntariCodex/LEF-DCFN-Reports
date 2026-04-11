# DCFN Technical Report: Adverse Childhood Experiences × Recidivism Prediction × Blockchain Data Sharing

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `579f0cdf83958978`
**Corpus fingerprint:** `no-corpus`
**Sources:** 430

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
| Run timestamp | `2026-04-11T03:10:45.277909` |
| Run fingerprint | `579f0cdf83958978` |
| Corpus fingerprint | `no-corpus` |
| Domain | Adverse Childhood Experiences × Recidivism Prediction × Blockchain Data Sharing |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 430 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 430 sources encoded |
| Concept graph | 488 nodes / 5651 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 7) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 407 entropy nodes inspected (294 critical, 34 high) |
| CTE branch cataloging | 4 clusters identified (3 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (2 entropy nodes resolved) |
| Apriori pattern mining | 22 1-itemsets, 48 2-itemsets, 13 3-itemsets, 15 rules |
| SVW synchronicity | 7476 candidate pairs scanned, 1 convergence events, 281 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 1m 43.6s |
| concept_graph | 603 ms |
| cte_traversal | 216 ms |
| apriori | 29 ms |
| svw | 455 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 275 ms |
| bridge_detection | 4 ms |
| **Total measured** | **1m 45.2s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 483 | 53 | 430 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 488 |
| Total edges | 5651 |
| Connected components | 19 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 430 |
| ENTITY | 48 |
| CONCEPT | 10 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 3165 |
| EXTENDS | 1342 |
| CONTAINS | 477 |
| BRIDGES | 447 |
| ENABLES | 108 |
| DEFENDED_BY | 103 |
| DEPENDS_ON | 9 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Adverse Childhood Experiences, Adverse Childhood Experiences × Recidivism Prediction × Blockchain Data Sharing, Blockchain Data Sharing, Recidivism Prediction |
| Cross-domain edges | 1253 |
| Bridge nodes | 326 |

### 2.3 Entropy Nodes

**Total:** 407 (critical: 294, high: 34, low: 79)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Ontology-Driven Self-Supervision for Adverse Childhood Experiences Identificatio | — |
| 2 | Adverse childhood experiences and premature all-cause mortality | — |
| 3 | Clients' current presentation yields best prediction of criminal recidivism: Joi | — |
| 4 | A Decision Tree Approach to Predicting Recidivism in Domestic Violence | — |
| 5 | Methodological advances in statistical prediction. | — |
| 6 | Neighborhood Risk Factors for Recidivism: For Whom do they Matter? | — |
| 7 | Criminal thought process as a dynamic risk factor: Variable- and person-oriented | — |
| 8 | Prediction of General and Violent Recidivism Among Mentally Disordered Adult Off | — |
| 9 | Anger and Prediction of Violent and Nonviolent Offenders' Recidivism | — |
| 10 | The Prediction of Recidivism with Aboriginal Offenders: A Theoretically Informed | — |
| 11 | Trusted Data Notifications from Private Blockchains | — |
| 12 | Association of Adverse Childhood Experiences and Social Isolation With Later-Lif | — |
| 13 | The Influence of Adverse Childhood Experiences in Pain Management: Mechanisms, P | — |
| 14 | Adverse Childhood Experiences and the Consequences on Neurobiological, Psychosoc | — |
| 15 | Lest we forget: comparing retrospective and prospective assessments of adverse c | — |
| 16 | Blockchain-Enabled Secure Data Sharing Scheme in Mobile-Edge Computing: An Async | — |
| 17 | The effect of multiple adverse childhood experiences on health: a systematic rev | — |
| 18 | Prevalence of Adverse Childhood Experiences From the 2011-2014 Behavioral Risk F | — |
| 19 | Adverse childhood experiences and associated health outcomes: A systematic revie | — |
| 20 | Life course health consequences and associated annual costs of adverse childhood | — |

### 2.4 Branch Clusters

**Total clusters:** 4 (emerging: 1, established: 3)
**Structural mirrors:** 3

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| The effect of multiple adverse childhood experiences on health: a systematic rev | 272 | Established |
| Blockchain and Federated Learning for Privacy-Preserved Data Sharing in Industri | 194 | Established |
| The association between adverse childhood experiences and childhood obesity: A s | 2 | Emerging |
| Data Encoding for Byzantine-Resilient Distributed Optimization | 2 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 1 |
| Convergence anchors | 281 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Blockchain-Based Sharing and Tamper-Proof Framework of Big D | 2020 | 44 |
| 2 | Blockchain Based Intelligent Vehicle Data sharing Framework | 2017 | 47 |
| 3 | Towards Blockchain-based Auditable Storage and Sharing of Io | 2017 | 43 |
| 4 | Secure Data Sharing over Vehicular Networks Based on Multi-s | 2023 | 40 |
| 5 | A Blockchain-Enabled Multi-Authority Secure IoT Data-Sharing | 2025 | 39 |
| 6 | Blockchain Interoperability Landscape | 2022 | 43 |
| 7 | Blockchain-Based Anonymous Data Sharing With Accountability  | 2023 | 39 |
| 8 | Secure and Efficient Data Sharing Among Vehicles Based on Co | 2021 | 40 |
| 9 | Digital Twins and Blockchain for IoT Management | 2023 | 40 |
| 10 | Secure Data Sharing for Consortium Blockchain-Enabled Vehicu | 2024 | 39 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | MEDIUM |
| Entropy nodes resolved | 2 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Blockchain-Enabled Secure Data Sharing Scheme in Mobile-Edge Computing | 2020 | Yes |
| 2 | Blockchain Empowered Asynchronous Federated Learning for Secure Data S | 2020 | — |
| 3 | Data Security Sharing and Storage Based on a Consortium Blockchain in  | 2019 | — |
| 4 | Secure and Efficient Data Sharing Among Vehicles Based on Consortium B | 2021 | — |
| 5 | LVBS: Lightweight Vehicular Blockchain for Secure Data Sharing in Disa | 2020 | — |
| 6 | SPDS: A Secure and Auditable Private Data Sharing Scheme for Smart Gri | 2020 | — |
| 7 | Trusted Data Notifications from Private Blockchains | 2021 | Yes |
| 8 | Benchmarking blockchain-based gene-drug interaction data sharing metho | 2021 | — |
| 9 | Towards Secure and Privacy-Preserving Data Sharing for COVID-19 Medica | 2021 | — |
| 10 | Efficient and Secure Data Sharing for 5G Flying Drones: A Blockchain-E | 2021 | — |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Ontology-Driven Self-Supervision for Adverse Childhood Experiences ...' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Ontology-Driven Self-Supervision for Adverse Childhood Ex...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)

**H02** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Adverse childhood experiences and premature all-cause mortality' will unlock currently blocked progress toward: Biology
- **Grounded in:** entropy gap node: Adverse childhood experiences and premature all-cause mor...
- **Novel because:** not yet connected to 'Biology' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)

**H03** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Clients' current presentation yields best prediction of criminal re...' will unlock currently blocked progress toward: Medicine
- **Grounded in:** entropy gap node: Clients' current presentation yields best prediction of c...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)

**H04** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'A Decision Tree Approach to Predicting Recidivism in Domestic Violence' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: A Decision Tree Approach to Predicting Recidivism in Dome...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Methodological advances in statistical prediction.' will unlock currently blocked progress toward: Education
- **Grounded in:** entropy gap node: Methodological advances in statistical prediction.
- **Novel because:** not yet connected to 'Education' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)


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