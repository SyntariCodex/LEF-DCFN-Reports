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
| Graph Edges | 112419 |
| Knowledge Gaps (total) | 2687 |
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
| Well-grounded (≥0.7) | 1018 |
| Partially grounded (0.4–0.7) | 1766 |
| Weakly grounded (0.2–0.4) | 69 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.692** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2365 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.1793 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.5841 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2365 × Stability + 0.1793 × Concentration + 0.5841 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.40669472901936266 (30th percentile) |
| HIGH threshold | ≥ 0.5402588751387755 (80th percentile) |
| Concentration p25/p50/p75 | 0.4237124025821686 / 0.4379284381866455 / 0.4521714746952057 |
| Distinctiveness p25/p50/p75 | 0.4503746032714844 / 0.5799602270126343 / 0.6835525035858154 |
| Stability p25/p50/p75 | 0.19245608511353934 / 0.20610111888424365 / 0.22031511582623273 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 2869 |
|   — CONCEPT | 16 |
|   — DOCUMENT | 2853 |
| Total Edges | 112419 |
|   — MIRRORS | 103282 |
|   — EXTENDS | 4592 |
|   — CONTAINS | 3893 |
|   — ENABLES | 595 |
|   — DEPENDS_ON | 57 |
| Density | 0.013662 |
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
| Learning analytics: state of the art | 4 | 0.64 | 4 |
| Computer Science | 1 | 0.00 | 0 |
| Investigating student exposure to competency-based | 1 | 0.00 | 1 |
| Supervised diagnostic classification of cognitive  | 1 | 0.00 | 0 |
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

**Total entropy nodes:** 2687
**Critical (≥7):** 0 | **High (5-6):** 1919 | **Low (<5):** 768

**Issue Distribution:**

| Type | Count |
|------|-------|
| STALE | 2116 |
| DECAYED | 2079 |
| ORPHAN | 235 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Molecular Docking: Shifting Paradigms in Drug | 6.0/9 | STALE | — | 0 | 0 |
| 2 | Statistical Methods for Detecting Differentia | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Adaptive Federated Learning in Resource Const | 6.0/9 | STALE | — | 0 | 0 |
| 4 | Deep Knowledge Tracing | 6.0/9 | STALE | — | 0 | 0 |
| 5 | Educational data mining and learning analytic | 6.0/9 | STALE | — | 0 | 0 |
| 6 | The current landscape of learning analytics i | 6.0/9 | STALE | — | 0 | 0 |
| 7 | Educational data mining: prediction of studen | 6.0/9 | STALE | — | 0 | 0 |
| 8 | A Systematic Review on Educational Data Minin | 6.0/9 | STALE | — | 0 | 0 |
| 9 | Learning Analytics | 6.0/9 | STALE | — | 0 | 0 |
| 10 | Utilising learning analytics to support study | 6.0/9 | STALE | — | 0 | 0 |
| 11 | Predicting Student Performance Using Data Min | 6.0/9 | STALE | — | 0 | 0 |
| 12 | Organizational mindfulness towards digital tr | 6.0/9 | STALE | — | 0 | 0 |
| 13 | QSAR-Based Virtual Screening: Advances and Ap | 6.0/9 | STALE | — | 0 | 0 |
| 14 | Educational data mining and learning analytic | 6.0/9 | STALE | — | 0 | 0 |
| 15 | Deep Docking: A Deep Learning Platform for Au | 6.0/9 | STALE | — | 0 | 0 |
| 16 | Adaptive Learning-Based Task Offloading for V | 6.0/9 | STALE | — | 0 | 0 |
| 17 | Addressing two problems in deep knowledge tra | 6.0/9 | STALE | — | 0 | 0 |
| 18 | Multimodal Data Fusion in Learning Analytics: | 6.0/9 | STALE | — | 0 | 0 |
| 19 | Artificial Intelligence and Learning Analytic | 6.0/9 | STALE | — | 0 | 0 |
| 20 | Learning Analytics for Learning Design: A Sys | 6.0/9 | STALE | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 13 total (10 emerging, 3 established)
**Structural mirrors:** 55

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The PRISMA 2020 statement: an updated guideline fo | 2515 | Established | 2019.0 |
| Beyond Language Barriers: Allowing Multiple Langua | 2 | Emerging | 2023.5 |
| Implementing Diagnostic Assessment in Designing Di | 2 | Emerging | 2023.5 |
| Mental Health Literacy of Multi-Tiered Systems of  | 2 | Emerging | 2024.5 |
| Utilizing Cognitive Diagnostic Assessments to Iden | 2 | Emerging | 2024.0 |
| Generative AI Based on Deep Knowledge Tracing for  | 2 | Emerging | 2023.0 |
| COVLIAS 1.0Lesion vs. MedSeg: An Artificial Intell | 3 | Established | 2021.3 |
| Achievement goal perception: An interpersonal appr | 2 | Emerging | 2024.0 |
| Primary School Students with Reading Comprehension | 3 | Emerging | 2022.3 |
| Relationships Between First-Year Student Resilienc | 2 | Emerging | 2024.0 |
| Internalization of Mastery Goals: The Differential | 4 | Established | 2019.8 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 93 | Emerging | 2023.3 |
| Formal extension of noncommutative tensor-triangul | 2 | Emerging | 2023.5 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.93 |
| Implementing Diagnostic Assessment  | Mental Health Literacy of Multi-Tie | 1.00 |
| Implementing Diagnostic Assessment  | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Implementing Diagnostic Assessment  | Generative AI Based on Deep Knowled | 1.00 |
| Implementing Diagnostic Assessment  | COVLIAS 1.0Lesion vs. MedSeg: An Ar | 1.00 |
| Implementing Diagnostic Assessment  | Achievement goal perception: An int | 1.00 |
| Implementing Diagnostic Assessment  | Primary School Students with Readin | 1.00 |
| Implementing Diagnostic Assessment  | Relationships Between First-Year St | 1.00 |
| Implementing Diagnostic Assessment  | Internalization of Mastery Goals: T | 1.00 |
| Implementing Diagnostic Assessment  | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Implementing Diagnostic Assessment  | Formal extension of noncommutative  | 0.45 |
| Mental Health Literacy of Multi-Tie | Utilizing Cognitive Diagnostic Asse | 1.00 |
| Mental Health Literacy of Multi-Tie | Generative AI Based on Deep Knowled | 1.00 |
| Mental Health Literacy of Multi-Tie | COVLIAS 1.0Lesion vs. MedSeg: An Ar | 1.00 |
| Mental Health Literacy of Multi-Tie | Achievement goal perception: An int | 1.00 |
| Mental Health Literacy of Multi-Tie | Primary School Students with Readin | 1.00 |
| Mental Health Literacy of Multi-Tie | Relationships Between First-Year St | 1.00 |
| Mental Health Literacy of Multi-Tie | Internalization of Mastery Goals: T | 1.00 |
| Mental Health Literacy of Multi-Tie | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Mental Health Literacy of Multi-Tie | Formal extension of noncommutative  | 0.45 |
| Utilizing Cognitive Diagnostic Asse | Generative AI Based on Deep Knowled | 1.00 |
| Utilizing Cognitive Diagnostic Asse | COVLIAS 1.0Lesion vs. MedSeg: An Ar | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Achievement goal perception: An int | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Primary School Students with Readin | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Relationships Between First-Year St | 1.00 |
| Utilizing Cognitive Diagnostic Asse | Internalization of Mastery Goals: T | 1.00 |
| Utilizing Cognitive Diagnostic Asse | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Utilizing Cognitive Diagnostic Asse | Formal extension of noncommutative  | 0.45 |
| Generative AI Based on Deep Knowled | COVLIAS 1.0Lesion vs. MedSeg: An Ar | 1.00 |
| Generative AI Based on Deep Knowled | Achievement goal perception: An int | 1.00 |
| Generative AI Based on Deep Knowled | Primary School Students with Readin | 1.00 |
| Generative AI Based on Deep Knowled | Relationships Between First-Year St | 1.00 |
| Generative AI Based on Deep Knowled | Internalization of Mastery Goals: T | 1.00 |
| Generative AI Based on Deep Knowled | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Generative AI Based on Deep Knowled | Formal extension of noncommutative  | 0.45 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Achievement goal perception: An int | 1.00 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Primary School Students with Readin | 1.00 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Relationships Between First-Year St | 1.00 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Internalization of Mastery Goals: T | 1.00 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Formal extension of noncommutative  | 0.45 |
| Achievement goal perception: An int | Primary School Students with Readin | 1.00 |
| Achievement goal perception: An int | Relationships Between First-Year St | 1.00 |
| Achievement goal perception: An int | Internalization of Mastery Goals: T | 1.00 |
| Achievement goal perception: An int | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Achievement goal perception: An int | Formal extension of noncommutative  | 0.45 |
| Primary School Students with Readin | Relationships Between First-Year St | 1.00 |
| Primary School Students with Readin | Internalization of Mastery Goals: T | 1.00 |
| Primary School Students with Readin | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Primary School Students with Readin | Formal extension of noncommutative  | 0.45 |
| Relationships Between First-Year St | Internalization of Mastery Goals: T | 1.00 |
| Relationships Between First-Year St | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Relationships Between First-Year St | Formal extension of noncommutative  | 0.45 |
| Internalization of Mastery Goals: T | VoiceOfML/CMLMUF-Education-And-Hist | 0.41 |
| Internalization of Mastery Goals: T | Formal extension of noncommutative  | 0.45 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 5.424
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
| 1 | Predicting Student Performance Using Data Mining a | 2020 | 0.603 | YES |
| 2 | Educational data mining: prediction of students' a | 2022 | 0.586 | YES |
| 3 | Utilising learning analytics to support study succ | 2020 | 0.591 | YES |
| 4 | Educational data mining and learning analytics: An | 2020 | 0.549 | YES |
| 5 | Educational data mining and learning analytics for | 2019 | 0.530 | YES |
| 6 | Learning Analytics | 2019 | 0.519 | YES |
| 7 | Learning Analytics for Learning Design: A Systemat | 2019 | 0.529 | YES |
| 8 | The current landscape of learning analytics in hig | 2018 | 0.509 | YES |
| 9 | Integration of artificial intelligence performance | 2023 | 0.501 | — |
| 10 | Addressing two problems in deep knowledge tracing  | 2018 | 0.506 | YES |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 22
**Frequent 2-itemsets:** 39
**Frequent 3-itemsets:** 16
**Association rules:** 33

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.354 |
| [Emerging] AND (Very Recent work) | 0.267 |
| (Very Recent work) AND research in Computer Science | 0.212 |
| using Machine Learning AND research in Computer Science | 0.184 |
| (Recent work) AND research in Computer Science | 0.164 |
| (Established work) AND research in Computer Science | 0.161 |
| [Emerging] AND using Machine Learning | 0.161 |
| [Emerging] AND research in Education | 0.155 |
| [Emerging] AND (Recent work) | 0.152 |
| with Positive findings AND [Emerging] | 0.148 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| population:clinical + topic:ed | impact:emerging | 0.051 | 0.99 | 1.62 |
| method:machine_learning + topi | topic:computer science | 0.050 | 0.95 | 1.51 |
| method:machine_learning + temp | topic:computer science | 0.054 | 0.94 | 1.49 |
| topic:education | impact:emerging | 0.155 | 0.85 | 1.39 |
| impact:highly_cited | topic:computer science | 0.118 | 0.85 | 1.34 |
| temporal:very_recent + topic:e | impact:emerging | 0.061 | 0.81 | 1.32 |
| impact:emerging + topic:mathem | topic:computer science | 0.070 | 0.81 | 1.29 |
| topic:mathematics | topic:computer science | 0.101 | 0.80 | 1.27 |
| population:clinical | impact:emerging | 0.102 | 0.78 | 1.27 |
| finding:positive + temporal:ve | impact:emerging | 0.081 | 0.77 | 1.26 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 44294
**High-tier pairs:** 318
**Convergence events:** 5

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_004 | 0.180 | 4 | 4y | 4 |
| svw_001 | 0.147 | 1936 | 53y | 1936 |
| svw_003 | 0.143 | 2 | 2y | 2 |
| svw_005 | 0.097 | 3 | 6y | 3 |
| svw_002 | 0.055 | 2 | 7y | 2 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Molecular Docking: Shifting Paradigms in Drug Discovery' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Molecular Docking: Shifting Paradigms in Drug Discovery
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 95% confidence in apriori patterns)
- **Gap node:** `8f7948d72b19b3be7191396c5e637cdb14a2371c` (severity: 6.0)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Statistical Methods for Detecting Differentially Abundant Features ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Statistical Methods for Detecting Differentially Abundant...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 95% confidence in apriori patterns)
- **Gap node:** `a80ba5b7c4ea6551a6f4ab64fde15819125bd1cb` (severity: 6.0)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Adaptive Federated Learning in Resource Constrained Edge Computing ...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Adaptive Federated Learning in Resource Constrained Edge ...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 95% confidence in apriori patterns)
- **Gap node:** `e2e0e226f1f74ff65c0de3e5ad565bcd8b9710da` (severity: 6.0)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Deep Knowledge Tracing' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Deep Knowledge Tracing
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 95% confidence in apriori patterns)
- **Gap node:** `fa98d609eb14ce25dd73cd8713a5e284948b4ff4` (severity: 6.0)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Educational data mining and learning analytics: An updated survey' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Educational data mining and learning analytics: An update... + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 95% confidence in apriori patterns)
- **Gap node:** `7bd598f6a7c6eb4265fe5a9ca64504d1d639684a` (severity: 6.0)
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
| Total sources | 2853 |
| Timestamp | 2026-04-05T23:33:32.427546 |
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