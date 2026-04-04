# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3123

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 3123 |
| Graph Nodes | 3140 |
| Graph Edges | 122773 |
| Knowledge Gaps (total) | 3113 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 12 |
| Convergence Events | 6 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3123

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
| Well-grounded (≥0.7) | 1139 |
| Partially grounded (0.4–0.7) | 1914 |
| Weakly grounded (0.2–0.4) | 70 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.696** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.3185 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.2667 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.4149 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.3185 × Stability + 0.2667 × Concentration + 0.4149 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.3881794084334168 (30th percentile) |
| HIGH threshold | ≥ 0.4851271606633092 (80th percentile) |
| Concentration p25/p50/p75 | 0.4234214127063751 / 0.4379459619522095 / 0.4521857351064682 |
| Distinctiveness p25/p50/p75 | 0.4686654508113861 / 0.5968894362449646 / 0.7003953754901886 |
| Stability p25/p50/p75 | 0.19390821813049475 / 0.20773002305461988 / 0.22081856300759195 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3140 |
|   — CONCEPT | 17 |
|   — DOCUMENT | 3123 |
| Total Edges | 122773 |
|   — MIRRORS | 113092 |
|   — EXTENDS | 4814 |
|   — CONTAINS | 4213 |
|   — ENABLES | 599 |
|   — DEPENDS_ON | 55 |
| Density | 0.012456 |
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
| Supervised diagnostic classification of cognitive  | 1 | 0.00 | 1 |
| Learning analytics: state of the art | 1 | 0.00 | 1 |
| Competency-based Education 101☆ | 1 | 0.00 | 1 |

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

**Total entropy nodes:** 3113
**Critical (≥7):** 0 | **High (5-6):** 2439 | **Low (<5):** 674

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3113 |
| STALE | 3020 |
| ORPHAN | 233 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Artificial intelligence to deep learning: mac | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Molecular Docking: Shifting Paradigms in Drug | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Adaptive Federated Learning in Resource Const | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Deep Knowledge Tracing | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Adaptive Learning Using Artificial Intelligen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Accelerated discovery of stable lead-free hyb | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | The current landscape of learning analytics i | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | Educational data mining: prediction of studen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | A Systematic Review on Educational Data Minin | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Learning Analytics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Artificial intelligence in cancer target iden | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Utilising learning analytics to support study | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Artificial intelligence in drug discovery: re | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Impact of word embedding models on text analy | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Organizational mindfulness towards digital tr | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | A Comparison of Undersampling, Oversampling,  | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 12 total (8 emerging, 4 established)
**Structural mirrors:** 33

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The PRISMA 2020 statement: an updated guideline fo | 2778 | Established | 2018.7 |
| Beyond Language Barriers: Allowing Multiple Langua | 2 | Emerging | 2023.5 |
| Implementing Diagnostic Assessment in Designing Di | 2 | Emerging | 2023.5 |
| Utilizing Cognitive Diagnostic Assessments to Iden | 2 | Emerging | 2024.0 |
| Learning Strategy Based on Deep Knowledge Tracing | 2 | Emerging | 2023.0 |
| COVLIAS 1.0: Lung Segmentation in COVID-19 Compute | 3 | Established | 2021.3 |
| On the influence of social norms on individual ach | 2 | Emerging | 2024.0 |
| Mindful self-care and resilience in first-year und | 2 | Emerging | 2024.0 |
| Downlink and Uplink Decoupling in Two-Tier Heterog | 20 | Established | 2018.3 |
| Formal extension of noncommutative tensor-triangul | 2 | Emerging | 2023.5 |
| Discovery of the Mercury Isotopes | 4 | Established | 2012.5 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 88 | Emerging | 2024.2 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The PRISMA 2020 statement: an updat | Downlink and Uplink Decoupling in T | 0.61 |
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.94 |
| Implementing Diagnostic Assessment  | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Implementing Diagnostic Assessment  | Learning Strategy Based on Deep Kno | 1.00 |
| Implementing Diagnostic Assessment  | COVLIAS 1.0: Lung Segmentation in C | 1.00 |
| Implementing Diagnostic Assessment  | On the influence of social norms on | 1.00 |
| Implementing Diagnostic Assessment  | Mindful self-care and resilience in | 1.00 |
| Implementing Diagnostic Assessment  | Formal extension of noncommutative  | 0.45 |
| Implementing Diagnostic Assessment  | Discovery of the Mercury Isotopes | 0.45 |
| Utilizing Cognitive Diagnostic Asse | Learning Strategy Based on Deep Kno | 1.00 |
| Utilizing Cognitive Diagnostic Asse | COVLIAS 1.0: Lung Segmentation in C | 1.00 |
| Utilizing Cognitive Diagnostic Asse | On the influence of social norms on | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Mindful self-care and resilience in | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Formal extension of noncommutative  | 0.45 |
| Utilizing Cognitive Diagnostic Asse | Discovery of the Mercury Isotopes | 0.45 |
| Learning Strategy Based on Deep Kno | COVLIAS 1.0: Lung Segmentation in C | 1.00 |
| Learning Strategy Based on Deep Kno | On the influence of social norms on | 1.00 |
| Learning Strategy Based on Deep Kno | Mindful self-care and resilience in | 1.00 |
| Learning Strategy Based on Deep Kno | Formal extension of noncommutative  | 0.45 |
| Learning Strategy Based on Deep Kno | Discovery of the Mercury Isotopes | 0.45 |
| COVLIAS 1.0: Lung Segmentation in C | On the influence of social norms on | 1.00 |
| COVLIAS 1.0: Lung Segmentation in C | Mindful self-care and resilience in | 1.00 |
| COVLIAS 1.0: Lung Segmentation in C | Formal extension of noncommutative  | 0.45 |
| COVLIAS 1.0: Lung Segmentation in C | Discovery of the Mercury Isotopes | 0.45 |
| On the influence of social norms on | Mindful self-care and resilience in | 1.00 |
| On the influence of social norms on | Formal extension of noncommutative  | 0.45 |
| On the influence of social norms on | Discovery of the Mercury Isotopes | 0.45 |
| Mindful self-care and resilience in | Formal extension of noncommutative  | 0.45 |
| Mindful self-care and resilience in | Discovery of the Mercury Isotopes | 0.45 |
| Downlink and Uplink Decoupling in T | Formal extension of noncommutative  | 0.82 |
| Downlink and Uplink Decoupling in T | Discovery of the Mercury Isotopes | 0.82 |
| Downlink and Uplink Decoupling in T | VoiceOfML/CMLMUF-Education-And-Hist | 0.71 |
| Formal extension of noncommutative  | Discovery of the Mercury Isotopes | 1.00 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.603
**Confidence:** HIGH
**Entropy nodes resolved:** 6

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
| 1 | Predicting Student Performance Using Data Mining a | 2020 | 0.559 | YES |
| 2 | A Comparison of Undersampling, Oversampling, and S | 2023 | 0.529 | YES |
| 3 | Computer Science | None | 0.394 | — |
| 4 | Impact of word embedding models on text analytics  | 2023 | 0.526 | YES |
| 5 | Transformer-based graphs for drug-drug interaction | 2026 | 0.274 | — |
| 6 | Artificial intelligence in cancer target identific | 2022 | 0.527 | YES |
| 7 | ProTox 3.0: a webserver for the prediction of toxi | 2024 | 0.370 | — |
| 8 | Artificial intelligence to deep learning: machine  | 2021 | 0.521 | YES |
| 9 | Artificial intelligence in drug discovery: recent  | 2021 | 0.520 | YES |
| 10 | jablonkagroup/chempile-education (dataset) | 2025 | 0.383 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 22
**Frequent 2-itemsets:** 36
**Frequent 3-itemsets:** 12
**Association rules:** 24

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.323 |
| [Emerging] AND (Very Recent work) | 0.262 |
| (Very Recent work) AND research in Computer Science | 0.194 |
| using Machine Learning AND research in Computer Science | 0.169 |
| [Emerging] AND using Machine Learning | 0.153 |
| [Emerging] AND (Recent work) | 0.151 |
| (Recent work) AND research in Computer Science | 0.151 |
| (Established work) AND research in Computer Science | 0.147 |
| with Positive findings AND [Emerging] | 0.143 |
| [Emerging] AND research in Education | 0.142 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| impact:emerging + topic:mathem | topic:computer science | 0.064 | 0.81 | 1.40 |
| topic:education | impact:emerging | 0.142 | 0.86 | 1.40 |
| topic:mathematics | topic:computer science | 0.092 | 0.80 | 1.39 |
| temporal:very_recent + topic:e | impact:emerging | 0.056 | 0.82 | 1.34 |
| method:machine_learning + temp | topic:computer science | 0.054 | 0.75 | 1.31 |
| impact:highly_cited | topic:computer science | 0.108 | 0.75 | 1.30 |
| method:machine_learning | topic:computer science | 0.169 | 0.74 | 1.28 |
| finding:positive + temporal:ve | impact:emerging | 0.076 | 0.77 | 1.25 |
| impact:emerging + method:machi | topic:computer science | 0.110 | 0.72 | 1.24 |
| method:machine_learning + temp | impact:emerging | 0.070 | 0.74 | 1.21 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 43393
**High-tier pairs:** 329
**Convergence events:** 6

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_002 | 0.246 | 2 | 1y | 2 |
| svw_005 | 0.180 | 4 | 4y | 4 |
| svw_004 | 0.176 | 5 | 12y | 5 |
| svw_001 | 0.146 | 2098 | 61y | 2098 |
| svw_003 | 0.143 | 2 | 2y | 2 |
| svw_006 | 0.097 | 3 | 6y | 3 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Artificial intelligence to deep learning: machine intelligence appr...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Artificial intelligence to deep learning: machine intelli... + included in golden token recommended path
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `29409efa04ac99ccf01d2a011d21d5d14e870000` (severity: 6)
- **On golden path:** Yes

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Molecular Docking: Shifting Paradigms in Drug Discovery' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Molecular Docking: Shifting Paradigms in Drug Discovery
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `8f7948d72b19b3be7191396c5e637cdb14a2371c` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Adaptive Federated Learning in Resource Constrained Edge Computing ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Adaptive Federated Learning in Resource Constrained Edge ...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `e2e0e226f1f74ff65c0de3e5ad565bcd8b9710da` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Deep Knowledge Tracing' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Deep Knowledge Tracing
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `fa98d609eb14ce25dd73cd8713a5e284948b4ff4` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Educational data mining and learning analytics: An updated survey' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Educational data mining and learning analytics: An update...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `7bd598f6a7c6eb4265fe5a9ca64504d1d639684a` (severity: 6)
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
| Total sources | 3123 |
| Timestamp | 2026-04-04T22:50:14.851503 |
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