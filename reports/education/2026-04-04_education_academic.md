# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3118

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 3118 |
| Graph Nodes | 3135 |
| Graph Edges | 7330 |
| Knowledge Gaps (total) | 3108 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 24 |
| Convergence Events | 12 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3118

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
| Well-grounded (≥0.7) | 1137 |
| Partially grounded (0.4–0.7) | 1916 |
| Weakly grounded (0.2–0.4) | 65 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.696** |

## 3. Source Encoding (QEB)

### 3.1 Method

TF-IDF vectorization (5,000 features, unigrams + bigrams, sublinear TF) → Truncated SVD → 256-dimensional dense vectors. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.40 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.35 | Energy fraction in top 10% of SVD dimensions |
| Corpus Distinctiveness | 0.25 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.40 × Stability + 0.35 × Concentration + 0.25 × Distinctiveness

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 256 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.4604668083887977 (30th percentile) |
| HIGH threshold | ≥ 0.4993727420572564 (80th percentile) |
| Concentration p25/p50/p75 | 0.491899828305727 / 0.5344054897614174 / 0.5908521009621022 |
| Distinctiveness p25/p50/p75 | 0.6521007369439367 / 0.694409818363625 / 0.7409783761877583 |
| Stability p25/p50/p75 | 0.26431726377057063 / 0.280953388899814 / 0.2977721357122917 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3135 |
|   — CONCEPT | 17 |
|   — DOCUMENT | 3118 |
| Total Edges | 7330 |
|   — CONTAINS | 4206 |
|   — MIRRORS | 1827 |
|   — ENABLES | 812 |
|   — EXTENDS | 413 |
|   — DEPENDS_ON | 72 |
| Density | 0.000746 |
| Connected Components | 347 |

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
| Education | 1 | 0.00 | 0 |
| Neuroscience | 1 | 0.00 | 0 |
| Biology | 1 | 0.00 | 0 |
| Mathematics | 1 | 0.00 | 0 |

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

**Total entropy nodes:** 3108
**Critical (≥7):** 0 | **High (5-6):** 950 | **Low (<5):** 2158

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3108 |
| STALE | 3018 |
| ORPHAN | 343 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Artificial intelligence to deep learning: mac | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Molecular Docking: Shifting Paradigms in Drug | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Deep Knowledge Tracing | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | The current landscape of learning analytics i | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Educational data mining: prediction of studen | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | A Systematic Review on Educational Data Minin | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Learning Analytics | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | Utilising learning analytics to support study | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Artificial intelligence in drug discovery: re | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Revolutionizing Medicinal Chemistry: The Appl | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Addressing two problems in deep knowledge tra | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Multimodal Data Fusion in Learning Analytics: | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Learning Analytics for Learning Design: A Sys | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | A Systematic Review of Empirical Studies on L | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | A Systematic Review of Deep Learning Approach | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | A Core Components Framework for Evaluating Im | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 24 total (7 emerging, 17 established)
**Structural mirrors:** 169

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| The PRISMA 2020 statement: an updated guideline fo | 2198 | Established | 2018.6 |
| Accelerated discovery of stable lead-free hybrid o | 2 | Established | 2018.0 |
| Core principles of assessment in competency-based  | 49 | Established | 2018.4 |
| Human Circulating and Tissue-Resident CD56bright N | 12 | Established | 2019.9 |
| Adaptive e-learning systems through learning style | 2 | Established | 2020.0 |
| Next challenges for adaptive learning systems | 2 | Established | 2015.0 |
| Toward a definition of competency-based education  | 120 | Established | 2017.6 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 290 | Established | 2018.9 |
| Revisiting education reform in Kenya: A case of Co | 4 | Established | 2019.0 |
| An Intelligent Prediction System for Educational D | 2 | Established | 2020.5 |
| Development of a machine learning-based tool to ev | 3 | Emerging | 2022.7 |
| Recovering Concept Prerequisite Relations from Uni | 2 | Established | 2019.0 |
| ContextKT: A Context-Based Method for Knowledge Tr | 2 | Emerging | 2023.0 |
| Designing School Health Services to Provide Multi- | 2 | Emerging | 2023.5 |
| Issues in Statewide Scale up of a Multi-Tiered Sys | 2 | Emerging | 2023.0 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| The PRISMA 2020 statement: an updat | Accelerated discovery of stable lea | 0.97 |
| The PRISMA 2020 statement: an updat | Core principles of assessment in co | 0.49 |
| The PRISMA 2020 statement: an updat | Human Circulating and Tissue-Reside | 0.82 |
| The PRISMA 2020 statement: an updat | Adaptive e-learning systems through | 0.83 |
| The PRISMA 2020 statement: an updat | Next challenges for adaptive learni | 0.83 |
| The PRISMA 2020 statement: an updat | Toward a definition of competency-b | 0.53 |
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.91 |
| The PRISMA 2020 statement: an updat | Revisiting education reform in Keny | 0.96 |
| The PRISMA 2020 statement: an updat | An Intelligent Prediction System fo | 0.83 |
| The PRISMA 2020 statement: an updat | Recovering Concept Prerequisite Rel | 0.83 |
| The PRISMA 2020 statement: an updat | Designing School Health Services to | 0.76 |
| The PRISMA 2020 statement: an updat | Evaluating English language learner | 0.93 |
| The PRISMA 2020 statement: an updat | Unearthing People from the SaND: Re | 0.97 |
| The PRISMA 2020 statement: an updat | Handbook of treatment for eating di | 0.89 |
| The PRISMA 2020 statement: an updat | Knowledge discovery in cardiology:  | 0.93 |
| The PRISMA 2020 statement: an updat | Discovery of the Einsteinium Isotop | 0.87 |
| The PRISMA 2020 statement: an updat | Skyemou5/Pysoma: A crossplatform Ho | 0.97 |
| Accelerated discovery of stable lea | Human Circulating and Tissue-Reside | 0.74 |
| Accelerated discovery of stable lea | Adaptive e-learning systems through | 0.71 |
| Accelerated discovery of stable lea | Next challenges for adaptive learni | 0.71 |
| Accelerated discovery of stable lea | VoiceOfML/CMLMUF-Education-And-Hist | 0.87 |
| Accelerated discovery of stable lea | Revisiting education reform in Keny | 0.95 |
| Accelerated discovery of stable lea | An Intelligent Prediction System fo | 0.71 |
| Accelerated discovery of stable lea | Recovering Concept Prerequisite Rel | 0.71 |
| Accelerated discovery of stable lea | Designing School Health Services to | 0.58 |
| Accelerated discovery of stable lea | Evaluating English language learner | 0.89 |
| Accelerated discovery of stable lea | Unearthing People from the SaND: Re | 1.00 |
| Accelerated discovery of stable lea | Handbook of treatment for eating di | 0.85 |
| Accelerated discovery of stable lea | Knowledge discovery in cardiology:  | 0.89 |
| Accelerated discovery of stable lea | Discovery of the Einsteinium Isotop | 0.89 |
| Accelerated discovery of stable lea | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| Core principles of assessment in co | Human Circulating and Tissue-Reside | 0.88 |
| Core principles of assessment in co | Toward a definition of competency-b | 1.00 |
| Core principles of assessment in co | VoiceOfML/CMLMUF-Education-And-Hist | 0.76 |
| Core principles of assessment in co | Revisiting education reform in Keny | 0.62 |
| Core principles of assessment in co | Designing School Health Services to | 0.79 |
| Core principles of assessment in co | Evaluating English language learner | 0.72 |
| Core principles of assessment in co | Handbook of treatment for eating di | 0.76 |
| Core principles of assessment in co | Knowledge discovery in cardiology:  | 0.72 |
| Core principles of assessment in co | processing/p5.js: p5.js is a client | 0.74 |
| Human Circulating and Tissue-Reside | Adaptive e-learning systems through | 0.53 |
| Human Circulating and Tissue-Reside | Next challenges for adaptive learni | 0.53 |
| Human Circulating and Tissue-Reside | Toward a definition of competency-b | 0.90 |
| Human Circulating and Tissue-Reside | VoiceOfML/CMLMUF-Education-And-Hist | 0.98 |
| Human Circulating and Tissue-Reside | Revisiting education reform in Keny | 0.92 |
| Human Circulating and Tissue-Reside | An Intelligent Prediction System fo | 0.53 |
| Human Circulating and Tissue-Reside | Recovering Concept Prerequisite Rel | 0.53 |
| Human Circulating and Tissue-Reside | Designing School Health Services to | 0.82 |
| Human Circulating and Tissue-Reside | Evaluating English language learner | 0.96 |
| Human Circulating and Tissue-Reside | Unearthing People from the SaND: Re | 0.74 |
| Human Circulating and Tissue-Reside | Handbook of treatment for eating di | 0.97 |
| Human Circulating and Tissue-Reside | Knowledge discovery in cardiology:  | 0.96 |
| Human Circulating and Tissue-Reside | Discovery of the Einsteinium Isotop | 0.66 |
| Human Circulating and Tissue-Reside | processing/p5.js: p5.js is a client | 0.61 |
| Human Circulating and Tissue-Reside | Skyemou5/Pysoma: A crossplatform Ho | 0.74 |
| Adaptive e-learning systems through | Next challenges for adaptive learni | 1.00 |
| Adaptive e-learning systems through | VoiceOfML/CMLMUF-Education-And-Hist | 0.61 |
| Adaptive e-learning systems through | Revisiting education reform in Keny | 0.67 |
| Adaptive e-learning systems through | An Intelligent Prediction System fo | 1.00 |
| Adaptive e-learning systems through | Development of a machine learning-b | 0.71 |
| Adaptive e-learning systems through | Recovering Concept Prerequisite Rel | 1.00 |
| Adaptive e-learning systems through | ContextKT: A Context-Based Method f | 0.71 |
| Adaptive e-learning systems through | Designing School Health Services to | 0.82 |
| Adaptive e-learning systems through | Issues in Statewide Scale up of a M | 0.71 |
| Adaptive e-learning systems through | Evaluating English language learner | 0.63 |
| Adaptive e-learning systems through | Unearthing People from the SaND: Re | 0.71 |
| Adaptive e-learning systems through | Handbook of treatment for eating di | 0.60 |
| Adaptive e-learning systems through | Knowledge discovery in cardiology:  | 0.63 |
| Adaptive e-learning systems through | Discovery of the Einsteinium Isotop | 0.63 |
| Adaptive e-learning systems through | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Next challenges for adaptive learni | VoiceOfML/CMLMUF-Education-And-Hist | 0.61 |
| Next challenges for adaptive learni | Revisiting education reform in Keny | 0.67 |
| Next challenges for adaptive learni | An Intelligent Prediction System fo | 1.00 |
| Next challenges for adaptive learni | Development of a machine learning-b | 0.71 |
| Next challenges for adaptive learni | Recovering Concept Prerequisite Rel | 1.00 |
| Next challenges for adaptive learni | ContextKT: A Context-Based Method f | 0.71 |
| Next challenges for adaptive learni | Designing School Health Services to | 0.82 |
| Next challenges for adaptive learni | Issues in Statewide Scale up of a M | 0.71 |
| Next challenges for adaptive learni | Evaluating English language learner | 0.63 |
| Next challenges for adaptive learni | Unearthing People from the SaND: Re | 0.71 |
| Next challenges for adaptive learni | Handbook of treatment for eating di | 0.60 |
| Next challenges for adaptive learni | Knowledge discovery in cardiology:  | 0.63 |
| Next challenges for adaptive learni | Discovery of the Einsteinium Isotop | 0.63 |
| Next challenges for adaptive learni | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Toward a definition of competency-b | VoiceOfML/CMLMUF-Education-And-Hist | 0.79 |
| Toward a definition of competency-b | Revisiting education reform in Keny | 0.65 |
| Toward a definition of competency-b | Designing School Health Services to | 0.82 |
| Toward a definition of competency-b | Evaluating English language learner | 0.75 |
| Toward a definition of competency-b | Handbook of treatment for eating di | 0.79 |
| Toward a definition of competency-b | Knowledge discovery in cardiology:  | 0.75 |
| Toward a definition of competency-b | processing/p5.js: p5.js is a client | 0.73 |
| VoiceOfML/CMLMUF-Education-And-Hist | Revisiting education reform in Keny | 0.98 |
| VoiceOfML/CMLMUF-Education-And-Hist | An Intelligent Prediction System fo | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Recovering Concept Prerequisite Rel | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Designing School Health Services to | 0.79 |
| VoiceOfML/CMLMUF-Education-And-Hist | Evaluating English language learner | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Unearthing People from the SaND: Re | 0.87 |
| VoiceOfML/CMLMUF-Education-And-Hist | Handbook of treatment for eating di | 0.99 |
| VoiceOfML/CMLMUF-Education-And-Hist | Knowledge discovery in cardiology:  | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Discovery of the Einsteinium Isotop | 0.78 |
| VoiceOfML/CMLMUF-Education-And-Hist | processing/p5.js: p5.js is a client | 0.52 |
| VoiceOfML/CMLMUF-Education-And-Hist | Skyemou5/Pysoma: A crossplatform Ho | 0.87 |
| Revisiting education reform in Keny | An Intelligent Prediction System fo | 0.67 |
| Revisiting education reform in Keny | Recovering Concept Prerequisite Rel | 0.67 |
| Revisiting education reform in Keny | Designing School Health Services to | 0.73 |
| Revisiting education reform in Keny | Evaluating English language learner | 0.99 |
| Revisiting education reform in Keny | Unearthing People from the SaND: Re | 0.95 |
| Revisiting education reform in Keny | Handbook of treatment for eating di | 0.96 |
| Revisiting education reform in Keny | Knowledge discovery in cardiology:  | 0.99 |
| Revisiting education reform in Keny | Discovery of the Einsteinium Isotop | 0.85 |
| Revisiting education reform in Keny | Skyemou5/Pysoma: A crossplatform Ho | 0.95 |
| An Intelligent Prediction System fo | Development of a machine learning-b | 0.71 |
| An Intelligent Prediction System fo | Recovering Concept Prerequisite Rel | 1.00 |
| An Intelligent Prediction System fo | ContextKT: A Context-Based Method f | 0.71 |
| An Intelligent Prediction System fo | Designing School Health Services to | 0.82 |
| An Intelligent Prediction System fo | Issues in Statewide Scale up of a M | 0.71 |
| An Intelligent Prediction System fo | Evaluating English language learner | 0.63 |
| An Intelligent Prediction System fo | Unearthing People from the SaND: Re | 0.71 |
| An Intelligent Prediction System fo | Handbook of treatment for eating di | 0.60 |
| An Intelligent Prediction System fo | Knowledge discovery in cardiology:  | 0.63 |
| An Intelligent Prediction System fo | Discovery of the Einsteinium Isotop | 0.63 |
| An Intelligent Prediction System fo | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Development of a machine learning-b | Recovering Concept Prerequisite Rel | 0.71 |
| Development of a machine learning-b | ContextKT: A Context-Based Method f | 1.00 |
| Development of a machine learning-b | Designing School Health Services to | 0.58 |
| Development of a machine learning-b | Issues in Statewide Scale up of a M | 1.00 |
| Recovering Concept Prerequisite Rel | ContextKT: A Context-Based Method f | 0.71 |
| Recovering Concept Prerequisite Rel | Designing School Health Services to | 0.82 |
| Recovering Concept Prerequisite Rel | Issues in Statewide Scale up of a M | 0.71 |
| Recovering Concept Prerequisite Rel | Evaluating English language learner | 0.63 |
| Recovering Concept Prerequisite Rel | Unearthing People from the SaND: Re | 0.71 |
| Recovering Concept Prerequisite Rel | Handbook of treatment for eating di | 0.60 |
| Recovering Concept Prerequisite Rel | Knowledge discovery in cardiology:  | 0.63 |
| Recovering Concept Prerequisite Rel | Discovery of the Einsteinium Isotop | 0.63 |
| Recovering Concept Prerequisite Rel | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| ContextKT: A Context-Based Method f | Designing School Health Services to | 0.58 |
| ContextKT: A Context-Based Method f | Issues in Statewide Scale up of a M | 1.00 |
| Designing School Health Services to | Issues in Statewide Scale up of a M | 0.58 |
| Designing School Health Services to | Evaluating English language learner | 0.77 |
| Designing School Health Services to | Unearthing People from the SaND: Re | 0.58 |
| Designing School Health Services to | Handbook of treatment for eating di | 0.78 |
| Designing School Health Services to | Knowledge discovery in cardiology:  | 0.77 |
| Designing School Health Services to | Discovery of the Einsteinium Isotop | 0.52 |
| Designing School Health Services to | processing/p5.js: p5.js is a client | 0.52 |
| Designing School Health Services to | Skyemou5/Pysoma: A crossplatform Ho | 0.58 |
| Evaluating English language learner | Unearthing People from the SaND: Re | 0.89 |
| Evaluating English language learner | Handbook of treatment for eating di | 0.98 |
| Evaluating English language learner | Knowledge discovery in cardiology:  | 1.00 |
| Evaluating English language learner | Discovery of the Einsteinium Isotop | 0.80 |
| Evaluating English language learner | processing/p5.js: p5.js is a client | 0.48 |
| Evaluating English language learner | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Unearthing People from the SaND: Re | Handbook of treatment for eating di | 0.85 |
| Unearthing People from the SaND: Re | Knowledge discovery in cardiology:  | 0.89 |
| Unearthing People from the SaND: Re | Discovery of the Einsteinium Isotop | 0.89 |
| Unearthing People from the SaND: Re | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| Handbook of treatment for eating di | Knowledge discovery in cardiology:  | 0.98 |
| Handbook of treatment for eating di | Discovery of the Einsteinium Isotop | 0.83 |
| Handbook of treatment for eating di | processing/p5.js: p5.js is a client | 0.63 |
| Handbook of treatment for eating di | Skyemou5/Pysoma: A crossplatform Ho | 0.85 |
| Culture, goal orientation and achie | COVLIAS 1.0Lesion vs. MedSeg: An Ar | 1.00 |
| Culture, goal orientation and achie | Discovery of the Einsteinium Isotop | 0.45 |
| Culture, goal orientation and achie | processing/p5.js: p5.js is a client | 0.67 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | Discovery of the Einsteinium Isotop | 0.45 |
| COVLIAS 1.0Lesion vs. MedSeg: An Ar | processing/p5.js: p5.js is a client | 0.67 |
| Knowledge discovery in cardiology:  | Discovery of the Einsteinium Isotop | 0.80 |
| Knowledge discovery in cardiology:  | processing/p5.js: p5.js is a client | 0.48 |
| Knowledge discovery in cardiology:  | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Discovery of the Einsteinium Isotop | processing/p5.js: p5.js is a client | 0.46 |
| Discovery of the Einsteinium Isotop | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.721
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
| 1 | Educational data mining: prediction of students' a | 2022 | 0.516 | YES |
| 2 | The current landscape of learning analytics in hig | 2018 | 0.479 | YES |
| 3 | Predicting Student Performance Using Data Mining a | 2020 | 0.498 | YES |
| 4 | Educational data mining and learning analytics: An | 2020 | 0.498 | YES |
| 5 | A Systematic Review of Deep Learning Approaches to | 2019 | 0.483 | YES |
| 6 | Educational data mining and learning analytics for | 2019 | 0.488 | YES |
| 7 | Computer Science | None | 0.393 | — |
| 8 | THU-TIOE-ML/GLM3_6B_Education_Ornstein | 2026 | 0.502 | — |
| 9 | THU-TIOE-ML/Mixtral8_7B_Education_Ornstein | 2026 | 0.502 | — |
| 10 | TheBloke/merlyn-education-corpus-qa-v2-GGUF | 2023 | 0.362 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 23
**Frequent 2-itemsets:** 36
**Frequent 3-itemsets:** 12
**Association rules:** 24

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.323 |
| [Emerging] AND (Very Recent work) | 0.262 |
| (Very Recent work) AND research in Computer Science | 0.192 |
| using Machine Learning AND research in Computer Science | 0.169 |
| [Emerging] AND using Machine Learning | 0.154 |
| [Emerging] AND (Recent work) | 0.152 |
| (Recent work) AND research in Computer Science | 0.151 |
| (Established work) AND research in Computer Science | 0.147 |
| with Positive findings AND [Emerging] | 0.144 |
| [Emerging] AND research in Education | 0.142 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| impact:emerging + topic:mathem | topic:computer science | 0.065 | 0.81 | 1.41 |
| topic:mathematics | topic:computer science | 0.093 | 0.80 | 1.40 |
| topic:education | impact:emerging | 0.142 | 0.85 | 1.39 |
| temporal:very_recent + topic:e | impact:emerging | 0.056 | 0.81 | 1.32 |
| impact:highly_cited | topic:computer science | 0.108 | 0.75 | 1.31 |
| method:machine_learning + temp | topic:computer science | 0.054 | 0.75 | 1.30 |
| method:machine_learning | topic:computer science | 0.169 | 0.74 | 1.29 |
| finding:positive + temporal:ve | impact:emerging | 0.077 | 0.77 | 1.25 |
| impact:emerging + method:machi | topic:computer science | 0.110 | 0.72 | 1.25 |
| method:machine_learning + temp | impact:emerging | 0.070 | 0.74 | 1.21 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 20398
**High-tier pairs:** 297
**Convergence events:** 12

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_002 | 0.311 | 3 | 2y | 3 |
| svw_012 | 0.200 | 2 | 1y | 2 |
| svw_011 | 0.181 | 5 | 8y | 5 |
| svw_001 | 0.171 | 2023 | 61y | 2023 |
| svw_009 | 0.134 | 2 | 2y | 2 |
| svw_010 | 0.055 | 3 | 10y | 3 |
| svw_005 | 0.053 | 2 | 7y | 2 |
| svw_004 | 0.048 | 2 | 8y | 2 |
| svw_003 | 0.046 | 2 | 9y | 2 |
| svw_007 | 0.034 | 2 | 11y | 2 |
| svw_006 | 0.034 | 2 | 12y | 2 |
| svw_008 | 0.027 | 3 | 16y | 3 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Artificial intelligence to deep learning: machine intelligence appr...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Artificial intelligence to deep learning: machine intelli...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `29409efa04ac99ccf01d2a011d21d5d14e870000` (severity: 6)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Molecular Docking: Shifting Paradigms in Drug Discovery' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Molecular Docking: Shifting Paradigms in Drug Discovery
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `8f7948d72b19b3be7191396c5e637cdb14a2371c` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Deep Knowledge Tracing' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Deep Knowledge Tracing
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `fa98d609eb14ce25dd73cd8713a5e284948b4ff4` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Educational data mining and learning analytics: An updated survey' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Educational data mining and learning analytics: An update... + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `7bd598f6a7c6eb4265fe5a9ca64504d1d639684a` (severity: 6)
- **On golden path:** Yes

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'The current landscape of learning analytics in higher education' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: The current landscape of learning analytics in higher edu... + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `17abdcb1da177cefb81d7d76dc801129f1d828f0` (severity: 6)
- **On golden path:** Yes


## 8. Limitations

1. **QEB encoding**: TF-IDF + SVD is a stand-in for transformer-based embeddings (Sentence-BERT). Semantic nuance may be lost, particularly for polysemous terms and domain-specific jargon.

2. **Source coverage**: The Semantic Scholar API provides a subset of published research. Important works outside this index, preprints on non-indexed platforms, and unpublished research are not captured.

3. **Temporal decay calibration**: Parameters (λ=0.12, floor=0.55) are calibrated for general academic literature. Domains with different publication rhythms (e.g., fast-moving ML vs. slow clinical trials) may need domain-specific calibration.

4. **Greedy pathfinding**: The golden token algorithm uses greedy selection at each step. This does not guarantee globally optimal trajectories. Future work: backtracking or beam search.

5. **Abstract-only synthesis**: Gap-bridging proposals are synthesized from abstract text only. Full-text access would enable deeper, more specific synthesis.

6. **Citation completeness**: Citation edges depend on reference list coverage in the Semantic Scholar graph. Missing citations can create false ORPHAN detections.

7. **CONTRADICTS edges**: TF-IDF vectors are non-negative, so cosine similarity cannot detect semantic contradiction. CONTRADICTS edges are inferred from structural patterns, not content analysis.

## 9. Reproducibility

### 9.1 Engine Configuration

| Parameter | Value |
|-----------|-------|
| Engine version | 0.3.0-prototype |
| Total sources | 3118 |
| Timestamp | 2026-04-04T04:37:16.241081 |
| Embedding dim | 256 |
| TF-IDF features | 5,000 |
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