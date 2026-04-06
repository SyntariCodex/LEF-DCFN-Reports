# DCFN Technical Report: how metacognition develops in children ages 5-12

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 06, 2026
**Sources:** 131

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | how metacognition develops in children ages 5-12 |
| Sources Analyzed | 131 |
| Graph Nodes | 140 |
| Graph Edges | 464 |
| Knowledge Gaps (total) | 128 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 3 |
| Convergence Events | 4 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | MEDIUM |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 131

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
| Well-grounded (≥0.7) | 68 |
| Partially grounded (0.4–0.7) | 63 |
| Weakly grounded (0.2–0.4) | 0 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.752** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2124 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.1717 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.25 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2124 × Stability + 0.1717 × Concentration + 0.25 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.24208180677577198 (30th percentile) |
| HIGH threshold | ≥ 0.3001837156718824 (80th percentile) |
| Concentration p25/p50/p75 | 0.42401327192783356 / 0.4381464123725891 / 0.4515985995531082 |
| Distinctiveness p25/p50/p75 | 0.47505223751068115 / 0.5782251358032227 / 0.6857597231864929 |
| Stability p25/p50/p75 | 0.19188017503599608 / 0.20504728914119977 / 0.21880633912917472 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 140 |
|   — CONCEPT | 9 |
|   — DOCUMENT | 131 |
| Total Edges | 464 |
|   — MIRRORS | 262 |
|   — CONTAINS | 181 |
|   — EXTENDS | 12 |
|   — ENABLES | 6 |
|   — DEPENDS_ON | 3 |
| Density | 0.023844 |
| Connected Components | 10 |

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
| Computer Science | 1 | 0.00 | 0 |
| Neuroscience | 1 | 0.00 | 0 |
| Metacognition and emotional regulation in children | 1 | 0.00 | 1 |
| How Flexible Is the Visuospatial Reference System  | 1 | 0.00 | 1 |
| Medicine | 1 | 0.00 | 0 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| Disentangling Gut Microbiome Alterations in C | 0 | 0 | 0 | 0 |
| S11: What Makes a Whole System Approach to Im | 0 | 0 | 0 | 0 |
| Influence of Family Setting on Behavioral Pat | 0 | 0 | 0 | 0 |
| Social Robots on the Loose: Supporting Childr | 0 | 0 | 0 | 0 |
| Calling for Backup: How Children Navigate Suc | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 128
**Critical (≥7):** 0 | **High (5-6):** 64 | **Low (<5):** 64

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 114 |
| STALE | 96 |
| ORPHAN | 9 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | What do US and Canadian parents do to encoura | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | The development of the size-weight illusion i | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | How Flexible Is the Visuospatial Reference Sy | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Young Children's Spontaneous Manifestation of | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Evaluation of Functional Vision and Eye-Relat | 6.0/9 | STALE | — | 0 | 0 |
| 6 | How physically literate are children today? A | 6.0/9 | STALE | — | 0 | 0 |
| 7 | Understanding Factors that Shape Children's L | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Exploring Children's Preferences for Taking C | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | When Children Program Intelligent Environment | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Attitudes of Children with Autism towards Rob | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Investigating Mental Representations about Ro | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Phone Duration Modeling for Speaker Age Estim | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | ChildCI Framework: Analysis of Motor and Cogn | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Learning a metacognition for object perceptio | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Development of modularity in the neural activ | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Psychophysiological Arousal in Young Children | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | How Adults Understand What Young Children Say | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Stellar Seismology, Stellar Ages and the Cosm | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Self-Efficacy and Academic Motivation | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | The Science of Mind Wandering: Empirically Na | 6.0/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 3 total (1 emerging, 2 established)
**Structural mirrors:** 3

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Arash: A social robot buddy to support children wi | 19 | Emerging | 2022.8 |
| Self-Efficacy and Academic Motivation | 98 | Established | 2015.0 |
| The Fractional Quantum Hall States at $ν=13/5$ and | 14 | Established | 2009.7 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Arash: A social robot buddy to supp | Self-Efficacy and Academic Motivati | 0.80 |
| Arash: A social robot buddy to supp | The Fractional Quantum Hall States  | 0.84 |
| Self-Efficacy and Academic Motivati | The Fractional Quantum Hall States  | 0.47 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 3.814
**Confidence:** MEDIUM
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
| 1 | The Science of Mind Wandering: Empirically Navigat | 2014 | 0.442 | YES |
| 2 | Learning a metacognition for object perception | 2020 | 0.375 | YES |
| 3 | The development of the size-weight illusion in chi | 2019 | 0.393 | YES |
| 4 | ChildCI Framework: Analysis of Motor and Cognitive | 2022 | 0.402 | YES |
| 5 | How physically literate are children today? A base | 2020 | 0.389 | YES |
| 6 | Medicine | None | 0.302 | — |
| 7 | Evaluation of Functional Vision and Eye-Related Qu | 2022 | 0.392 | YES |
| 8 | How Flexible Is the Visuospatial Reference System  | 2015 | 0.364 | YES |
| 9 | How Adults Understand What Young Children Say | 2022 | 0.396 | YES |
| 10 | Computer Science | None | 0.360 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 21
**Frequent 2-itemsets:** 51
**Frequent 3-itemsets:** 40
**Association rules:** 101

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND studying Children | 0.458 |
| studying Children AND (Very Recent work) | 0.313 |
| [Emerging] AND (Very Recent work) | 0.298 |
| studying Children AND research in Computer Science | 0.275 |
| [Emerging] AND research in Computer Science | 0.275 |
| [Highly Cited] AND research in Neuroscience | 0.252 |
| [Highly Cited] AND (Foundational work) | 0.237 |
| studying Children AND research in Medicine | 0.214 |
| (Foundational work) AND research in Neuroscience | 0.214 |
| [Highly Cited] AND research in Computer Science | 0.176 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| impact:emerging + temporal:fou | topic:physics | 0.076 | 0.91 | 5.41 |
| impact:highly_cited + topic:ph | topic:neuroscience | 0.069 | 1.00 | 3.85 |
| impact:highly_cited + topic:bi | topic:neuroscience | 0.053 | 0.88 | 3.37 |
| topic:neuroscience + topic:phy | impact:highly_cited | 0.069 | 1.00 | 3.36 |
| impact:highly_cited + temporal | topic:neuroscience | 0.206 | 0.87 | 3.36 |
| impact:highly_cited | topic:neuroscience | 0.252 | 0.85 | 3.26 |
| topic:neuroscience | impact:highly_cited | 0.252 | 0.97 | 3.26 |
| temporal:foundational + topic: | impact:highly_cited | 0.206 | 0.96 | 3.24 |
| topic:computer science + topic | impact:highly_cited | 0.137 | 0.95 | 3.18 |
| temporal:foundational + topic: | topic:neuroscience | 0.115 | 0.79 | 3.04 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 144
**High-tier pairs:** 3
**Convergence events:** 4

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_003 | 0.211 | 11 | 14y | 11 |
| svw_002 | 0.204 | 9 | 7y | 9 |
| svw_001 | 0.118 | 49 | 33y | 49 |
| svw_004 | 0.059 | 5 | 32y | 5 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'What do US and Canadian parents do to encourage or discourage physi...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: What do US and Canadian parents do to encourage or discou...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)
- **Gap node:** `e6a13950c55e91f7259c928ffd64078d5976588c` (severity: 6.0)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'The development of the size-weight illusion in children coincides w...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: The development of the size-weight illusion in children c... + included in golden token recommended path
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)
- **Gap node:** `2358a14db05cb0bf2ec154645b813722e1aa8523` (severity: 6.0)
- **On golden path:** Yes

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'How Flexible Is the Visuospatial Reference System in Children Aged ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: How Flexible Is the Visuospatial Reference System in Chil... + included in golden token recommended path
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)
- **Gap node:** `c746f98ce5d016cf9cb350725c95b3671e2f73cf` (severity: 6.0)
- **On golden path:** Yes

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Young Children's Spontaneous Manifestation of Self-Regulation and M...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Young Children's Spontaneous Manifestation of Self-Regula...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)
- **Gap node:** `1b1b00b7c1eac97bce7a283546086d9848e6374d` (severity: 6.0)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Evaluation of Functional Vision and Eye-Related Quality of Life in ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Evaluation of Functional Vision and Eye-Related Quality o... + included in golden token recommended path
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** survey (co-occurs with similar gaps at 64% confidence in apriori patterns)
- **Gap node:** `a0c62152647ce8353b7b5fda238baa07f7885a2f` (severity: 6.0)
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
| Total sources | 131 |
| Timestamp | 2026-04-06T02:41:27.732405 |
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