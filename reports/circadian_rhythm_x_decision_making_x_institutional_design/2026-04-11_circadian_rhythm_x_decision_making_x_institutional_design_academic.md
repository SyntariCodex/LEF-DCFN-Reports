# DCFN Technical Report: Circadian rhythm × decision making × institutional design

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `2cede1a8de4f3e8f`
**Corpus fingerprint:** `no-corpus`
**Sources:** 352

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
| Run timestamp | `2026-04-11T00:53:13.440771` |
| Run fingerprint | `2cede1a8de4f3e8f` |
| Corpus fingerprint | `no-corpus` |
| Domain | Circadian rhythm × decision making × institutional design |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 352 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 352 sources encoded |
| Concept graph | 368 nodes / 3528 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 5) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 350 entropy nodes inspected (201 critical, 48 high) |
| CTE branch cataloging | 7 clusters identified (10 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (7 entropy nodes resolved) |
| Apriori pattern mining | 19 1-itemsets, 43 2-itemsets, 14 3-itemsets, 11 rules |
| SVW synchronicity | 1385 candidate pairs scanned, 2 convergence events, 184 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 47.55 s |
| concept_graph | 552 ms |
| cte_traversal | 132 ms |
| apriori | 23 ms |
| svw | 40 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 109 ms |
| bridge_detection | 2 ms |
| **Total measured** | **48.41 s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 407 | 55 | 352 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 368 |
| Total edges | 3528 |
| Connected components | 40 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 352 |
| CONCEPT | 14 |
| ENTITY | 2 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 2821 |
| CONTAINS | 462 |
| EXTENDS | 192 |
| ENABLES | 28 |
| BRIDGES | 19 |
| DEFENDED_BY | 4 |
| DEPENDS_ON | 2 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Circadian rhythm, Circadian rhythm × decision making × institutional design, decision making, institutional design |
| Cross-domain edges | 311 |
| Bridge nodes | 148 |

### 2.3 Entropy Nodes

**Total:** 350 (critical: 201, high: 48, low: 101)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | A minimal model of peripheral clocks reveals differential circadian re-entrainme | — |
| 2 | Protein sequestration versus Hill-type repression in circadian clock models | — |
| 3 | A self-assessment questionnaire to determine morningness-eveningness in human ci | — |
| 4 | Circadian rhythm disturbances in depression | — |
| 5 | Ethics-Based Auditing of Automated Decision-Making Systems: Nature, Scope, and L | — |
| 6 | Enforcing Group Fairness in Algorithmic Decision Making: Utility Maximization Un | — |
| 7 | Decision making in dynamic and interactive environments based on cognitive hiera | — |
| 8 | Shared Decision Making: A Model for Clinical Practice | — |
| 9 | Ethical Decision Making by Individuals in Organizations: An Issue-Contingent Mod | — |
| 10 | Regret in Decision Making under Uncertainty | — |
| 11 | Institutional Design and Democratic Consolidation in the Third World | — |
| 12 | Institutional Transformation and Planning: From Institutionalization Theory to I | — |
| 13 | Social Capital and Local Governance: Exploring the Institutional Design Variable | — |
| 14 | Institutional design for complex technological systems | — |
| 15 | Problem Structure, Institutional Design, and the Relative Effectiveness of Inter | — |
| 16 | Circadian Rhythm Dysregulation and Restoration: The Role of Melatonin | — |
| 17 | Circadian rhythm and disease: Relationship, new insights, and future perspective | — |
| 18 | Circadian Rhythm, Clock Genes, and Hypertension: Recent Advances in Hypertension | — |
| 19 | Sleep, circadian rhythm, and gut microbiota. | — |
| 20 | The role of sleep deprivation and circadian rhythm disruption as risk factors of | — |

### 2.4 Branch Clusters

**Total clusters:** 7 (emerging: 2, established: 5)
**Structural mirrors:** 10

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| A self-assessment questionnaire to determine morningness-eveningness in human ci | 150 | Established |
| Measuring the efficiency of decision making units | 46 | Established |
| Circadian Blood Pressure Rhythm in Cardiovascular and Renal Health and Disease. | 2 | Emerging |
| The effects of circadian rhythm on reproductive functions. | 2 | Emerging |
| Emotion, Decision Making and the Orbitofrontal Cortex | 30 | Established |
| Shared Decision Making: A Model for Clinical Practice | 30 | Established |
| Policy Paradox: The Art of Political Decision Making | 69 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 2 |
| Convergence anchors | 184 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Shared Decision Making: A Model for Clinical Practice | 2012 | 27 |
| 2 | Shared decision-making in mental and behavioural health inte | 2019 | 23 |
| 3 | [Shared decision-making: ethical issues]. | 2023 | 22 |
| 4 | Shared decision making and physical therapy: What, when, how | 2022 | 19 |
| 5 | Institutions and Their Design | 1996 | 22 |
| 6 | Informed Consent and Decision-Making for Patients with Acqui | 2023 | 25 |
| 7 | Shared decision-making in palliative cancer care: A systemat | 2024 | 19 |
| 8 | Shared Decision Making: Radiology's Role and Opportunities. | 2020 | 18 |
| 9 | Shared decision-making in epilepsy management. | 2015 | 18 |
| 10 | Shared Decision Making: Improving Patient Outcomes by Unders | 2019 | 14 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 7 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Circadian Rhythm Dysregulation and Restoration: The Role of Melatonin | 2021 | Yes |
| 2 | A minimal model of peripheral clocks reveals differential circadian re | 2022 | Yes |
| 3 | Circadian Rhythm, Clock Genes, and Hypertension: Recent Advances in Hy | 2021 | Yes |
| 4 | Circadian rhythm disturbances in depression | 2008 | Yes |
| 5 | Circadian rhythm and disease: Relationship, new insights, and future p | 2022 | Yes |
| 6 | Protein sequestration versus Hill-type repression in circadian clock m | 2016 | Yes |
| 7 | The role of sleep deprivation and circadian rhythm disruption as risk  | 2019 | Yes |
| 8 | Effects of light on human circadian rhythms, sleep and mood | 2019 | — |
| 9 | Molecular regulations of circadian rhythm and implications for physiol | 2022 | — |
| 10 | Effect of Circadian Rhythm on Metabolic Processes and the Regulation o | 2019 | — |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [HIGH]
- **Hypothesis:** Resolving the research gap in 'A minimal model of peripheral clocks reveals differential circadian...' will unlock currently blocked progress toward: Physics
- **Grounded in:** entropy gap node: A minimal model of peripheral clocks reveals differential... + included in golden token recommended path
- **Novel because:** not yet connected to 'Physics' despite logical dependency in prerequisite chain
- **Suggested method:** simulation (co-occurs with similar gaps at 96% confidence in apriori patterns)

**H02** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Protein sequestration versus Hill-type repression in circadian cloc...' will unlock currently blocked progress toward: Biology
- **Grounded in:** entropy gap node: Protein sequestration versus Hill-type repression in circ... + included in golden token recommended path
- **Novel because:** not yet connected to 'Biology' despite logical dependency in prerequisite chain
- **Suggested method:** simulation (co-occurs with similar gaps at 96% confidence in apriori patterns)

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'A self-assessment questionnaire to determine morningness-eveningnes...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: A self-assessment questionnaire to determine morningness-...
- **Novel because:** not yet connected to 'Neuroscience' despite logical dependency in prerequisite chain
- **Suggested method:** simulation (co-occurs with similar gaps at 96% confidence in apriori patterns)

**H04** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Circadian rhythm disturbances in depression' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Circadian rhythm disturbances in depression + included in golden token recommended path
- **Novel because:** absent from 'A self-assessment questionnaire to determine mo...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** simulation (co-occurs with similar gaps at 96% confidence in apriori patterns)

**H05** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Ethics-Based Auditing of Automated Decision-Making Systems: Nature,...' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Ethics-Based Auditing of Automated Decision-Making System...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** simulation (co-occurs with similar gaps at 96% confidence in apriori patterns)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 3 |
| 2 | Untitled | 3 |
| 3 | Untitled | 3 |
| 4 | Untitled | 3 |
| 5 | Untitled | 2 |
| 6 | Untitled | 3 |
| 7 | Untitled | 2 |
| 8 | Untitled | 3 |
| 9 | Untitled | 2 |
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