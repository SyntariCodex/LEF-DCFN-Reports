# DCFN Technical Report: quantum physics × dream psychology

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 05, 2026
**Sources:** 231

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | quantum physics × dream psychology |
| Sources Analyzed | 231 |
| Graph Nodes | 243 |
| Graph Edges | 2054 |
| Knowledge Gaps (total) | 231 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 3 |
| Convergence Events | 2 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 20 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 231

**Source APIs:**

| API | Status |
|-----|--------|
| Semantic Scholar | Primary |
| arXiv | Supplementary |
| PubMed | Supplementary |
| OpenAlex | Supplementary |
| GitHub | Supplementary |
| Local Files | If configured |

**Deduplication:** Title-based fuzzy matching (SequenceMatcher ≥ 0.85) across all sources. Sources lacking abstracts excluded.

**Epistemic Grounding Distribution:**

| Status | Count |
|--------|-------|
| Well-grounded (≥0.7) | 104 |
| Partially grounded (0.4–0.7) | 127 |
| Weakly grounded (0.2–0.4) | 0 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.741** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2806 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.2322 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.4872 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2806 × Stability + 0.2322 × Concentration + 0.4872 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.3732341873739663 (30th percentile) |
| HIGH threshold | ≥ 0.5055680837585907 (80th percentile) |
| Concentration p25/p50/p75 | 0.4179571121931076 / 0.43390029668807983 / 0.4496483951807022 |
| Distinctiveness p25/p50/p75 | 0.4085632860660553 / 0.5336964726448059 / 0.6651456654071808 |
| Stability p25/p50/p75 | 0.19271531646329637 / 0.20627714358606894 / 0.22174262477721352 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 243 |
|   — CONCEPT | 12 |
|   — DOCUMENT | 231 |
| Total Edges | 2054 |
|   — MIRRORS | 1439 |
|   — CONTAINS | 297 |
|   — EXTENDS | 205 |
|   — BRIDGES | 96 |
|   — ENABLES | 15 |
|   — DEPENDS_ON | 2 |
| Density | 0.034928 |
| Connected Components | 11 |

### 4.2 Cross-Domain Topology

| Metric | Value |
|--------|-------|
| Domains | dream psychology, quantum physics |
| Cross-domain edges | 335 |
| Bridge nodes | 148 |

### 4.3 Edge Construction Rules

| Edge Type | Rule |
|-----------|------|
| ENABLES | older → newer via citation (ref list) |
| DEPENDS_ON | newer → older via citation |
| EXTENDS | cosine sim > 0.85 |
| MIRRORS | cosine 0.5–0.85, different fields |
| BRIDGES | cross-domain semantic connection |
| CONTAINS | source → field of study |

**Temporal decay:** confidence(t) = max(0.55, initial × exp(−0.12 × t)), t in months

## 5. CTE Traversal Results

### 5.1 Backward Traversal

**Chains analyzed:** 5

| Source | Chain Depth | Total Drift | Forgotten Ancestors |
|--------|------------|-------------|--------------------|
| The Dream of God: How Do Religion and Science See  | 2 | 0.44 | 2 |
| Physics | 1 | 0.00 | 0 |
| Jungian theory of dreaming and contemporary dream  | 1 | 0.00 | 1 |
| On not being able to dream. | 1 | 0.00 | 1 |
| Evidence of an active role of dreaming in emotiona | 1 | 0.00 | 1 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| What is quantum biology? | 0 | 0 | 0 | 0 |
| Dreaming Is Not a Bug: A Jung-Inspired Dream  | 0 | 0 | 0 | 0 |
| A large corpus of lucid and non-lucid dream r | 0 | 0 | 0 | 0 |
| A computational account of dreaming: learning | 0 | 0 | 0 | 0 |
| The Psychological Science of Artificial Intel | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 231
**Critical (≥7):** 0 | **High (5-6):** 159 | **Low (<5):** 72

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 231 |
| STALE | 224 |
| ORPHAN | 10 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Review of Alyssa Ney’s The World in the Wave  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Towards a better understanding of conceptual  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Quantum Computing in the NISQ era and beyond | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Quantum physics in space | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Testing the foundation of quantum physics in  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Essay: Quantum Sensing with Atomic, Molecular | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Quantum Physics Education Research over the L | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Investigating teachers’ and students’ experie | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | Quantum Physics Literacy Aimed at K12 and the | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Effect of an introductory quantum physics cou | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Predicting research trends with semantic and  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | A new teaching concept on quantum physics in  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | The relevance of learning quantum physics fro | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Quantum Simulation for High-Energy Physics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Quantum machine learning: from physics to sof | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Quantum sensing for particle physics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Quantum computing with Qiskit | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Quantum Computation and Quantum Information | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Standard model physics and the digital quantu | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Certified randomness in quantum physics | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 3 total (0 emerging, 3 established)
**Structural mirrors:** 2

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The Hero with a Thousand Faces | 131 | Established | 2009.4 |
| Quantum Computation and Quantum Information | 100 | Established | 2012.9 |
| Recent Advances on Graphene Quantum Dots: From Che | 2 | Established | 2019.0 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The Hero with a Thousand Faces | Quantum Computation and Quantum Inf | 0.76 |
| Quantum Computation and Quantum Inf | Recent Advances on Graphene Quantum | 0.68 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.452
**Confidence:** HIGH
**Entropy nodes resolved:** 8

**Scoring weights:**

| Factor | Weight |
|--------|--------|
| Centrality | 0.25 |
| Recency | 0.25 |
| Entropy Resolution | 0.25 |
| Strategic Alignment | 0.25 |

**Full Path:**

| Step | Source | Year | Score | Gap Node |
|------|--------|------|-------|----------|
| 1 | Quantum computing with Qiskit | 2024 | 0.540 | YES |
| 2 | Quantum Physics Literacy Aimed at K12 and the Gene | 2021 | 0.435 | YES |
| 3 | Quantum Simulation for High-Energy Physics | 2022 | 0.523 | YES |
| 4 | Quantum Computing in the NISQ era and beyond | 2018 | 0.485 | YES |
| 5 | Quantum machine learning: from physics to software | 2023 | 0.464 | YES |
| 6 | Physics | None | 0.341 | — |
| 7 | Standard model physics and the digital quantum rev | 2021 | 0.498 | YES |
| 8 | Medicine | None | 0.270 | — |
| 9 | Essay: Quantum Sensing with Atomic, Molecular, and | 2024 | 0.468 | YES |
| 10 | Quantum sensing for particle physics | 2023 | 0.428 | YES |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 19
**Frequent 2-itemsets:** 31
**Frequent 3-itemsets:** 5
**Association rules:** 16

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND (Very Recent work) | 0.191 |
| [Emerging] AND research in Physics | 0.177 |
| [Highly Cited] AND research in Physics | 0.151 |
| (Foundational work) AND research in Neuroscience | 0.151 |
| [Emerging] AND (Established work) | 0.147 |
| [Emerging] AND (Foundational work) | 0.147 |
| [Emerging] AND research in Neuroscience | 0.130 |
| (Foundational work) AND research in Physics | 0.126 |
| [Emerging] AND research in Computer Science | 0.121 |
| [Highly Cited] AND (Foundational work) | 0.117 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| impact:moderately_cited + temp | topic:neuroscience | 0.052 | 1.00 | 4.20 |
| temporal:foundational + topic: | impact:highly_cited | 0.078 | 0.62 | 3.05 |
| impact:emerging + topic:comput | temporal:very_recent | 0.082 | 0.68 | 3.01 |
| impact:moderately_cited + topi | temporal:foundational | 0.052 | 1.00 | 3.00 |
| topic:medicine | temporal:recent | 0.052 | 0.63 | 2.81 |
| topic:mathematics | temporal:foundational | 0.087 | 0.67 | 2.00 |
| impact:highly_cited | topic:physics | 0.151 | 0.74 | 1.95 |
| topic:neuroscience | temporal:foundational | 0.151 | 0.64 | 1.91 |
| impact:highly_cited + temporal | topic:physics | 0.078 | 0.67 | 1.75 |
| temporal:very_recent + topic:c | impact:emerging | 0.082 | 0.95 | 1.61 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 815
**High-tier pairs:** 6
**Convergence events:** 2

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.124 | 134 | 92y | 134 |
| svw_002 | 0.119 | 12 | 25y | 12 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Review of Alyssa Ney’s The World in the Wave Function: A Metaphysic...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Review of Alyssa Ney’s The World in the Wave Function: A ...
- **Novel because:** absent from 'Quantum Computation and Quantum Information' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)
- **Gap node:** `6eb7c4d58cb7d5015d88c7f43edd0fdc97cc7bd4` (severity: 6)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Towards a better understanding of conceptual difficulties in introd...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Towards a better understanding of conceptual difficulties...
- **Novel because:** not yet connected to 'Investigating teachers’ and students’ experiences of quantum' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)
- **Gap node:** `a4003705047ec8fd62539e78f2efb996abb098c4` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Quantum Computing in the NISQ era and beyond' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Quantum Computing in the NISQ era and beyond + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)
- **Gap node:** `f3d594544126e202dbd81c186ca3ce448af5255c` (severity: 6)
- **On golden path:** Yes

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Quantum physics in space' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Quantum physics in space
- **Novel because:** not yet connected to 'Physics' despite logical dependency in prerequisite chain
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)
- **Gap node:** `11688e8e905aec52905d0f0305594acbe4adb24f` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Testing the foundation of quantum physics in space via Interferomet...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Testing the foundation of quantum physics in space via In...
- **Novel because:** absent from 'Quantum Computation and Quantum Information' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** mixed-methods approach (apriori patterns unavailable)
- **Gap node:** `90ab8b277f8b886a56191632957d576391e9fd8e` (severity: 6)
- **On golden path:** No


## 8. Limitations

1. **QEB encoding**: When using TF-IDF + SVD fallback, semantic nuance may be lost for polysemous terms and domain-specific jargon. Sentence-BERT (all-MiniLM-L6-v2) mitigates this but is limited to 384-dimensional embeddings.

2. **Source coverage**: The Semantic Scholar API provides a subset of published research. Important works outside this index, preprints on non-indexed platforms, and unpublished research are not captured.

3. **Temporal decay calibration**: Parameters (λ=0.12, floor=0.55) are calibrated for general academic literature. Domains with different publication rhythms (e.g., fast-moving ML vs. slow clinical trials) may need domain-specific calibration.

4. **Greedy pathfinding**: The golden token algorithm uses greedy selection at each step. This does not guarantee globally optimal trajectories. Future work: backtracking or beam search.

5. **Abstract-only synthesis**: Gap-bridging proposals are synthesized from abstract text only. Full-text access would enable deeper, more specific synthesis.

6. **Citation completeness**: Citation edges depend on reference list coverage in the Semantic Scholar graph. Missing citations can create false ORPHAN detections.

7. **CONTRADICTS edges**: Cosine similarity (whether from TF-IDF or Sentence-BERT) cannot detect semantic contradiction directly. CONTRADICTS edges are inferred from structural patterns, not content analysis.

## 9. Reproducibility

### 9.1 Engine Configuration

| Parameter | Value |
|-----------|-------|
| Engine version | 0.3.0-prototype |
| Total sources | 231 |
| Timestamp | 2026-04-05T00:07:39.323684 |
| Embedding backend | tfidf |
| Embedding dim | 256 |
| Perturbation σ | 0.1 |
| Temporal decay λ | 0.12 |
| Temporal decay floor | 0.55 |
| Backward max depth | 20 |
| Forward max depth | 15 |
| Forward confidence floor | 0.1 |
| Concept drift threshold | 0.4 |
| Forgotten ancestor days | 60 |
| Staleness threshold days | 30 |
| Min cluster size | 2 |
| Structural mirror threshold | 0.4 |
| Apriori min support | 0.05 |
| Apriori min confidence | 0.60 |
| SVW similarity threshold | 0.40 |
| Golden token path min/max | 3–10 |

### 9.2 Patent References

- QECO: Three-Signal Adaptive Confidence (Module 1)
- QECO: Epistemic Grounding Score (Module 1b)
- QECO: Co-Occurrence Pattern Discovery (Module 2, Apriori)
- CTE: All 5 Operations
- CTE: Domain-Tagged Concept Graph + Temporal Decay
- SVW: Synchronicity Weaver
- Generation: Hypothesis Production
- Cross-Domain Bridge Detection

### 9.3 How to Replicate

1. Install dependencies: `pip install -r requirements.txt`
2. Set API keys: `SEMANTIC_SCHOLAR_API_KEY`, `ANTHROPIC_API_KEY` (optional, for auto-builder)
3. Run: `python main.py <domain_key>` for single-domain, or `python main.py <domain1> <domain2> --unified` for cross-domain
4. Reports output to `data/<domain_key>/`

*DCFN is built on patented technology by Living Eden Frameworks LLC: CTE Patent 64/002,205, QECO Patent 63/993,979, LPA Patent 64/023,988.*