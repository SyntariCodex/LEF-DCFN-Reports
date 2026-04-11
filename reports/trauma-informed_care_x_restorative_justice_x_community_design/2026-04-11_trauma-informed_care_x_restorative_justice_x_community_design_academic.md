# DCFN Technical Report: Trauma-informed care × restorative justice × community design

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `afd333daa409c773`
**Corpus fingerprint:** `no-corpus`
**Sources:** 422

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
| Run timestamp | `2026-04-11T04:15:51.068847` |
| Run fingerprint | `afd333daa409c773` |
| Corpus fingerprint | `no-corpus` |
| Domain | Trauma-informed care × restorative justice × community design |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 422 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 422 sources encoded |
| Concept graph | 457 nodes / 5768 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 5) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 399 entropy nodes inspected (293 critical, 46 high) |
| CTE branch cataloging | 6 clusters identified (7 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (7 entropy nodes resolved) |
| Apriori pattern mining | 20 1-itemsets, 30 2-itemsets, 7 3-itemsets, 9 rules |
| SVW synchronicity | 3435 candidate pairs scanned, 1 convergence events, 255 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 1m 6.0s |
| concept_graph | 400 ms |
| cte_traversal | 469 ms |
| apriori | 28 ms |
| svw | 325 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 314 ms |
| bridge_detection | 4 ms |
| **Total measured** | **1m 7.6s** |

### 1.5 Filter Telemetry

*The DCFN engine applies a topical-relevance filter on ingested sources before they reach the graph. The telemetry below records what each filter inspected, dropped, and kept on this run. Drops are evidence the engine enforces its own quality bar.*

| Filter | Inspected | Dropped | Kept |
|--------|-----------|---------|------|
| contamination_filter | 486 | 64 | 422 |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 457 |
| Total edges | 5768 |
| Connected components | 15 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 422 |
| ENTITY | 21 |
| CONCEPT | 14 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 2830 |
| EXTENDS | 1837 |
| BRIDGES | 591 |
| CONTAINS | 397 |
| ENABLES | 56 |
| DEFENDED_BY | 48 |
| DEPENDS_ON | 9 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Trauma-informed care, Trauma-informed care × restorative justice × community design, community design, restorative justice |
| Cross-domain edges | 1260 |
| Bridge nodes | 320 |

### 2.3 Entropy Nodes

**Total:** 399 (critical: 293, high: 46, low: 60)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Data Justice Stories: A Repository of Case Studies | — |
| 2 | Toward a Theory of Justice for Artificial Intelligence | — |
| 3 | Restorative Justice: Pedagogy, Praxis, and Discipline | — |
| 4 | Community-Based Trauma-Informed Care Following Immigrant Family Reunification: A | — |
| 5 | Sita's Trousseau: restorative justice, domestic violence, and South Asian cultur | — |
| 6 | Restorative justice | — |
| 7 | Setting Standards for Restorative Justice | — |
| 8 | Restorative Justice and Gendered Violence: Diversion or Effective Justice? | — |
| 9 | Restorative Justice and De-Professionalization | — |
| 10 | An annotation based approach to support design communication | — |
| 11 | Healthy Aging and Where You Live: Community Design Relationships With Physical A | — |
| 12 | Building Successful Online Communities: Evidence-Based Social Design | — |
| 13 | What are effective strategies for implementing trauma-informed care in youth inp | — |
| 14 | Radical Futures: Supporting Community-Led Design Engagements through an Afrofutu | — |
| 15 | Deconstructing Community-Based Collaborative Design | — |
| 16 | Enhancing Community-Based Participatory Research Through Human-Centered Design S | — |
| 17 | Trauma-informed care: recognizing and resisting re-traumatization in health care | — |
| 18 | Trauma-informed Care Interventions in Emergency Medicine: A Systematic Review | — |
| 19 | Trauma-informed care in the UK: where are we? A qualitative study of health poli | — |
| 20 | Understanding the Conceptualization and Operationalization of Trauma-Informed Ca | — |

### 2.4 Branch Clusters

**Total clusters:** 6 (emerging: 1, established: 5)
**Structural mirrors:** 7

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| Restorative justice | 303 | Established |
| Trauma-Informed Care: The Professional Development Needs of Early Childhood Spec | 4 | Emerging |
| Audience-specific online community design | 126 | Established |
| Virtual Community: An Open World for Humans, Robots, and Society | 5 | Established |
| Creating Walkable Communities: Understanding Trade-Offs. | 2 | Established |
| Processes of developing 'community livability' in older age. | 3 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 1 |
| Convergence anchors | 255 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Evaluating the Effectiveness of Trauma-Informed Care Framewo | 2024 | 18 |
| 2 | Supporting Active Living Through Community Plans: The Associ | 2019 | 30 |
| 3 | Smart growth community design and physical activity in child | 2013 | 26 |
| 4 | Healthy Community Design, Anti-displacement, and Equity Stra | 2022 | 26 |
| 5 | The Impact of Community Design and Land-Use Choices on Publi | 2003 | 24 |
| 6 | Community Lenses Revealing the Role of Sociocultural Environ | 2016 | 27 |
| 7 | An ecological approach to creating active living communities | 2006 | 22 |
| 8 | Codesigning Parks for Increasing Park Visits and Physical Ac | 2020 | 21 |
| 9 | Physical Activity–Friendly Policies and Community Design Fea | 2023 | 23 |
| 10 | Community Design for Physical Activity | 2011 | 21 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 7 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | Enhancing Community-Based Participatory Research Through Human-Centere | 2020 | Yes |
| 2 | Radical Futures: Supporting Community-Led Design Engagements through a | 2022 | Yes |
| 3 | Design Justice: Community-Led Practices to Build the World We Need | 2020 | — |
| 4 | Restorative Justice: Pedagogy, Praxis, and Discipline | 2012 | Yes |
| 5 | Data Justice Stories: A Repository of Case Studies | 2022 | Yes |
| 6 | Setting Standards for Restorative Justice | 2002 | Yes |
| 7 | Toward a Theory of Justice for Artificial Intelligence | 2021 | Yes |
| 8 | What is Restorative Justice? Fresh Answers to a Vexed Question | 2015 | — |
| 9 | Restorative Justice and Gendered Violence: Diversion or Effective Just | 2002 | Yes |
| 10 | The Psychological Impact of Restorative Justice Practices on Victims o | 2022 | — |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Data Justice Stories: A Repository of Case Studies' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Data Justice Stories: A Repository of Case Studies + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H02** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Toward a Theory of Justice for Artificial Intelligence' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Toward a Theory of Justice for Artificial Intelligence + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H03** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Restorative Justice: Pedagogy, Praxis, and Discipline' will unlock currently blocked progress toward: Neuroscience
- **Grounded in:** entropy gap node: Restorative Justice: Pedagogy, Praxis, and Discipline + included in golden token recommended path
- **Novel because:** absent from 'Restorative Justice & Responsive Regulation' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Community-Based Trauma-Informed Care Following Immigrant Family Reu...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Community-Based Trauma-Informed Care Following Immigrant ...
- **Novel because:** not yet connected to 'The great reconnection: Restorative justice as remedy for fr' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Sita's Trousseau: restorative justice, domestic violence, and South...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Sita's Trousseau: restorative justice, domestic violence,...
- **Novel because:** not yet connected to 'Sexual and Reproductive Healthcare Needs of Refugee Women Ex' despite logical dependency in prerequisite chain
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
| 6 | Untitled | 2 |
| 7 | Untitled | 3 |
| 8 | Untitled | 2 |
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