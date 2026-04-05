# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 05, 2026
**Sources:** 2853

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 2853 |
| Graph Nodes | 2869 |
| Graph Edges | 112318 |
| Knowledge Gaps (total) | 2843 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 13 |
| Convergence Events | 5 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 2853

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
| Well-grounded (≥0.7) | 1020 |
| Partially grounded (0.4–0.7) | 1765 |
| Weakly grounded (0.2–0.4) | 68 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.692** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2483 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.1501 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.25 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2483 × Stability + 0.1501 × Concentration + 0.25 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.23634545568142779 (30th percentile) |
| HIGH threshold | ≥ 0.2944397186593036 (80th percentile) |
| Concentration p25/p50/p75 | 0.42376941442489624 / 0.4379591941833496 / 0.45224010944366455 |
| Distinctiveness p25/p50/p75 | 0.4502091407775879 / 0.5799564719200134 / 0.6834682822227478 |
| Stability p25/p50/p75 | 0.1931784927296375 / 0.2064043464045397 / 0.21998075550301407 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 2869 |
|   — CONCEPT | 16 |
|   — DOCUMENT | 2853 |
| Total Edges | 112318 |
|   — MIRRORS | 103173 |
|   — EXTENDS | 4603 |
|   — CONTAINS | 3895 |
|   — ENABLES | 589 |
|   — DEPENDS_ON | 58 |
| Density | 0.013650 |
| Connected Components | 240 |

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
| Learning analytics: state of the art | 3 | 0.56 | 3 |
| Computer Science | 1 | 0.00 | 0 |
| Investigating student exposure to competency-based | 1 | 0.00 | 1 |
| Supervised diagnostic classification of cognitive  | 1 | 0.00 | 1 |
| Self-Regulated Learning Model in Educational Data  | 1 | 0.00 | 1 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| BamaER: A Behavior-Aware Memory-Augmented Mod | 0 | 0 | 0 | 0 |
| A Survey on the Classification Techniques In  | 0 | 0 | 0 | 0 |
| From neurotechnology to the classroom: the pr | 0 | 0 | 0 | 0 |
| Measuring Implementation of Multi-Tiered Syst | 0 | 0 | 0 | 0 |
| Debiased Cognitive Diagnosis: A Contrastive C | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 2843
**Critical (≥7):** 0 | **High (5-6):** 2199 | **Low (<5):** 644

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 2843 |
| STALE | 2753 |
| ORPHAN | 235 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Molecular Docking: Shifting Paradigms in Drug | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Adaptive Federated Learning in Resource Const | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Deep Knowledge Tracing | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Adaptive Learning Using Artificial Intelligen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | D’ya Like DAGs? A Survey on Structure Learnin | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | The current landscape of learning analytics i | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Educational data mining: prediction of studen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | A Systematic Review on Educational Data Minin | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Learning Analytics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Utilising learning analytics to support study | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Impact of word embedding models on text analy | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Organizational mindfulness towards digital tr | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | A Comparison of Undersampling, Oversampling,  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Deep Docking: A Deep Learning Platform for Au | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Addressing two problems in deep knowledge tra | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Human-Centred Learning Analytics and AI in Ed | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 13 total (10 emerging, 3 established)
**Structural mirrors:** 46

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The PRISMA 2020 statement: an updated guideline fo | 2514 | Established | 2019.0 |
| Beyond Language Barriers: Allowing Multiple Langua | 2 | Emerging | 2023.5 |
| Implementing Diagnostic Assessment in Designing Di | 2 | Emerging | 2023.5 |
| Mental Health Literacy of Multi-Tiered Systems of  | 2 | Emerging | 2024.5 |
| Utilizing Cognitive Diagnostic Assessments to Iden | 2 | Emerging | 2024.0 |
| Learning Strategy Based on Deep Knowledge Tracing | 2 | Emerging | 2023.0 |
| Inter-Variability Study of COVLIAS 1.0: Hybrid Dee | 3 | Established | 2021.3 |
| On the influence of social norms on individual ach | 2 | Emerging | 2024.0 |
| Primary School Students with Reading Comprehension | 3 | Emerging | 2022.3 |
| Mindful self-care and resilience in first-year und | 2 | Emerging | 2024.0 |
| The development of achievement goals throughout co | 4 | Established | 2019.8 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 94 | Emerging | 2023.6 |
| Formal extension of noncommutative tensor-triangul | 2 | Emerging | 2023.5 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.93 |
| Implementing Diagnostic Assessment  | Mental Health Literacy of Multi-Tie | 1.00 |
| Implementing Diagnostic Assessment  | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Implementing Diagnostic Assessment  | Learning Strategy Based on Deep Kno | 1.00 |
| Implementing Diagnostic Assessment  | Inter-Variability Study of COVLIAS  | 1.00 |
| Implementing Diagnostic Assessment  | On the influence of social norms on | 1.00 |
| Implementing Diagnostic Assessment  | Primary School Students with Readin | 1.00 |
| Implementing Diagnostic Assessment  | Mindful self-care and resilience in | 1.00 |
| Implementing Diagnostic Assessment  | The development of achievement goal | 1.00 |
| Implementing Diagnostic Assessment  | Formal extension of noncommutative  | 0.45 |
| Mental Health Literacy of Multi-Tie | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Mental Health Literacy of Multi-Tie | Learning Strategy Based on Deep Kno | 1.00 |
| Mental Health Literacy of Multi-Tie | Inter-Variability Study of COVLIAS  | 1.00 |
| Mental Health Literacy of Multi-Tie | On the influence of social norms on | 1.00 |
| Mental Health Literacy of Multi-Tie | Primary School Students with Readin | 1.00 |
| Mental Health Literacy of Multi-Tie | Mindful self-care and resilience in | 1.00 |
| Mental Health Literacy of Multi-Tie | The development of achievement goal | 1.00 |
| Mental Health Literacy of Multi-Tie | Formal extension of noncommutative  | 0.45 |
| Utilizing Cognitive Diagnostic Asse | Learning Strategy Based on Deep Kno | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Inter-Variability Study of COVLIAS  | 1.00 |
| Utilizing Cognitive Diagnostic Asse | On the influence of social norms on | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Primary School Students with Readin | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Mindful self-care and resilience in | 1.00 |
| Utilizing Cognitive Diagnostic Asse | The development of achievement goal | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Formal extension of noncommutative  | 0.45 |
| Learning Strategy Based on Deep Kno | Inter-Variability Study of COVLIAS  | 1.00 |
| Learning Strategy Based on Deep Kno | On the influence of social norms on | 1.00 |
| Learning Strategy Based on Deep Kno | Primary School Students with Readin | 1.00 |
| Learning Strategy Based on Deep Kno | Mindful self-care and resilience in | 1.00 |
| Learning Strategy Based on Deep Kno | The development of achievement goal | 1.00 |
| Learning Strategy Based on Deep Kno | Formal extension of noncommutative  | 0.45 |
| Inter-Variability Study of COVLIAS  | On the influence of social norms on | 1.00 |
| Inter-Variability Study of COVLIAS  | Primary School Students with Readin | 1.00 |
| Inter-Variability Study of COVLIAS  | Mindful self-care and resilience in | 1.00 |
| Inter-Variability Study of COVLIAS  | The development of achievement goal | 1.00 |
| Inter-Variability Study of COVLIAS  | Formal extension of noncommutative  | 0.45 |
| On the influence of social norms on | Primary School Students with Readin | 1.00 |
| On the influence of social norms on | Mindful self-care and resilience in | 1.00 |
| On the influence of social norms on | The development of achievement goal | 1.00 |
| On the influence of social norms on | Formal extension of noncommutative  | 0.45 |
| Primary School Students with Readin | Mindful self-care and resilience in | 1.00 |
| Primary School Students with Readin | The development of achievement goal | 1.00 |
| Primary School Students with Readin | Formal extension of noncommutative  | 0.45 |
| Mindful self-care and resilience in | The development of achievement goal | 1.00 |
| Mindful self-care and resilience in | Formal extension of noncommutative  | 0.45 |
| The development of achievement goal | Formal extension of noncommutative  | 0.45 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.301
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
| 1 | Predicting Student Performance Using Data Mining a | 2020 | 0.565 | YES |
| 2 | A Comparison of Undersampling, Oversampling, and S | 2023 | 0.529 | YES |
| 3 | Computer Science | None | 0.407 | — |
| 4 | Impact of word embedding models on text analytics  | 2023 | 0.526 | YES |
| 5 | Transformer-based graphs for drug-drug interaction | 2026 | 0.273 | — |
| 6 | Deep Docking: A Deep Learning Platform for Augment | 2020 | 0.498 | YES |
| 7 | Molecular Docking: Shifting Paradigms in Drug Disc | 2019 | 0.488 | YES |
| 8 | Medicine | None | 0.260 | — |
| 9 | QSAR-Based Virtual Screening: Advances and Applica | 2018 | 0.479 | YES |
| 10 | Large scale comparison of QSAR and conformal predi | 2019 | 0.277 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 22
**Frequent 2-itemsets:** 39
**Frequent 3-itemsets:** 15
**Association rules:** 32

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.354 |
| [Emerging] AND (Very Recent work) | 0.266 |
| (Very Recent work) AND research in Computer Science | 0.212 |
| using Machine Learning AND research in Computer Science | 0.185 |
| (Recent work) AND research in Computer Science | 0.165 |
| [Emerging] AND using Machine Learning | 0.161 |
| (Established work) AND research in Computer Science | 0.161 |
| [Emerging] AND research in Education | 0.155 |
| [Emerging] AND (Recent work) | 0.152 |
| with Positive findings AND [Emerging] | 0.148 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| population:clinical + topic:ed | impact:emerging | 0.051 | 0.99 | 1.62 |
| method:machine_learning + temp | topic:computer science | 0.054 | 0.94 | 1.49 |
| topic:education | impact:emerging | 0.155 | 0.86 | 1.40 |
| impact:highly_cited | topic:computer science | 0.118 | 0.85 | 1.34 |
| temporal:very_recent + topic:e | impact:emerging | 0.061 | 0.82 | 1.34 |
| impact:emerging + topic:mathem | topic:computer science | 0.070 | 0.81 | 1.28 |
| topic:mathematics | topic:computer science | 0.102 | 0.80 | 1.27 |
| population:clinical | impact:emerging | 0.102 | 0.78 | 1.27 |
| method:machine_learning + temp | topic:computer science | 0.059 | 0.79 | 1.25 |
| finding:positive + temporal:ve | impact:emerging | 0.081 | 0.77 | 1.25 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 44761
**High-tier pairs:** 314
**Convergence events:** 5

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_004 | 0.180 | 4 | 4y | 4 |
| svw_001 | 0.147 | 1935 | 53y | 1935 |
| svw_003 | 0.143 | 2 | 2y | 2 |
| svw_005 | 0.097 | 3 | 6y | 3 |
| svw_002 | 0.055 | 2 | 7y | 2 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Molecular Docking: Shifting Paradigms in Drug Discovery' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Molecular Docking: Shifting Paradigms in Drug Discovery + included in golden token recommended path
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 94% confidence in apriori patterns)
- **Gap node:** `8f7948d72b19b3be7191396c5e637cdb14a2371c` (severity: 6)
- **On golden path:** Yes

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Adaptive Federated Learning in Resource Constrained Edge Computing ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Adaptive Federated Learning in Resource Constrained Edge ...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 94% confidence in apriori patterns)
- **Gap node:** `e2e0e226f1f74ff65c0de3e5ad565bcd8b9710da` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Deep Knowledge Tracing' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Deep Knowledge Tracing
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 94% confidence in apriori patterns)
- **Gap node:** `fa98d609eb14ce25dd73cd8713a5e284948b4ff4` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Educational data mining and learning analytics: An updated survey' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Educational data mining and learning analytics: An update...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 94% confidence in apriori patterns)
- **Gap node:** `7bd598f6a7c6eb4265fe5a9ca64504d1d639684a` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Adaptive Learning Using Artificial Intelligence in e-Learning: A Li...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Adaptive Learning Using Artificial Intelligence in e-Lear...
- **Novel because:** not yet connected to 'Adaptive Learning through Artificial Intelligence' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 94% confidence in apriori patterns)
- **Gap node:** `f54faf827b5ccd529bd602659f607db6560dfb85` (severity: 6)
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
| Total sources | 2853 |
| Timestamp | 2026-04-05T05:14:43.661318 |
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