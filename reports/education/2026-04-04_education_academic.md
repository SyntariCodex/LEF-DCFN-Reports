# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3119

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 3119 |
| Graph Nodes | 3136 |
| Graph Edges | 7342 |
| Knowledge Gaps (total) | 3109 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 27 |
| Convergence Events | 13 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3119

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
| Partially grounded (0.4–0.7) | 1916 |
| Weakly grounded (0.2–0.4) | 65 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.697** |

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
| LOW threshold | < 0.4601592546122725 (30th percentile) |
| HIGH threshold | ≥ 0.4992780638743476 (80th percentile) |
| Concentration p25/p50/p75 | 0.4910486139653215 / 0.5351543539027033 / 0.5922945180434553 |
| Distinctiveness p25/p50/p75 | 0.6519776652695525 / 0.6937343003320651 / 0.7412925435508686 |
| Stability p25/p50/p75 | 0.2637405235807041 / 0.2812825280402143 / 0.2974679182800183 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3136 |
|   — CONCEPT | 17 |
|   — DOCUMENT | 3119 |
| Total Edges | 7342 |
|   — CONTAINS | 4208 |
|   — MIRRORS | 1825 |
|   — ENABLES | 825 |
|   — EXTENDS | 412 |
|   — DEPENDS_ON | 72 |
| Density | 0.000747 |
| Connected Components | 344 |

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

**Total entropy nodes:** 3109
**Critical (≥7):** 0 | **High (5-6):** 939 | **Low (<5):** 2170

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3109 |
| STALE | 3019 |
| ORPHAN | 340 |

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
| 9 | Artificial intelligence in cancer target iden | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Utilising learning analytics to support study | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Artificial intelligence in drug discovery: re | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | A Comparison of Undersampling, Oversampling,  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Revolutionizing Medicinal Chemistry: The Appl | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Deep Docking: A Deep Learning Platform for Au | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Addressing two problems in deep knowledge tra | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Multimodal Data Fusion in Learning Analytics: | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Learning Analytics for Learning Design: A Sys | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 27 total (7 emerging, 20 established)
**Structural mirrors:** 240

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Artificial intelligence to deep learning: machine  | 109 | Established | 2019.6 |
| The PRISMA 2020 statement: an updated guideline fo | 2121 | Established | 2018.6 |
| Accelerated discovery of stable lead-free hybrid o | 2 | Established | 2018.0 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 301 | Established | 2018.9 |
| Adaptive e-learning systems through learning style | 2 | Established | 2020.0 |
| Next challenges for adaptive learning systems | 2 | Established | 2015.0 |
| The promise of competency-based education in the h | 127 | Established | 2018.0 |
| Revisiting education reform in Kenya: A case of Co | 5 | Established | 2019.5 |
| An Intelligent Prediction System for Educational D | 2 | Established | 2020.5 |
| Development of a machine learning-based tool to ev | 3 | Emerging | 2022.7 |
| Recovering Concept Prerequisite Relations from Uni | 2 | Established | 2019.0 |
| Deep Neural Network-Based Prediction and Early War | 2 | Established | 2021.0 |
| ContextKT: A Context-Based Method for Knowledge Tr | 2 | Emerging | 2023.0 |
| Designing School Health Services to Provide Multi- | 2 | Emerging | 2023.5 |
| Issues in Statewide Scale up of a Multi-Tiered Sys | 2 | Emerging | 2023.0 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Artificial intelligence to deep lea | The PRISMA 2020 statement: an updat | 0.61 |
| Artificial intelligence to deep lea | Accelerated discovery of stable lea | 0.49 |
| Artificial intelligence to deep lea | VoiceOfML/CMLMUF-Education-And-Hist | 0.87 |
| Artificial intelligence to deep lea | Adaptive e-learning systems through | 0.42 |
| Artificial intelligence to deep lea | Next challenges for adaptive learni | 0.42 |
| Artificial intelligence to deep lea | The promise of competency-based edu | 1.00 |
| Artificial intelligence to deep lea | Revisiting education reform in Keny | 0.69 |
| Artificial intelligence to deep lea | An Intelligent Prediction System fo | 0.42 |
| Artificial intelligence to deep lea | Recovering Concept Prerequisite Rel | 0.42 |
| Artificial intelligence to deep lea | Deep Neural Network-Based Predictio | 0.42 |
| Artificial intelligence to deep lea | Designing School Health Services to | 0.42 |
| Artificial intelligence to deep lea | Handbook of treatment for eating di | 0.86 |
| Artificial intelligence to deep lea | Evaluating English language learner | 0.83 |
| Artificial intelligence to deep lea | Unearthing People from the SaND: Re | 0.49 |
| Artificial intelligence to deep lea | Human Circulating and Tissue-Reside | 0.89 |
| Artificial intelligence to deep lea | The Relationship between Vocabulary | 0.91 |
| Artificial intelligence to deep lea | The Handbook of School Psychology | 0.42 |
| Artificial intelligence to deep lea | Complexity in Mathematics Education | 0.83 |
| Artificial intelligence to deep lea | Discovery of the Einsteinium Isotop | 0.44 |
| Artificial intelligence to deep lea | processing/p5.js: p5.js is a client | 0.71 |
| Artificial intelligence to deep lea | Skyemou5/Pysoma: A crossplatform Ho | 0.49 |
| The PRISMA 2020 statement: an updat | Accelerated discovery of stable lea | 0.97 |
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.89 |
| The PRISMA 2020 statement: an updat | Adaptive e-learning systems through | 0.83 |
| The PRISMA 2020 statement: an updat | Next challenges for adaptive learni | 0.83 |
| The PRISMA 2020 statement: an updat | The promise of competency-based edu | 0.54 |
| The PRISMA 2020 statement: an updat | Revisiting education reform in Keny | 0.97 |
| The PRISMA 2020 statement: an updat | An Intelligent Prediction System fo | 0.83 |
| The PRISMA 2020 statement: an updat | Recovering Concept Prerequisite Rel | 0.83 |
| The PRISMA 2020 statement: an updat | Deep Neural Network-Based Predictio | 0.83 |
| The PRISMA 2020 statement: an updat | Designing School Health Services to | 0.83 |
| The PRISMA 2020 statement: an updat | Handbook of treatment for eating di | 0.89 |
| The PRISMA 2020 statement: an updat | Evaluating English language learner | 0.92 |
| The PRISMA 2020 statement: an updat | Unearthing People from the SaND: Re | 0.97 |
| The PRISMA 2020 statement: an updat | Human Circulating and Tissue-Reside | 0.88 |
| The PRISMA 2020 statement: an updat | The Relationship between Vocabulary | 0.85 |
| The PRISMA 2020 statement: an updat | The Handbook of School Psychology | 0.83 |
| The PRISMA 2020 statement: an updat | Complexity in Mathematics Education | 0.92 |
| The PRISMA 2020 statement: an updat | Discovery of the Einsteinium Isotop | 0.87 |
| The PRISMA 2020 statement: an updat | Skyemou5/Pysoma: A crossplatform Ho | 0.97 |
| Accelerated discovery of stable lea | VoiceOfML/CMLMUF-Education-And-Hist | 0.85 |
| Accelerated discovery of stable lea | Adaptive e-learning systems through | 0.71 |
| Accelerated discovery of stable lea | Next challenges for adaptive learni | 0.71 |
| Accelerated discovery of stable lea | The promise of competency-based edu | 0.41 |
| Accelerated discovery of stable lea | Revisiting education reform in Keny | 0.97 |
| Accelerated discovery of stable lea | An Intelligent Prediction System fo | 0.71 |
| Accelerated discovery of stable lea | Recovering Concept Prerequisite Rel | 0.71 |
| Accelerated discovery of stable lea | Deep Neural Network-Based Predictio | 0.71 |
| Accelerated discovery of stable lea | Designing School Health Services to | 0.71 |
| Accelerated discovery of stable lea | Handbook of treatment for eating di | 0.85 |
| Accelerated discovery of stable lea | Evaluating English language learner | 0.89 |
| Accelerated discovery of stable lea | Unearthing People from the SaND: Re | 1.00 |
| Accelerated discovery of stable lea | Human Circulating and Tissue-Reside | 0.83 |
| Accelerated discovery of stable lea | The Relationship between Vocabulary | 0.80 |
| Accelerated discovery of stable lea | The Handbook of School Psychology | 0.71 |
| Accelerated discovery of stable lea | Complexity in Mathematics Education | 0.89 |
| Accelerated discovery of stable lea | Discovery of the Einsteinium Isotop | 0.89 |
| Accelerated discovery of stable lea | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Adaptive e-learning systems through | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Next challenges for adaptive learni | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | The promise of competency-based edu | 0.82 |
| VoiceOfML/CMLMUF-Education-And-Hist | Revisiting education reform in Keny | 0.95 |
| VoiceOfML/CMLMUF-Education-And-Hist | An Intelligent Prediction System fo | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Recovering Concept Prerequisite Rel | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Deep Neural Network-Based Predictio | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Designing School Health Services to | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Handbook of treatment for eating di | 0.99 |
| VoiceOfML/CMLMUF-Education-And-Hist | Evaluating English language learner | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Unearthing People from the SaND: Re | 0.85 |
| VoiceOfML/CMLMUF-Education-And-Hist | Human Circulating and Tissue-Reside | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | The Relationship between Vocabulary | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | The Handbook of School Psychology | 0.61 |
| VoiceOfML/CMLMUF-Education-And-Hist | Complexity in Mathematics Education | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Discovery of the Einsteinium Isotop | 0.77 |
| VoiceOfML/CMLMUF-Education-And-Hist | processing/p5.js: p5.js is a client | 0.54 |
| VoiceOfML/CMLMUF-Education-And-Hist | Skyemou5/Pysoma: A crossplatform Ho | 0.85 |
| Adaptive e-learning systems through | Next challenges for adaptive learni | 1.00 |
| Adaptive e-learning systems through | Revisiting education reform in Keny | 0.69 |
| Adaptive e-learning systems through | An Intelligent Prediction System fo | 1.00 |
| Adaptive e-learning systems through | Development of a machine learning-b | 0.71 |
| Adaptive e-learning systems through | Recovering Concept Prerequisite Rel | 1.00 |
| Adaptive e-learning systems through | Deep Neural Network-Based Predictio | 1.00 |
| Adaptive e-learning systems through | ContextKT: A Context-Based Method f | 0.71 |
| Adaptive e-learning systems through | Designing School Health Services to | 1.00 |
| Adaptive e-learning systems through | Issues in Statewide Scale up of a M | 0.71 |
| Adaptive e-learning systems through | Handbook of treatment for eating di | 0.60 |
| Adaptive e-learning systems through | Evaluating English language learner | 0.63 |
| Adaptive e-learning systems through | Unearthing People from the SaND: Re | 0.71 |
| Adaptive e-learning systems through | Human Circulating and Tissue-Reside | 0.59 |
| Adaptive e-learning systems through | The Relationship between Vocabulary | 0.57 |
| Adaptive e-learning systems through | The Handbook of School Psychology | 1.00 |
| Adaptive e-learning systems through | Complexity in Mathematics Education | 0.63 |
| Adaptive e-learning systems through | Discovery of the Einsteinium Isotop | 0.63 |
| Adaptive e-learning systems through | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Next challenges for adaptive learni | Revisiting education reform in Keny | 0.69 |
| Next challenges for adaptive learni | An Intelligent Prediction System fo | 1.00 |
| Next challenges for adaptive learni | Development of a machine learning-b | 0.71 |
| Next challenges for adaptive learni | Recovering Concept Prerequisite Rel | 1.00 |
| Next challenges for adaptive learni | Deep Neural Network-Based Predictio | 1.00 |
| Next challenges for adaptive learni | ContextKT: A Context-Based Method f | 0.71 |
| Next challenges for adaptive learni | Designing School Health Services to | 1.00 |
| Next challenges for adaptive learni | Issues in Statewide Scale up of a M | 0.71 |
| Next challenges for adaptive learni | Handbook of treatment for eating di | 0.60 |
| Next challenges for adaptive learni | Evaluating English language learner | 0.63 |
| Next challenges for adaptive learni | Unearthing People from the SaND: Re | 0.71 |
| Next challenges for adaptive learni | Human Circulating and Tissue-Reside | 0.59 |
| Next challenges for adaptive learni | The Relationship between Vocabulary | 0.57 |
| Next challenges for adaptive learni | The Handbook of School Psychology | 1.00 |
| Next challenges for adaptive learni | Complexity in Mathematics Education | 0.63 |
| Next challenges for adaptive learni | Discovery of the Einsteinium Isotop | 0.63 |
| Next challenges for adaptive learni | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| The promise of competency-based edu | Revisiting education reform in Keny | 0.62 |
| The promise of competency-based edu | Handbook of treatment for eating di | 0.80 |
| The promise of competency-based edu | Evaluating English language learner | 0.77 |
| The promise of competency-based edu | Unearthing People from the SaND: Re | 0.41 |
| The promise of competency-based edu | Human Circulating and Tissue-Reside | 0.84 |
| The promise of competency-based edu | The Relationship between Vocabulary | 0.87 |
| The promise of competency-based edu | Complexity in Mathematics Education | 0.77 |
| The promise of competency-based edu | processing/p5.js: p5.js is a client | 0.73 |
| The promise of competency-based edu | Skyemou5/Pysoma: A crossplatform Ho | 0.41 |
| Revisiting education reform in Keny | An Intelligent Prediction System fo | 0.69 |
| Revisiting education reform in Keny | Recovering Concept Prerequisite Rel | 0.69 |
| Revisiting education reform in Keny | Deep Neural Network-Based Predictio | 0.69 |
| Revisiting education reform in Keny | Designing School Health Services to | 0.69 |
| Revisiting education reform in Keny | Handbook of treatment for eating di | 0.94 |
| Revisiting education reform in Keny | Evaluating English language learner | 0.98 |
| Revisiting education reform in Keny | Unearthing People from the SaND: Re | 0.97 |
| Revisiting education reform in Keny | Human Circulating and Tissue-Reside | 0.94 |
| Revisiting education reform in Keny | The Relationship between Vocabulary | 0.92 |
| Revisiting education reform in Keny | The Handbook of School Psychology | 0.69 |
| Revisiting education reform in Keny | Complexity in Mathematics Education | 0.98 |
| Revisiting education reform in Keny | Discovery of the Einsteinium Isotop | 0.87 |
| Revisiting education reform in Keny | Skyemou5/Pysoma: A crossplatform Ho | 0.97 |
| An Intelligent Prediction System fo | Development of a machine learning-b | 0.71 |
| An Intelligent Prediction System fo | Recovering Concept Prerequisite Rel | 1.00 |
| An Intelligent Prediction System fo | Deep Neural Network-Based Predictio | 1.00 |
| An Intelligent Prediction System fo | ContextKT: A Context-Based Method f | 0.71 |
| An Intelligent Prediction System fo | Designing School Health Services to | 1.00 |
| An Intelligent Prediction System fo | Issues in Statewide Scale up of a M | 0.71 |
| An Intelligent Prediction System fo | Handbook of treatment for eating di | 0.60 |
| An Intelligent Prediction System fo | Evaluating English language learner | 0.63 |
| An Intelligent Prediction System fo | Unearthing People from the SaND: Re | 0.71 |
| An Intelligent Prediction System fo | Human Circulating and Tissue-Reside | 0.59 |
| An Intelligent Prediction System fo | The Relationship between Vocabulary | 0.57 |
| An Intelligent Prediction System fo | The Handbook of School Psychology | 1.00 |
| An Intelligent Prediction System fo | Complexity in Mathematics Education | 0.63 |
| An Intelligent Prediction System fo | Discovery of the Einsteinium Isotop | 0.63 |
| An Intelligent Prediction System fo | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Development of a machine learning-b | Recovering Concept Prerequisite Rel | 0.71 |
| Development of a machine learning-b | Deep Neural Network-Based Predictio | 0.71 |
| Development of a machine learning-b | ContextKT: A Context-Based Method f | 1.00 |
| Development of a machine learning-b | Designing School Health Services to | 0.71 |
| Development of a machine learning-b | Issues in Statewide Scale up of a M | 1.00 |
| Development of a machine learning-b | The Handbook of School Psychology | 0.71 |
| Recovering Concept Prerequisite Rel | Deep Neural Network-Based Predictio | 1.00 |
| Recovering Concept Prerequisite Rel | ContextKT: A Context-Based Method f | 0.71 |
| Recovering Concept Prerequisite Rel | Designing School Health Services to | 1.00 |
| Recovering Concept Prerequisite Rel | Issues in Statewide Scale up of a M | 0.71 |
| Recovering Concept Prerequisite Rel | Handbook of treatment for eating di | 0.60 |
| Recovering Concept Prerequisite Rel | Evaluating English language learner | 0.63 |
| Recovering Concept Prerequisite Rel | Unearthing People from the SaND: Re | 0.71 |
| Recovering Concept Prerequisite Rel | Human Circulating and Tissue-Reside | 0.59 |
| Recovering Concept Prerequisite Rel | The Relationship between Vocabulary | 0.57 |
| Recovering Concept Prerequisite Rel | The Handbook of School Psychology | 1.00 |
| Recovering Concept Prerequisite Rel | Complexity in Mathematics Education | 0.63 |
| Recovering Concept Prerequisite Rel | Discovery of the Einsteinium Isotop | 0.63 |
| Recovering Concept Prerequisite Rel | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Deep Neural Network-Based Predictio | ContextKT: A Context-Based Method f | 0.71 |
| Deep Neural Network-Based Predictio | Designing School Health Services to | 1.00 |
| Deep Neural Network-Based Predictio | Issues in Statewide Scale up of a M | 0.71 |
| Deep Neural Network-Based Predictio | Handbook of treatment for eating di | 0.60 |
| Deep Neural Network-Based Predictio | Evaluating English language learner | 0.63 |
| Deep Neural Network-Based Predictio | Unearthing People from the SaND: Re | 0.71 |
| Deep Neural Network-Based Predictio | Human Circulating and Tissue-Reside | 0.59 |
| Deep Neural Network-Based Predictio | The Relationship between Vocabulary | 0.57 |
| Deep Neural Network-Based Predictio | The Handbook of School Psychology | 1.00 |
| Deep Neural Network-Based Predictio | Complexity in Mathematics Education | 0.63 |
| Deep Neural Network-Based Predictio | Discovery of the Einsteinium Isotop | 0.63 |
| Deep Neural Network-Based Predictio | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| ContextKT: A Context-Based Method f | Designing School Health Services to | 0.71 |
| ContextKT: A Context-Based Method f | Issues in Statewide Scale up of a M | 1.00 |
| ContextKT: A Context-Based Method f | The Handbook of School Psychology | 0.71 |
| Designing School Health Services to | Issues in Statewide Scale up of a M | 0.71 |
| Designing School Health Services to | Handbook of treatment for eating di | 0.60 |
| Designing School Health Services to | Evaluating English language learner | 0.63 |
| Designing School Health Services to | Unearthing People from the SaND: Re | 0.71 |
| Designing School Health Services to | Human Circulating and Tissue-Reside | 0.59 |
| Designing School Health Services to | The Relationship between Vocabulary | 0.57 |
| Designing School Health Services to | The Handbook of School Psychology | 1.00 |
| Designing School Health Services to | Complexity in Mathematics Education | 0.63 |
| Designing School Health Services to | Discovery of the Einsteinium Isotop | 0.63 |
| Designing School Health Services to | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Issues in Statewide Scale up of a M | The Handbook of School Psychology | 0.71 |
| Handbook of treatment for eating di | Evaluating English language learner | 0.98 |
| Handbook of treatment for eating di | Unearthing People from the SaND: Re | 0.85 |
| Handbook of treatment for eating di | Human Circulating and Tissue-Reside | 0.98 |
| Handbook of treatment for eating di | The Relationship between Vocabulary | 0.98 |
| Handbook of treatment for eating di | The Handbook of School Psychology | 0.60 |
| Handbook of treatment for eating di | Complexity in Mathematics Education | 0.98 |
| Handbook of treatment for eating di | Discovery of the Einsteinium Isotop | 0.83 |
| Handbook of treatment for eating di | processing/p5.js: p5.js is a client | 0.63 |
| Handbook of treatment for eating di | Skyemou5/Pysoma: A crossplatform Ho | 0.85 |
| Evaluating English language learner | Unearthing People from the SaND: Re | 0.89 |
| Evaluating English language learner | Human Circulating and Tissue-Reside | 0.99 |
| Evaluating English language learner | The Relationship between Vocabulary | 0.98 |
| Evaluating English language learner | The Handbook of School Psychology | 0.63 |
| Evaluating English language learner | Complexity in Mathematics Education | 1.00 |
| Evaluating English language learner | Discovery of the Einsteinium Isotop | 0.80 |
| Evaluating English language learner | processing/p5.js: p5.js is a client | 0.48 |
| Evaluating English language learner | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Unearthing People from the SaND: Re | Human Circulating and Tissue-Reside | 0.83 |
| Unearthing People from the SaND: Re | The Relationship between Vocabulary | 0.80 |
| Unearthing People from the SaND: Re | The Handbook of School Psychology | 0.71 |
| Unearthing People from the SaND: Re | Complexity in Mathematics Education | 0.89 |
| Unearthing People from the SaND: Re | Discovery of the Einsteinium Isotop | 0.89 |
| Unearthing People from the SaND: Re | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| Human Circulating and Tissue-Reside | The Relationship between Vocabulary | 1.00 |
| Human Circulating and Tissue-Reside | The Handbook of School Psychology | 0.59 |
| Human Circulating and Tissue-Reside | Complexity in Mathematics Education | 0.99 |
| Human Circulating and Tissue-Reside | Discovery of the Einsteinium Isotop | 0.74 |
| Human Circulating and Tissue-Reside | processing/p5.js: p5.js is a client | 0.54 |
| Human Circulating and Tissue-Reside | Skyemou5/Pysoma: A crossplatform Ho | 0.83 |
| The Relationship between Vocabulary | The Handbook of School Psychology | 0.57 |
| The Relationship between Vocabulary | Complexity in Mathematics Education | 0.98 |
| The Relationship between Vocabulary | Discovery of the Einsteinium Isotop | 0.72 |
| The Relationship between Vocabulary | processing/p5.js: p5.js is a client | 0.57 |
| The Relationship between Vocabulary | Skyemou5/Pysoma: A crossplatform Ho | 0.80 |
| The Handbook of School Psychology | Complexity in Mathematics Education | 0.63 |
| The Handbook of School Psychology | Discovery of the Einsteinium Isotop | 0.63 |
| The Handbook of School Psychology | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| COVLIAS 1.0: Lung Segmentation in C | The impact of adolescent achievemen | 1.00 |
| COVLIAS 1.0: Lung Segmentation in C | Discovery of the Einsteinium Isotop | 0.45 |
| COVLIAS 1.0: Lung Segmentation in C | processing/p5.js: p5.js is a client | 0.67 |
| The impact of adolescent achievemen | Discovery of the Einsteinium Isotop | 0.45 |
| The impact of adolescent achievemen | processing/p5.js: p5.js is a client | 0.67 |
| Complexity in Mathematics Education | Discovery of the Einsteinium Isotop | 0.80 |
| Complexity in Mathematics Education | processing/p5.js: p5.js is a client | 0.48 |
| Complexity in Mathematics Education | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Discovery of the Einsteinium Isotop | processing/p5.js: p5.js is a client | 0.45 |
| Discovery of the Einsteinium Isotop | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.482
**Confidence:** HIGH
**Entropy nodes resolved:** 7

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
| 1 | A Comparison of Undersampling, Oversampling, and S | 2023 | 0.526 | YES |
| 2 | Computer Science | None | 0.393 | — |
| 3 | Educational data mining: prediction of students' a | 2022 | 0.516 | YES |
| 4 | The current landscape of learning analytics in hig | 2018 | 0.479 | YES |
| 5 | Predicting Student Performance Using Data Mining a | 2020 | 0.498 | YES |
| 6 | Educational data mining and learning analytics: An | 2020 | 0.498 | YES |
| 7 | A Systematic Review of Deep Learning Approaches to | 2019 | 0.316 | — |
| 8 | Educational data mining and learning analytics for | 2019 | 0.488 | YES |
| 9 | Learning analytics in higher education: a preponde | 2021 | 0.271 | — |
| 10 | Utilising learning analytics to support study succ | 2020 | 0.497 | YES |

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
| impact:emerging + topic:mathem | topic:computer science | 0.064 | 0.81 | 1.41 |
| topic:mathematics | topic:computer science | 0.093 | 0.80 | 1.40 |
| topic:education | impact:emerging | 0.142 | 0.85 | 1.39 |
| temporal:very_recent + topic:e | impact:emerging | 0.056 | 0.81 | 1.32 |
| impact:highly_cited | topic:computer science | 0.108 | 0.75 | 1.31 |
| method:machine_learning + temp | topic:computer science | 0.053 | 0.75 | 1.30 |
| method:machine_learning | topic:computer science | 0.169 | 0.74 | 1.28 |
| impact:emerging + method:machi | topic:computer science | 0.110 | 0.72 | 1.25 |
| finding:positive + temporal:ve | impact:emerging | 0.077 | 0.76 | 1.25 |
| method:machine_learning + temp | impact:emerging | 0.070 | 0.74 | 1.21 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 20405
**High-tier pairs:** 300
**Convergence events:** 13

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_010 | 0.206 | 2 | 2y | 2 |
| svw_008 | 0.201 | 3 | 3y | 3 |
| svw_011 | 0.195 | 2 | 2y | 2 |
| svw_001 | 0.170 | 2007 | 61y | 2007 |
| svw_003 | 0.148 | 5 | 18y | 5 |
| svw_013 | 0.059 | 2 | 6y | 2 |
| svw_006 | 0.052 | 4 | 10y | 4 |
| svw_012 | 0.052 | 2 | 7y | 2 |
| svw_002 | 0.047 | 2 | 8y | 2 |
| svw_007 | 0.045 | 2 | 11y | 2 |
| svw_005 | 0.044 | 2 | 10y | 2 |
| svw_009 | 0.037 | 2 | 11y | 2 |
| svw_004 | 0.018 | 2 | 22y | 2 |

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
| Total sources | 3119 |
| Timestamp | 2026-04-04T02:51:44.374347 |
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