# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 05, 2026
**Sources:** 2257

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 2257 |
| Graph Nodes | 2274 |
| Graph Edges | 85395 |
| Knowledge Gaps (total) | 2247 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 10 |
| Convergence Events | 2 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 2257

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
| Well-grounded (≥0.7) | 1138 |
| Partially grounded (0.4–0.7) | 1049 |
| Weakly grounded (0.2–0.4) | 70 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.752** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2796 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.1917 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.5287 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2796 × Stability + 0.1917 × Concentration + 0.5287 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.38796792350276277 (30th percentile) |
| HIGH threshold | ≥ 0.5221141938180571 (80th percentile) |
| Concentration p25/p50/p75 | 0.4237124025821686 / 0.43808847665786743 / 0.4525608420372009 |
| Distinctiveness p25/p50/p75 | 0.4404500722885132 / 0.5570766925811768 / 0.6966648697853088 |
| Stability p25/p50/p75 | 0.19346359327299947 / 0.2068400414539112 / 0.22041247153713864 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 2274 |
|   — CONCEPT | 17 |
|   — DOCUMENT | 2257 |
| Total Edges | 85395 |
|   — MIRRORS | 77420 |
|   — EXTENDS | 4249 |
|   — CONTAINS | 3064 |
|   — ENABLES | 600 |
|   — DEPENDS_ON | 62 |
| Density | 0.016521 |
| Connected Components | 237 |

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
| Investigating student exposure to competency-based | 1 | 0.00 | 1 |
| Competency-based Education 101☆ | 1 | 0.00 | 1 |
| Learning analytics: state of the art | 1 | 0.00 | 1 |
| Self-Regulated Learning Model in Educational Data  | 1 | 0.00 | 1 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| Stratified Causal Inference for Intensive Car | 0 | 0 | 0 | 0 |
| BamaER: A Behavior-Aware Memory-Augmented Mod | 0 | 0 | 0 | 0 |
| A Survey on the Classification Techniques In  | 0 | 0 | 0 | 0 |
| From neurotechnology to the classroom: the pr | 0 | 0 | 0 | 0 |
| Measuring Implementation of Multi-Tiered Syst | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 2247
**Critical (≥7):** 0 | **High (5-6):** 1746 | **Low (<5):** 501

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 2247 |
| STALE | 2179 |
| ORPHAN | 233 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Artificial intelligence to deep learning: mac | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Molecular Docking: Shifting Paradigms in Drug | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Statistical Methods for Detecting Differentia | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Adaptive Federated Learning in Resource Const | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Deep Knowledge Tracing | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Adaptive Learning Using Artificial Intelligen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Accelerated discovery of stable lead-free hyb | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | The current landscape of learning analytics i | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Educational data mining: prediction of studen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | A Systematic Review on Educational Data Minin | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Learning Analytics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Artificial intelligence in cancer target iden | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Utilising learning analytics to support study | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Artificial intelligence in drug discovery: re | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Impact of word embedding models on text analy | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | A Comparison of Undersampling, Oversampling,  | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 10 total (8 emerging, 2 established)
**Structural mirrors:** 22

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The PRISMA 2020 statement: an updated guideline fo | 1938 | Established | 2018.2 |
| Beyond Language Barriers: Allowing Multiple Langua | 2 | Emerging | 2023.5 |
| Implementing Diagnostic Assessment in Designing Di | 2 | Emerging | 2023.5 |
| Utilizing Cognitive Diagnostic Assessments to Iden | 2 | Emerging | 2024.0 |
| A REVIEW ON INTELLIGENT TUTORING SYSTEMS: Enhancin | 2 | Emerging | 2025.0 |
| Learning Strategy Based on Deep Knowledge Tracing | 2 | Emerging | 2023.0 |
| Inter-Variability Study of COVLIAS 1.0: Hybrid Dee | 3 | Established | 2021.3 |
| On the influence of social norms on individual ach | 2 | Emerging | 2024.0 |
| Relationships Between First-Year Student Resilienc | 2 | Emerging | 2024.0 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 86 | Emerging | 2024.3 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.95 |
| Implementing Diagnostic Assessment  | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Implementing Diagnostic Assessment  | A REVIEW ON INTELLIGENT TUTORING SY | 1.00 |
| Implementing Diagnostic Assessment  | Learning Strategy Based on Deep Kno | 1.00 |
| Implementing Diagnostic Assessment  | Inter-Variability Study of COVLIAS  | 1.00 |
| Implementing Diagnostic Assessment  | On the influence of social norms on | 1.00 |
| Implementing Diagnostic Assessment  | Relationships Between First-Year St | 1.00 |
| Utilizing Cognitive Diagnostic Asse | A REVIEW ON INTELLIGENT TUTORING SY | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Learning Strategy Based on Deep Kno | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Inter-Variability Study of COVLIAS  | 1.00 |
| Utilizing Cognitive Diagnostic Asse | On the influence of social norms on | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Relationships Between First-Year St | 1.00 |
| A REVIEW ON INTELLIGENT TUTORING SY | Learning Strategy Based on Deep Kno | 1.00 |
| A REVIEW ON INTELLIGENT TUTORING SY | Inter-Variability Study of COVLIAS  | 1.00 |
| A REVIEW ON INTELLIGENT TUTORING SY | On the influence of social norms on | 1.00 |
| A REVIEW ON INTELLIGENT TUTORING SY | Relationships Between First-Year St | 1.00 |
| Learning Strategy Based on Deep Kno | Inter-Variability Study of COVLIAS  | 1.00 |
| Learning Strategy Based on Deep Kno | On the influence of social norms on | 1.00 |
| Learning Strategy Based on Deep Kno | Relationships Between First-Year St | 1.00 |
| Inter-Variability Study of COVLIAS  | On the influence of social norms on | 1.00 |
| Inter-Variability Study of COVLIAS  | Relationships Between First-Year St | 1.00 |
| On the influence of social norms on | Relationships Between First-Year St | 1.00 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 5.083
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
| 1 | Predicting Student Performance Using Data Mining a | 2020 | 0.567 | YES |
| 2 | A Comparison of Undersampling, Oversampling, and S | 2023 | 0.530 | YES |
| 3 | Learning analytics dashboard: a tool for providing | 2022 | 0.381 | — |
| 4 | Utilising learning analytics to support study succ | 2020 | 0.554 | YES |
| 5 | Educational data mining: prediction of students' a | 2022 | 0.527 | YES |
| 6 | The current landscape of learning analytics in hig | 2018 | 0.492 | YES |
| 7 | Educational data mining and learning analytics for | 2019 | 0.503 | YES |
| 8 | Educational data mining and learning analytics: An | 2020 | 0.512 | YES |
| 9 | Learning Analytics | 2019 | 0.492 | YES |
| 10 | Adaptive Learning Using Artificial Intelligence in | 2023 | 0.527 | YES |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 23
**Frequent 2-itemsets:** 48
**Frequent 3-itemsets:** 7
**Association rules:** 13

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND (Very Recent work) | 0.229 |
| [Emerging] AND research in Education | 0.196 |
| (Very Recent work) AND research in Computer Science | 0.153 |
| [Highly Cited] AND research in Computer Science | 0.149 |
| [Moderately Cited] AND research in Computer Science | 0.137 |
| [Emerging] AND research in Computer Science | 0.133 |
| (Recent work) AND research in Computer Science | 0.129 |
| [Emerging] AND studying Clinical | 0.123 |
| using Machine Learning AND research in Computer Science | 0.119 |
| with Positive findings AND [Emerging] | 0.119 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| population:clinical + topic:ed | impact:emerging | 0.064 | 0.99 | 2.14 |
| topic:education | impact:emerging | 0.196 | 0.86 | 1.84 |
| population:clinical + temporal | impact:emerging | 0.055 | 0.84 | 1.81 |
| impact:emerging + method:machi | temporal:very_recent | 0.059 | 0.65 | 1.80 |
| impact:highly_cited + temporal | topic:computer science | 0.055 | 0.86 | 1.78 |
| temporal:very_recent + topic:e | impact:emerging | 0.077 | 0.82 | 1.77 |
| impact:highly_cited | topic:computer science | 0.149 | 0.75 | 1.55 |
| population:clinical | impact:emerging | 0.123 | 0.69 | 1.48 |
| finding:positive + temporal:ve | impact:emerging | 0.068 | 0.67 | 1.45 |
| temporal:very_recent | impact:emerging | 0.229 | 0.64 | 1.37 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 26586
**High-tier pairs:** 267
**Convergence events:** 2

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.147 | 1523 | 61y | 1523 |
| svw_002 | 0.097 | 3 | 6y | 3 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Artificial intelligence to deep learning: machine intelligence appr...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Artificial intelligence to deep learning: machine intelli...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 65% confidence in apriori patterns)
- **Gap node:** `29409efa04ac99ccf01d2a011d21d5d14e870000` (severity: 6)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Molecular Docking: Shifting Paradigms in Drug Discovery' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Molecular Docking: Shifting Paradigms in Drug Discovery
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 65% confidence in apriori patterns)
- **Gap node:** `8f7948d72b19b3be7191396c5e637cdb14a2371c` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Statistical Methods for Detecting Differentially Abundant Features ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Statistical Methods for Detecting Differentially Abundant...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 65% confidence in apriori patterns)
- **Gap node:** `a80ba5b7c4ea6551a6f4ab64fde15819125bd1cb` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Adaptive Federated Learning in Resource Constrained Edge Computing ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Adaptive Federated Learning in Resource Constrained Edge ...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 65% confidence in apriori patterns)
- **Gap node:** `e2e0e226f1f74ff65c0de3e5ad565bcd8b9710da` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Deep Knowledge Tracing' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Deep Knowledge Tracing
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 65% confidence in apriori patterns)
- **Gap node:** `fa98d609eb14ce25dd73cd8713a5e284948b4ff4` (severity: 6)
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
| Total sources | 2257 |
| Timestamp | 2026-04-05T02:25:27.564677 |
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