# DCFN Technical Report: Trauma-informed care × restorative justice × community design (Layer 2)

**Proof of Receipt — DCFN Engine Run**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 11, 2026
**Run fingerprint:** `6bc488003efc31de`
**Corpus fingerprint:** `no-corpus`
**Sources:** 581

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
| Run timestamp | `2026-04-11T06:00:14.496054` |
| Run fingerprint | `6bc488003efc31de` |
| Corpus fingerprint | `no-corpus` |
| Domain | Trauma-informed care × restorative justice × community design (Layer 2) |

### 1.2 Corpus

| Field | Value |
|-------|-------|
| Sources analyzed | 581 |

### 1.3 Stage Execution Counts

*Each row is a count of work the stage actually performed. These are not findings — they are evidence the stage ran.*

| Stage | Work performed |
|-------|----------------|
| QEB encoding | 581 sources encoded |
| Concept graph | 616 nodes / 7580 edges constructed |
| CTE backward traversal | 5 chains (sum of chain depths: 7) |
| CTE forward cascade | 5 cascades (0 implications, 0 blocked paths) |
| CTE entropy detection | 555 entropy nodes inspected (293 critical, 129 high) |
| CTE branch cataloging | 10 clusters identified (26 structural mirrors) |
| CTE golden-token pathfinding | path length 10 (6 entropy nodes resolved) |
| Apriori pattern mining | 21 1-itemsets, 31 2-itemsets, 6 3-itemsets, 5 rules |
| SVW synchronicity | 2688 candidate pairs scanned, 4 convergence events, 284 convergence anchors |
| Hypothesis generation | 5 hypotheses produced |
| Bridge detection | 20 cross-domain bridge nodes |

### 1.4 Wall-Clock Timings

*Per-stage execution time on the run host. Useful for verifying the pipeline did not short-circuit any stage.*

| Stage | Duration |
|-------|----------|
| qeb_encoding | 2m 34.6s |
| concept_graph | 778 ms |
| cte_traversal | 968 ms |
| apriori | 101 ms |
| svw | 404 ms |
| hypothesis_generation | 0 ms |
| post_traversal_calibration | 1.14 s |
| bridge_detection | 11 ms |
| contradiction_resolution | 14.32 s |
| **Total measured** | **2m 52.3s** |

## Band 2 — What It Produced

*Results only. Counts, classifications, titles, ranks. Internal calibration that produced these results is documented at the component level in Band 3 — never numerically.*

### 2.1 Graph

| Metric | Value |
|--------|-------|
| Total nodes | 616 |
| Total edges | 7580 |
| Connected components | 16 |

**Node types:**

| Type | Count |
|------|-------|
| DOCUMENT | 581 |
| ENTITY | 21 |
| CONCEPT | 14 |

**Edge types:**

| Type | Count |
|------|-------|
| MIRRORS | 3569 |
| EXTENDS | 1865 |
| BRIDGES | 1396 |
| CONTAINS | 632 |
| ENABLES | 61 |
| DEFENDED_BY | 48 |
| DEPENDS_ON | 9 |

### 2.2 Cross-Domain Topology

| Field | Value |
|-------|-------|
| Domains | Trauma-informed care × restorative justice × community design (Layer 2), gap: Advancing Data Justice Research and Prac, gap: Community-Based Trauma-Informed Care Fol, gap: Data Justice Stories: A Repository of Ca, gap: Restorative Justice: Pedagogy, Praxis, a, gap: Restorative justice, gap: Setting Standards for Restorative Justic, gap: Sita's Trousseau: restorative justice, d, gap: Toward a Theory of Justice for Artificia |
| Cross-domain edges | 2283 |
| Bridge nodes | 465 |

### 2.3 Entropy Nodes

**Total:** 555 (critical: 293, high: 129, low: 133)

**Surfaced gaps (classification only):**

| # | Title | Bridge confidence |
|---|-------|-------------------|
| 1 | Evidence and guidelines for trauma-informed doula care. | — |
| 2 | Toward a Theory of Justice for Artificial Intelligence | — |
| 3 | Community-Based Trauma-Informed Care Following Immigrant Family Reunification: A | — |
| 4 | Community-based Trauma-informed Care following Immigrant Family Reunification: A | — |
| 5 | Data Justice Stories: A Repository of Case Studies | — |
| 6 | Restorative Justice and Gendered Violence: Diversion or Effective Justice? | — |
| 7 | Restorative Justice and De-Professionalization | — |
| 8 | Smart growth community design and physical activity in children. | — |
| 9 | Healthy Aging and Where You Live: Community Design Relationships With Physical A | — |
| 10 | Community Design for Physical Activity | — |
| 11 | Building Successful Online Communities: Evidence-Based Social Design | — |
| 12 | Legitimacy and Criminal Justice: The Benefits of Self-Regulation | — |
| 13 | What are effective strategies for implementing trauma-informed care in youth inp | — |
| 14 | Restorative Justice: Pedagogy, Praxis, and Discipline | — |
| 15 | Radical Futures: Supporting Community-Led Design Engagements through an Afrofutu | — |
| 16 | Enhancing Community-Based Participatory Research Through Human-Centered Design S | — |
| 17 | The Fallacy of AI Functionality | — |
| 18 | The Impact of COVID-19 on Family Violence in Immigrant Communities in the United | — |
| 19 | Trauma-informed care: recognizing and resisting re-traumatization in health care | — |
| 20 | Trauma-informed Care Interventions in Emergency Medicine: A Systematic Review | — |

### 2.4 Branch Clusters

**Total clusters:** 10 (emerging: 0, established: 10)
**Structural mirrors:** 26

**Cluster representatives:**

| Cluster | Size | Status |
|---------|------|--------|
| Trauma Providers' Knowledge, Views, and Practice of Trauma-Informed Care | 189 | Established |
| How Does Restorative Justice Work? A Qualitative Metasynthesis | 197 | Established |
| Audience-specific online community design | 172 | Established |
| AI-Enhanced Intensive Care Unit: Revolutionizing Patient Care with Pervasive Sen | 4 | Established |
| Automatic Classification of User Requirements from Online Feedback -- A Replicat | 5 | Established |
| Virtual Community: An Open World for Humans, Robots, and Society | 8 | Established |
| How Weyl stumbled across electricity while pursuing mathematical justice | 21 | Established |
| Creating Walkable Communities: Understanding Trade-Offs. | 2 | Established |
| How national context, project design, and local community characteristics influe | 2 | Established |
| Processes of developing 'community livability' in older age. | 3 | Established |

### 2.5 Convergence Detection

| Field | Value |
|-------|-------|
| Convergence events | 4 |
| Convergence anchors | 284 |

**Top anchors (rank only):**

| Rank | Anchor | Year | Independent groups |
|------|--------|------|--------------------|
| 1 | Smart growth community design and physical activity in child | 2013 | 24 |
| 2 | Trauma-informed care education for midwives: Does education  | 2024 | 17 |
| 3 | Supporting Active Living Through Community Plans: The Associ | 2019 | 26 |
| 4 | Meta-analyses of teacher-delivered trauma-based and trauma-i | 2023 | 18 |
| 5 | How Healthcare Providers Reconcile Bad Things Happening to G | 2023 | 16 |
| 6 | Health and community design: the impact of the built environ | 2004 | 21 |
| 7 | Trauma-Informed Care Addressing the Mental and Emotional Nee | 2024 | 16 |
| 8 | Community Lenses Revealing the Role of Sociocultural Environ | 2016 | 24 |
| 9 | The Impact of Community Design and Land-Use Choices on Publi | 2003 | 21 |
| 10 | Physical Activity–Friendly Policies and Community Design Fea | 2023 | 20 |

### 2.6 Golden Trajectory

| Field | Value |
|-------|-------|
| Path length | 10 |
| Confidence class | HIGH |
| Entropy nodes resolved | 6 |

**Trajectory steps (titles only):**

| Step | Title | Year | Resolves gap |
|------|-------|------|--------------|
| 1 | The Fallacy of AI Functionality | 2022 | Yes |
| 2 | Toward a Theory of Justice for Artificial Intelligence | 2021 | Yes |
| 3 | Connecting the dots in trustworthy Artificial Intelligence: From AI pr | 2023 | — |
| 4 | Operationalizing Justice: Towards the Development of a Principle Based | 2025 | — |
| 5 | Restorative Justice: Pedagogy, Praxis, and Discipline | 2012 | Yes |
| 6 | Data Justice Stories: A Repository of Case Studies | 2022 | Yes |
| 7 | Re-Thinking Data Strategy and Integration for Artificial Intelligence: | 2023 | — |
| 8 | Social Data: Biases, Methodological Pitfalls, and Ethical Boundaries | 2019 | — |
| 9 | Building Successful Online Communities: Evidence-Based Social Design | 2012 | Yes |
| 10 | Enhancing Community-Based Participatory Research Through Human-Centere | 2020 | Yes |

### 2.7 Generated Hypotheses

**Total:** 5

**H01** [MEDIUM]
- **Hypothesis:** Resolving the research gap in 'Evidence and guidelines for trauma-informed doula care.' will unlock currently blocked progress toward: Trauma care disparities: is equity the key? Output from SAFE
- **Grounded in:** entropy gap node: Evidence and guidelines for trauma-informed doula care.
- **Novel because:** not yet connected to 'Trauma care disparities: is equity the key? Output from SAFE' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H02** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Toward a Theory of Justice for Artificial Intelligence' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Toward a Theory of Justice for Artificial Intelligence + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Community-Based Trauma-Informed Care Following Immigrant Family Reu...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Community-Based Trauma-Informed Care Following Immigrant ...
- **Novel because:** not yet connected to 'The Impact of COVID-19 on Family Violence in Immigrant Commu' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Community-based Trauma-informed Care following Immigrant Family Reu...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Community-based Trauma-informed Care following Immigrant ...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)

**H05** [HIGH]
- **Hypothesis:** Resolving the research gap in 'Data Justice Stories: A Repository of Case Studies' will unlock currently blocked progress toward: Computer Science
- **Grounded in:** entropy gap node: Data Justice Stories: A Repository of Case Studies + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)


### 2.8 Cross-Domain Bridges

**Total:** 20

| # | Title | Domains touched |
|---|-------|-----------------|
| 1 | Untitled | 6 |
| 2 | Untitled | 3 |
| 3 | Untitled | 4 |
| 4 | Untitled | 5 |
| 5 | Untitled | 3 |
| 6 | Untitled | 4 |
| 7 | Untitled | 3 |
| 8 | Untitled | 3 |
| 9 | Untitled | 6 |
| 10 | Untitled | 3 |

### 2.9 Contradiction Target Resolution (Go Deeper)

| Field | Value |
|-------|-------|
| Papers with C-lite markers | 6 |
| Papers with resolved targets | 0 |
| CONTRADICTS edges created | 0 |

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