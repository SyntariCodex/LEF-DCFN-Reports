# DCFN Technical Report: quantum physics × dream psychology

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 42

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | quantum physics × dream psychology |
| Sources Analyzed | 42 |
| Graph Nodes | 47 |
| Graph Edges | 96 |
| Knowledge Gaps (total) | 42 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 3 |
| Convergence Events | 1 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 42

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
| Well-grounded (≥0.7) | 40 |
| Partially grounded (0.4–0.7) | 2 |
| Weakly grounded (0.2–0.4) | 0 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.842** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.3218 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.2789 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.3993 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.3218 × Stability + 0.2789 × Concentration + 0.3993 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.3048810541482832 (30th percentile) |
| HIGH threshold | ≥ 0.40537113328721397 (80th percentile) |
| Concentration p25/p50/p75 | 0.4269399642944336 / 0.4369931221008301 / 0.4507129043340683 |
| Distinctiveness p25/p50/p75 | 0.2811817526817322 / 0.3358965814113617 / 0.5059857666492462 |
| Stability p25/p50/p75 | 0.19355609870629076 / 0.207458536121718 / 0.21925117377269943 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 47 |
|   — CONCEPT | 5 |
|   — DOCUMENT | 42 |
| Total Edges | 96 |
|   — CONTAINS | 49 |
|   — MIRRORS | 24 |
|   — EXTENDS | 17 |
|   — ENABLES | 6 |
| Density | 0.044403 |
| Connected Components | 14 |

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
| Medicine | 1 | 0.00 | 0 |
| Psychology | 1 | 0.00 | 0 |
| The Museum as 'Dream Space': Psychology and Aesthe | 1 | 0.00 | 1 |
| Lockdown dreams: Dream content and emotions during | 1 | 0.00 | 1 |
| Evidence of an active role of dreaming in emotiona | 1 | 0.00 | 1 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| Do Tourists Dream of Urban Air Mobility? Psyc | 0 | 0 | 0 | 0 |
| Evidence of an active role of dreaming in emo | 0 | 0 | 0 | 0 |
| Psychology of dreams: justification and devel | 0 | 0 | 0 | 0 |
| Integrating the Complementary Therapies of En | 0 | 0 | 0 | 0 |
| Collectively Dreaming Toward Indigenized Scho | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 42
**Critical (≥7):** 0 | **High (5-6):** 14 | **Low (<5):** 28

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 42 |
| STALE | 41 |
| ORPHAN | 12 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Pandemic Dreams: Network Analysis of Dream Co | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Dreaming during the Covid-19 pandemic: Comput | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Lockdown dreams: Dream content and emotions d | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | The Museum as 'Dream Space': Psychology and A | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Testing the Empathy Theory of Dreaming: The R | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Dreaming during the Covid-19 pandemic: Comput | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Freud's Dream Interpretation: A Different Per | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Book Review: Dreams: Understanding Biology, P | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | EEG oscillations during sleep and dream recal | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Comparing personal insight gains due to consi | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Evidence of an active role of dreaming in emo | 5/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | My Dream, My Rules: Can Lucid Dreaming Treat  | 5/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Jungian theory of dreaming and contemporary d | 5/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | A Novel Approach to Dream Content Analysis Re | 5/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Do Tourists Dream of Urban Air Mobility? Psyc | 4/9 | STALE, ORPHAN, DECAYED | — | 0 | 0 |
| 16 | Integrating the Complementary Therapies of En | 4/9 | STALE, ORPHAN, DECAYED | — | 0 | 0 |
| 17 | Psychology of Dream by Ibn Sirin’s Perspectiv | 4/9 | STALE, ORPHAN, DECAYED | — | 0 | 0 |
| 18 | Beyond a Dream: The Practical Foundations of  | 4/9 | STALE, ORPHAN, DECAYED | — | 0 | 0 |
| 19 | Psychology of dreams: justification and devel | 4/9 | STALE, ORPHAN, DECAYED | — | 0 | 0 |
| 20 | Comparing dream to reality: an assessment of  | 4/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 3 total (0 emerging, 3 established)
**Structural mirrors:** 3

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Pandemic Dreams: Network Analysis of Dream Content | 31 | Established | 2019.0 |
| Comparing dream to reality: an assessment of adher | 2 | Established | 2020.0 |
| Let us dream of positive pedagogy! | 2 | Established | 2019.0 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Pandemic Dreams: Network Analysis o | Comparing dream to reality: an asse | 0.80 |
| Pandemic Dreams: Network Analysis o | Let us dream of positive pedagogy! | 0.85 |
| Comparing dream to reality: an asse | Let us dream of positive pedagogy! | 0.71 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.203
**Confidence:** HIGH
**Entropy nodes resolved:** 9

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
| 1 | Lockdown dreams: Dream content and emotions during | 2021 | 0.447 | YES |
| 2 | Pandemic Dreams: Network Analysis of Dream Content | 2020 | 0.446 | YES |
| 3 | Dreaming during the Covid-19 pandemic: Computation | 2020 | 0.443 | YES |
| 4 | Testing the Empathy Theory of Dreaming: The Relati | 2019 | 0.414 | YES |
| 5 | Dreaming during the Covid-19 pandemic: Computation | 2020 | 0.413 | YES |
| 6 | Medicine | None | 0.401 | — |
| 7 | Evidence of an active role of dreaming in emotiona | 2024 | 0.442 | YES |
| 8 | Book Review: Dreams: Understanding Biology, Psycho | 2020 | 0.409 | YES |
| 9 | Freud's Dream Interpretation: A Different Perspect | 2018 | 0.396 | YES |
| 10 | Jungian theory of dreaming and contemporary dream  | 2020 | 0.392 | YES |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 15
**Frequent 2-itemsets:** 39
**Frequent 3-itemsets:** 26
**Association rules:** 64

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| research in Medicine AND research in Psychology | 0.452 |
| [Moderately Cited] AND research in Medicine | 0.333 |
| [Moderately Cited] AND research in Psychology | 0.309 |
| (Established work) AND research in Psychology | 0.286 |
| (Recent work) AND research in Medicine | 0.262 |
| (Established work) AND research in Medicine | 0.262 |
| (Recent work) AND research in Psychology | 0.238 |
| [Moderately Cited] AND (Established work) | 0.238 |
| [Emerging] AND (Recent work) | 0.167 |
| [Cited] AND research in Medicine | 0.167 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| population:children | method:qualitative | 0.071 | 1.00 | 6.00 |
| method:survey + temporal:estab | impact:moderately_cited | 0.071 | 1.00 | 2.80 |
| method:longitudinal + topic:me | temporal:established | 0.071 | 1.00 | 2.62 |
| method:longitudinal + topic:ps | temporal:established | 0.071 | 1.00 | 2.62 |
| population:clinical + temporal | impact:emerging | 0.071 | 0.75 | 2.42 |
| impact:emerging + population:c | temporal:recent | 0.071 | 1.00 | 2.33 |
| temporal:established + topic:m | impact:moderately_cited | 0.214 | 0.82 | 2.29 |
| temporal:established + topic:p | impact:moderately_cited | 0.214 | 0.75 | 2.10 |
| method:longitudinal | temporal:established | 0.071 | 0.75 | 1.97 |
| impact:moderately_cited + meth | temporal:established | 0.071 | 0.75 | 1.97 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 83
**High-tier pairs:** 0
**Convergence events:** 1

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.203 | 26 | 13y | 26 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Pandemic Dreams: Network Analysis of Dream Content During the COVID...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Pandemic Dreams: Network Analysis of Dream Content During... + included in golden token recommended path
- **Novel because:** absent from 'Pandemic Dreams: Network Analysis of Dream Cont...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** qualitative (co-occurs with similar gaps at 100% confidence in apriori patterns)
- **Gap node:** `806b6e0358701fdaab0c1ad798759396249da04e` (severity: 6)
- **On golden path:** Yes

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Dreaming during the Covid-19 pandemic: Computational assessment of ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Dreaming during the Covid-19 pandemic: Computational asse... + included in golden token recommended path
- **Novel because:** absent from 'Pandemic Dreams: Network Analysis of Dream Cont...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** qualitative (co-occurs with similar gaps at 100% confidence in apriori patterns)
- **Gap node:** `48269ba2f62e2bcb676445f3228d1b9cab82c8af` (severity: 6)
- **On golden path:** Yes

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Lockdown dreams: Dream content and emotions during the COVID-19 pan...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Lockdown dreams: Dream content and emotions during the CO... + included in golden token recommended path
- **Novel because:** absent from 'Pandemic Dreams: Network Analysis of Dream Cont...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** qualitative (co-occurs with similar gaps at 100% confidence in apriori patterns)
- **Gap node:** `04b5a26db92f03e5b415e49bdfdb0b1695899515` (severity: 6)
- **On golden path:** Yes

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'The Museum as 'Dream Space': Psychology and Aesthetic Response in G...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: The Museum as 'Dream Space': Psychology and Aesthetic Res...
- **Novel because:** absent from 'Pandemic Dreams: Network Analysis of Dream Cont...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** qualitative (co-occurs with similar gaps at 100% confidence in apriori patterns)
- **Gap node:** `12de5a83590535d9c9261d793b4f2b7a99fba4e6` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Testing the Empathy Theory of Dreaming: The Relationships Between D...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Testing the Empathy Theory of Dreaming: The Relationships... + included in golden token recommended path
- **Novel because:** absent from 'Pandemic Dreams: Network Analysis of Dream Cont...' — no existing paper bridges this gap to adjacent clusters
- **Suggested method:** qualitative (co-occurs with similar gaps at 100% confidence in apriori patterns)
- **Gap node:** `608560bb5c8865cbbea7456affa78da001cf5bc1` (severity: 6)
- **On golden path:** Yes


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
| Total sources | 42 |
| Timestamp | 2026-04-04T22:25:04.613353 |
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