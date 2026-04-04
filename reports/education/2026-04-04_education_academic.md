# DCFN Technical Report: Education & EdTech

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3120

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Education & EdTech |
| Sources Analyzed | 3120 |
| Graph Nodes | 3137 |
| Graph Edges | 7331 |
| Knowledge Gaps (total) | 3110 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 25 |
| Convergence Events | 15 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3120

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
| LOW threshold | < 0.46050519268080464 (30th percentile) |
| HIGH threshold | ≥ 0.4992487640047231 (80th percentile) |
| Concentration p25/p50/p75 | 0.4917023142702343 / 0.5340590016724573 / 0.5929042625040722 |
| Distinctiveness p25/p50/p75 | 0.6517464077848157 / 0.6941701450006017 / 0.7418608056038299 |
| Stability p25/p50/p75 | 0.265165961915117 / 0.2811667926556693 / 0.2974426695605491 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3137 |
|   — CONCEPT | 17 |
|   — DOCUMENT | 3120 |
| Total Edges | 7331 |
|   — CONTAINS | 4211 |
|   — MIRRORS | 1827 |
|   — ENABLES | 828 |
|   — EXTENDS | 394 |
|   — DEPENDS_ON | 71 |
| Density | 0.000745 |
| Connected Components | 345 |

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

**Total entropy nodes:** 3110
**Critical (≥7):** 0 | **High (5-6):** 957 | **Low (<5):** 2153

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3110 |
| STALE | 3020 |
| ORPHAN | 341 |

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
| 10 | Predicting Student Performance Using Data Min | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | QSAR-Based Virtual Screening: Advances and Ap | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Educational data mining and learning analytic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Revolutionizing Medicinal Chemistry: The Appl | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Addressing two problems in deep knowledge tra | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Multimodal Data Fusion in Learning Analytics: | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Learning Analytics for Learning Design: A Sys | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | A Systematic Review of Empirical Studies on L | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | A Systematic Review of Deep Learning Approach | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | A Core Components Framework for Evaluating Im | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Educational data mining: Predictive analysis  | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 25 total (7 emerging, 18 established)
**Structural mirrors:** 198

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Molecular Docking: Shifting Paradigms in Drug Disc | 120 | Established | 2020.0 |
| The PRISMA 2020 statement: an updated guideline fo | 2119 | Established | 2018.5 |
| Accelerated discovery of stable lead-free hybrid o | 2 | Established | 2018.0 |
| VoiceOfML/CMLMUF-Education-And-History (dataset) | 292 | Established | 2019.0 |
| Adaptive e-learning systems through learning style | 2 | Established | 2020.0 |
| Next challenges for adaptive learning systems | 2 | Established | 2015.0 |
| The promise of competency-based education in the h | 134 | Established | 2017.9 |
| Revisiting education reform in Kenya: A case of Co | 4 | Established | 2019.0 |
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
| Molecular Docking: Shifting Paradig | The PRISMA 2020 statement: an updat | 0.61 |
| Molecular Docking: Shifting Paradig | Accelerated discovery of stable lea | 0.50 |
| Molecular Docking: Shifting Paradig | VoiceOfML/CMLMUF-Education-And-Hist | 0.86 |
| Molecular Docking: Shifting Paradig | Adaptive e-learning systems through | 0.41 |
| Molecular Docking: Shifting Paradig | Next challenges for adaptive learni | 0.41 |
| Molecular Docking: Shifting Paradig | The promise of competency-based edu | 0.99 |
| Molecular Docking: Shifting Paradig | Revisiting education reform in Keny | 0.50 |
| Molecular Docking: Shifting Paradig | An Intelligent Prediction System fo | 0.41 |
| Molecular Docking: Shifting Paradig | Recovering Concept Prerequisite Rel | 0.41 |
| Molecular Docking: Shifting Paradig | Deep Neural Network-Based Predictio | 0.41 |
| Molecular Docking: Shifting Paradig | Designing School Health Services to | 0.41 |
| Molecular Docking: Shifting Paradig | How Should DSM-V Criteria for Schiz | 0.87 |
| Molecular Docking: Shifting Paradig | Evaluating English language learner | 0.83 |
| Molecular Docking: Shifting Paradig | Unearthing People from the SaND: Re | 0.50 |
| Molecular Docking: Shifting Paradig | Confronting the Challenges of Parti | 0.83 |
| Molecular Docking: Shifting Paradig | A Benchmark to Select Data Mining B | 0.83 |
| Molecular Docking: Shifting Paradig | Discovery of the Mercury Isotopes | 0.44 |
| Molecular Docking: Shifting Paradig | processing/p5.js: p5.js is a client | 0.72 |
| Molecular Docking: Shifting Paradig | Skyemou5/Pysoma: A crossplatform Ho | 0.50 |
| The PRISMA 2020 statement: an updat | Accelerated discovery of stable lea | 0.97 |
| The PRISMA 2020 statement: an updat | VoiceOfML/CMLMUF-Education-And-Hist | 0.90 |
| The PRISMA 2020 statement: an updat | Adaptive e-learning systems through | 0.83 |
| The PRISMA 2020 statement: an updat | Next challenges for adaptive learni | 0.83 |
| The PRISMA 2020 statement: an updat | The promise of competency-based edu | 0.54 |
| The PRISMA 2020 statement: an updat | Revisiting education reform in Keny | 0.97 |
| The PRISMA 2020 statement: an updat | An Intelligent Prediction System fo | 0.83 |
| The PRISMA 2020 statement: an updat | Recovering Concept Prerequisite Rel | 0.83 |
| The PRISMA 2020 statement: an updat | Deep Neural Network-Based Predictio | 0.83 |
| The PRISMA 2020 statement: an updat | Designing School Health Services to | 0.83 |
| The PRISMA 2020 statement: an updat | How Should DSM-V Criteria for Schiz | 0.88 |
| The PRISMA 2020 statement: an updat | Evaluating English language learner | 0.92 |
| The PRISMA 2020 statement: an updat | Unearthing People from the SaND: Re | 0.97 |
| The PRISMA 2020 statement: an updat | Confronting the Challenges of Parti | 0.92 |
| The PRISMA 2020 statement: an updat | A Benchmark to Select Data Mining B | 0.92 |
| The PRISMA 2020 statement: an updat | Discovery of the Mercury Isotopes | 0.87 |
| The PRISMA 2020 statement: an updat | Skyemou5/Pysoma: A crossplatform Ho | 0.97 |
| Accelerated discovery of stable lea | VoiceOfML/CMLMUF-Education-And-Hist | 0.86 |
| Accelerated discovery of stable lea | Adaptive e-learning systems through | 0.71 |
| Accelerated discovery of stable lea | Next challenges for adaptive learni | 0.71 |
| Accelerated discovery of stable lea | The promise of competency-based edu | 0.41 |
| Accelerated discovery of stable lea | Revisiting education reform in Keny | 1.00 |
| Accelerated discovery of stable lea | An Intelligent Prediction System fo | 0.71 |
| Accelerated discovery of stable lea | Recovering Concept Prerequisite Rel | 0.71 |
| Accelerated discovery of stable lea | Deep Neural Network-Based Predictio | 0.71 |
| Accelerated discovery of stable lea | Designing School Health Services to | 0.71 |
| Accelerated discovery of stable lea | How Should DSM-V Criteria for Schiz | 0.83 |
| Accelerated discovery of stable lea | Evaluating English language learner | 0.89 |
| Accelerated discovery of stable lea | Unearthing People from the SaND: Re | 1.00 |
| Accelerated discovery of stable lea | Confronting the Challenges of Parti | 0.89 |
| Accelerated discovery of stable lea | A Benchmark to Select Data Mining B | 0.89 |
| Accelerated discovery of stable lea | Discovery of the Mercury Isotopes | 0.89 |
| Accelerated discovery of stable lea | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Adaptive e-learning systems through | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | Next challenges for adaptive learni | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | The promise of competency-based edu | 0.81 |
| VoiceOfML/CMLMUF-Education-And-Hist | Revisiting education reform in Keny | 0.86 |
| VoiceOfML/CMLMUF-Education-And-Hist | An Intelligent Prediction System fo | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | Recovering Concept Prerequisite Rel | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | Deep Neural Network-Based Predictio | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | Designing School Health Services to | 0.62 |
| VoiceOfML/CMLMUF-Education-And-Hist | How Should DSM-V Criteria for Schiz | 0.99 |
| VoiceOfML/CMLMUF-Education-And-Hist | Evaluating English language learner | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Unearthing People from the SaND: Re | 0.86 |
| VoiceOfML/CMLMUF-Education-And-Hist | Confronting the Challenges of Parti | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | A Benchmark to Select Data Mining B | 1.00 |
| VoiceOfML/CMLMUF-Education-And-Hist | Discovery of the Mercury Isotopes | 0.78 |
| VoiceOfML/CMLMUF-Education-And-Hist | processing/p5.js: p5.js is a client | 0.53 |
| VoiceOfML/CMLMUF-Education-And-Hist | Skyemou5/Pysoma: A crossplatform Ho | 0.86 |
| Adaptive e-learning systems through | Next challenges for adaptive learni | 1.00 |
| Adaptive e-learning systems through | Revisiting education reform in Keny | 0.71 |
| Adaptive e-learning systems through | An Intelligent Prediction System fo | 1.00 |
| Adaptive e-learning systems through | Development of a machine learning-b | 0.71 |
| Adaptive e-learning systems through | Recovering Concept Prerequisite Rel | 1.00 |
| Adaptive e-learning systems through | Deep Neural Network-Based Predictio | 1.00 |
| Adaptive e-learning systems through | ContextKT: A Context-Based Method f | 0.71 |
| Adaptive e-learning systems through | Designing School Health Services to | 1.00 |
| Adaptive e-learning systems through | Issues in Statewide Scale up of a M | 0.71 |
| Adaptive e-learning systems through | How Should DSM-V Criteria for Schiz | 0.59 |
| Adaptive e-learning systems through | Evaluating English language learner | 0.63 |
| Adaptive e-learning systems through | Unearthing People from the SaND: Re | 0.71 |
| Adaptive e-learning systems through | Confronting the Challenges of Parti | 0.63 |
| Adaptive e-learning systems through | A Benchmark to Select Data Mining B | 0.63 |
| Adaptive e-learning systems through | Discovery of the Mercury Isotopes | 0.63 |
| Adaptive e-learning systems through | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Next challenges for adaptive learni | Revisiting education reform in Keny | 0.71 |
| Next challenges for adaptive learni | An Intelligent Prediction System fo | 1.00 |
| Next challenges for adaptive learni | Development of a machine learning-b | 0.71 |
| Next challenges for adaptive learni | Recovering Concept Prerequisite Rel | 1.00 |
| Next challenges for adaptive learni | Deep Neural Network-Based Predictio | 1.00 |
| Next challenges for adaptive learni | ContextKT: A Context-Based Method f | 0.71 |
| Next challenges for adaptive learni | Designing School Health Services to | 1.00 |
| Next challenges for adaptive learni | Issues in Statewide Scale up of a M | 0.71 |
| Next challenges for adaptive learni | How Should DSM-V Criteria for Schiz | 0.59 |
| Next challenges for adaptive learni | Evaluating English language learner | 0.63 |
| Next challenges for adaptive learni | Unearthing People from the SaND: Re | 0.71 |
| Next challenges for adaptive learni | Confronting the Challenges of Parti | 0.63 |
| Next challenges for adaptive learni | A Benchmark to Select Data Mining B | 0.63 |
| Next challenges for adaptive learni | Discovery of the Mercury Isotopes | 0.63 |
| Next challenges for adaptive learni | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| The promise of competency-based edu | Revisiting education reform in Keny | 0.41 |
| The promise of competency-based edu | How Should DSM-V Criteria for Schiz | 0.82 |
| The promise of competency-based edu | Evaluating English language learner | 0.77 |
| The promise of competency-based edu | Unearthing People from the SaND: Re | 0.41 |
| The promise of competency-based edu | Confronting the Challenges of Parti | 0.77 |
| The promise of competency-based edu | A Benchmark to Select Data Mining B | 0.77 |
| The promise of competency-based edu | processing/p5.js: p5.js is a client | 0.74 |
| The promise of competency-based edu | Skyemou5/Pysoma: A crossplatform Ho | 0.41 |
| Revisiting education reform in Keny | An Intelligent Prediction System fo | 0.71 |
| Revisiting education reform in Keny | Recovering Concept Prerequisite Rel | 0.71 |
| Revisiting education reform in Keny | Deep Neural Network-Based Predictio | 0.71 |
| Revisiting education reform in Keny | Designing School Health Services to | 0.71 |
| Revisiting education reform in Keny | How Should DSM-V Criteria for Schiz | 0.83 |
| Revisiting education reform in Keny | Evaluating English language learner | 0.89 |
| Revisiting education reform in Keny | Unearthing People from the SaND: Re | 1.00 |
| Revisiting education reform in Keny | Confronting the Challenges of Parti | 0.89 |
| Revisiting education reform in Keny | A Benchmark to Select Data Mining B | 0.89 |
| Revisiting education reform in Keny | Discovery of the Mercury Isotopes | 0.89 |
| Revisiting education reform in Keny | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| An Intelligent Prediction System fo | Development of a machine learning-b | 0.71 |
| An Intelligent Prediction System fo | Recovering Concept Prerequisite Rel | 1.00 |
| An Intelligent Prediction System fo | Deep Neural Network-Based Predictio | 1.00 |
| An Intelligent Prediction System fo | ContextKT: A Context-Based Method f | 0.71 |
| An Intelligent Prediction System fo | Designing School Health Services to | 1.00 |
| An Intelligent Prediction System fo | Issues in Statewide Scale up of a M | 0.71 |
| An Intelligent Prediction System fo | How Should DSM-V Criteria for Schiz | 0.59 |
| An Intelligent Prediction System fo | Evaluating English language learner | 0.63 |
| An Intelligent Prediction System fo | Unearthing People from the SaND: Re | 0.71 |
| An Intelligent Prediction System fo | Confronting the Challenges of Parti | 0.63 |
| An Intelligent Prediction System fo | A Benchmark to Select Data Mining B | 0.63 |
| An Intelligent Prediction System fo | Discovery of the Mercury Isotopes | 0.63 |
| An Intelligent Prediction System fo | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Development of a machine learning-b | Recovering Concept Prerequisite Rel | 0.71 |
| Development of a machine learning-b | Deep Neural Network-Based Predictio | 0.71 |
| Development of a machine learning-b | ContextKT: A Context-Based Method f | 1.00 |
| Development of a machine learning-b | Designing School Health Services to | 0.71 |
| Development of a machine learning-b | Issues in Statewide Scale up of a M | 1.00 |
| Recovering Concept Prerequisite Rel | Deep Neural Network-Based Predictio | 1.00 |
| Recovering Concept Prerequisite Rel | ContextKT: A Context-Based Method f | 0.71 |
| Recovering Concept Prerequisite Rel | Designing School Health Services to | 1.00 |
| Recovering Concept Prerequisite Rel | Issues in Statewide Scale up of a M | 0.71 |
| Recovering Concept Prerequisite Rel | How Should DSM-V Criteria for Schiz | 0.59 |
| Recovering Concept Prerequisite Rel | Evaluating English language learner | 0.63 |
| Recovering Concept Prerequisite Rel | Unearthing People from the SaND: Re | 0.71 |
| Recovering Concept Prerequisite Rel | Confronting the Challenges of Parti | 0.63 |
| Recovering Concept Prerequisite Rel | A Benchmark to Select Data Mining B | 0.63 |
| Recovering Concept Prerequisite Rel | Discovery of the Mercury Isotopes | 0.63 |
| Recovering Concept Prerequisite Rel | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| Deep Neural Network-Based Predictio | ContextKT: A Context-Based Method f | 0.71 |
| Deep Neural Network-Based Predictio | Designing School Health Services to | 1.00 |
| Deep Neural Network-Based Predictio | Issues in Statewide Scale up of a M | 0.71 |
| Deep Neural Network-Based Predictio | How Should DSM-V Criteria for Schiz | 0.59 |
| Deep Neural Network-Based Predictio | Evaluating English language learner | 0.63 |
| Deep Neural Network-Based Predictio | Unearthing People from the SaND: Re | 0.71 |
| Deep Neural Network-Based Predictio | Confronting the Challenges of Parti | 0.63 |
| Deep Neural Network-Based Predictio | A Benchmark to Select Data Mining B | 0.63 |
| Deep Neural Network-Based Predictio | Discovery of the Mercury Isotopes | 0.63 |
| Deep Neural Network-Based Predictio | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| ContextKT: A Context-Based Method f | Designing School Health Services to | 0.71 |
| ContextKT: A Context-Based Method f | Issues in Statewide Scale up of a M | 1.00 |
| Designing School Health Services to | Issues in Statewide Scale up of a M | 0.71 |
| Designing School Health Services to | How Should DSM-V Criteria for Schiz | 0.59 |
| Designing School Health Services to | Evaluating English language learner | 0.63 |
| Designing School Health Services to | Unearthing People from the SaND: Re | 0.71 |
| Designing School Health Services to | Confronting the Challenges of Parti | 0.63 |
| Designing School Health Services to | A Benchmark to Select Data Mining B | 0.63 |
| Designing School Health Services to | Discovery of the Mercury Isotopes | 0.63 |
| Designing School Health Services to | Skyemou5/Pysoma: A crossplatform Ho | 0.71 |
| How Should DSM-V Criteria for Schiz | Evaluating English language learner | 0.98 |
| How Should DSM-V Criteria for Schiz | Unearthing People from the SaND: Re | 0.83 |
| How Should DSM-V Criteria for Schiz | Confronting the Challenges of Parti | 0.98 |
| How Should DSM-V Criteria for Schiz | A Benchmark to Select Data Mining B | 0.98 |
| How Should DSM-V Criteria for Schiz | Discovery of the Mercury Isotopes | 0.81 |
| How Should DSM-V Criteria for Schiz | processing/p5.js: p5.js is a client | 0.64 |
| How Should DSM-V Criteria for Schiz | Skyemou5/Pysoma: A crossplatform Ho | 0.83 |
| Evaluating English language learner | Unearthing People from the SaND: Re | 0.89 |
| Evaluating English language learner | Confronting the Challenges of Parti | 1.00 |
| Evaluating English language learner | A Benchmark to Select Data Mining B | 1.00 |
| Evaluating English language learner | Discovery of the Mercury Isotopes | 0.80 |
| Evaluating English language learner | processing/p5.js: p5.js is a client | 0.49 |
| Evaluating English language learner | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Unearthing People from the SaND: Re | Confronting the Challenges of Parti | 0.89 |
| Unearthing People from the SaND: Re | A Benchmark to Select Data Mining B | 0.89 |
| Unearthing People from the SaND: Re | Discovery of the Mercury Isotopes | 0.89 |
| Unearthing People from the SaND: Re | Skyemou5/Pysoma: A crossplatform Ho | 1.00 |
| Confronting the Challenges of Parti | A Benchmark to Select Data Mining B | 1.00 |
| Confronting the Challenges of Parti | Discovery of the Mercury Isotopes | 0.80 |
| Confronting the Challenges of Parti | processing/p5.js: p5.js is a client | 0.49 |
| Confronting the Challenges of Parti | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Inter-Variability Study of COVLIAS  | Culture, goal orientation and achie | 1.00 |
| Inter-Variability Study of COVLIAS  | Discovery of the Mercury Isotopes | 0.45 |
| Inter-Variability Study of COVLIAS  | processing/p5.js: p5.js is a client | 0.66 |
| Culture, goal orientation and achie | Discovery of the Mercury Isotopes | 0.45 |
| Culture, goal orientation and achie | processing/p5.js: p5.js is a client | 0.66 |
| A Benchmark to Select Data Mining B | Discovery of the Mercury Isotopes | 0.80 |
| A Benchmark to Select Data Mining B | processing/p5.js: p5.js is a client | 0.49 |
| A Benchmark to Select Data Mining B | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |
| Discovery of the Mercury Isotopes | processing/p5.js: p5.js is a client | 0.45 |
| Discovery of the Mercury Isotopes | Skyemou5/Pysoma: A crossplatform Ho | 0.89 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.621
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
| 2 | Educational data mining: Predictive analysis of ac | 2019 | 0.487 | YES |
| 3 | Psychology | None | 0.254 | — |
| 4 | Predicting Student Performance Using Data Mining a | 2020 | 0.498 | YES |
| 5 | Educational data mining and learning analytics: An | 2020 | 0.498 | YES |
| 6 | A Systematic Review of Deep Learning Approaches to | 2019 | 0.483 | YES |
| 7 | Educational data mining and learning analytics for | 2019 | 0.488 | YES |
| 8 | Computer Science | None | 0.393 | — |
| 9 | THU-TIOE-ML/GLM3_6B_Education_Ornstein | 2026 | 0.502 | — |
| 10 | THU-TIOE-ML/Mixtral8_7B_Education_Ornstein | 2026 | 0.502 | — |

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
| [Emerging] AND using Machine Learning | 0.153 |
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
| temporal:very_recent + topic:e | impact:emerging | 0.056 | 0.81 | 1.33 |
| impact:highly_cited | topic:computer science | 0.108 | 0.75 | 1.31 |
| method:machine_learning + temp | topic:computer science | 0.054 | 0.75 | 1.30 |
| method:machine_learning | topic:computer science | 0.169 | 0.74 | 1.29 |
| finding:positive + temporal:ve | impact:emerging | 0.077 | 0.77 | 1.25 |
| impact:emerging + method:machi | topic:computer science | 0.110 | 0.72 | 1.25 |
| method:machine_learning + temp | impact:emerging | 0.070 | 0.74 | 1.21 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 20683
**High-tier pairs:** 313
**Convergence events:** 15

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_013 | 0.402 | 2 | 0y | 2 |
| svw_002 | 0.280 | 3 | 2y | 3 |
| svw_011 | 0.222 | 2 | 1y | 2 |
| svw_003 | 0.209 | 2 | 1y | 2 |
| svw_009 | 0.204 | 2 | 1y | 2 |
| svw_010 | 0.203 | 2 | 2y | 2 |
| svw_012 | 0.201 | 2 | 2y | 2 |
| svw_001 | 0.172 | 2010 | 53y | 2010 |
| svw_005 | 0.151 | 6 | 18y | 6 |
| svw_007 | 0.142 | 3 | 5y | 3 |
| svw_014 | 0.128 | 3 | 5y | 3 |
| svw_015 | 0.073 | 2 | 5y | 2 |
| svw_008 | 0.053 | 2 | 7y | 2 |
| svw_006 | 0.052 | 2 | 7y | 2 |
| svw_004 | 0.047 | 2 | 8y | 2 |

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
- **Grounded in:** entropy gap node: The current landscape of learning analytics in higher edu...
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 75% confidence in apriori patterns)
- **Gap node:** `17abdcb1da177cefb81d7d76dc801129f1d828f0` (severity: 6)
- **On golden path:** No


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
| Total sources | 3120 |
| Timestamp | 2026-04-04T01:50:05.773568 |
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