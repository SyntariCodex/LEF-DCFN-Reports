# DCFN Technical Report: Neuroscience

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 06, 2026
**Sources:** 3122

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Neuroscience |
| Sources Analyzed | 3122 |
| Graph Nodes | 3135 |
| Graph Edges | 314123 |
| Knowledge Gaps (total) | 2858 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 5 |
| Convergence Events | 2 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3122

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
| Well-grounded (≥0.7) | 1077 |
| Partially grounded (0.4–0.7) | 1957 |
| Weakly grounded (0.2–0.4) | 88 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.698** |

## 3. Source Encoding (QEB)

### 3.1 Method

Sentence-BERT (all-MiniLM-L6-v2) → 384-dimensional semantic embeddings. Gaussian perturbation (σ = 0.1) applied per QECO Patent §6.2.1.

### 3.2 Three-Signal Adaptive Confidence

| Signal | Weight | Description |
|--------|--------|-------------|
| Perturbation Stability | 0.2234 | Mean pairwise cosine across 5 perturbation iterations |
| Vector Concentration | 0.1766 | Energy fraction in top 10% of embedding dimensions |
| Corpus Distinctiveness | 0.6 | Cosine distance from corpus centroid |

**Formula:** Composite = 0.2234 × Stability + 0.1766 × Concentration + 0.6 × Distinctiveness (calibrated)

### 3.3 Calibration State

| Parameter | Value |
|-----------|-------|
| Embedding dim | 384 |
| Perturbation σ | 0.1 |
| LOW threshold | < 0.3948419153600761 (30th percentile) |
| HIGH threshold | ≥ 0.502183874742841 (80th percentile) |
| Concentration p25/p50/p75 | 0.42376288771629333 / 0.43800656497478485 / 0.4527628421783447 |
| Distinctiveness p25/p50/p75 | 0.43721477687358856 / 0.509370744228363 / 0.6055646687746048 |
| Stability p25/p50/p75 | 0.19209155404625103 / 0.205763683202903 / 0.21996629217555674 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3135 |
|   — CONCEPT | 13 |
|   — DOCUMENT | 3122 |
| Total Edges | 314123 |
|   — MIRRORS | 296570 |
|   — EXTENDS | 12207 |
|   — CONTAINS | 4738 |
|   — ENABLES | 573 |
|   — DEPENDS_ON | 35 |
| Density | 0.031972 |
| Connected Components | 69 |

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
| Contribution of default mode network to game and d | 1 | 0.00 | 0 |
| Neuroscience | 1 | 0.00 | 0 |
| Sleep Enhances Consolidation of Memory Traces for  | 1 | 0.00 | 1 |
| Object-Location Memory Training in Older Adults Le | 1 | 0.00 | 1 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| Beyond Cognitive Load Theory: Why Learning Ne | 0 | 0 | 0 | 0 |
| Mirror Neurons and Pain: A Scoping Review of  | 0 | 0 | 0 | 0 |
| D-MEM: Dopamine-Gated Agentic Memory via Rewa | 0 | 0 | 0 | 0 |
| Span capacity and age-related differences in  | 0 | 0 | 0 | 0 |
| BDNF and miRNAs in acupuncture-regulated neur | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 2858
**Critical (≥7):** 0 | **High (5-6):** 2314 | **Low (<5):** 544

**Issue Distribution:**

| Type | Count |
|------|-------|
| STALE | 2293 |
| DECAYED | 2247 |
| ORPHAN | 67 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Competitive Mechanisms Subserve Attention in  | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Attention is not not Explanation | 6.0/9 | STALE | — | 0 | 0 |
| 3 | Synaptic Plasticity Forms and Functions. | 6.0/9 | STALE | — | 0 | 0 |
| 4 | Review and Classification of Emotion Recognit | 6.0/9 | STALE | — | 0 | 0 |
| 5 | From Cognitive Load Theory to Collaborative C | 6.0/9 | STALE | — | 0 | 0 |
| 6 | Attend and Diagnose: Clinical Time Series Ana | 6.0/9 | STALE | — | 0 | 0 |
| 7 | Casting a Wide Net: Role of Perineuronal Nets | 6.0/9 | STALE | — | 0 | 0 |
| 8 | Microglia regulation of synaptic plasticity a | 6.0/9 | STALE | — | 0 | 0 |
| 9 | Rehabilitation robots for the treatment of se | 6.0/9 | STALE | — | 0 | 0 |
| 10 | Dopamine reward prediction error coding | 6.0/9 | STALE | — | 0 | 0 |
| 11 | The temporal relationship between reduction o | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Paying attention to attention in depression | 6.0/9 | STALE | — | 0 | 0 |
| 13 | Diverse synaptic plasticity mechanisms orches | 6.0/9 | STALE | — | 0 | 0 |
| 14 | Reinforcement Learning in Multidimensional En | 6.0/9 | STALE | — | 0 | 0 |
| 15 | Neuroplasticity of Language Networks in Aphas | 6.0/9 | STALE | — | 0 | 0 |
| 16 | Neural Mechanisms of Sustained Attention Are  | 6.0/9 | STALE | — | 0 | 0 |
| 17 | Neural Mechanisms of Object-Based Attention | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Training the Emotional Brain: Improving Affec | 6.0/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | A Review of Transcranial Magnetic Stimulation | 6.0/9 | STALE | — | 0 | 0 |
| 20 | Neural functions of calcineurin in synaptic p | 6.0/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 5 total (3 emerging, 2 established)
**Structural mirrors:** 2

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Faster R-CNN: Towards Real-Time Object Detection w | 2812 | Established | 2018.1 |
| brain-bzh/reve-positions (feature-extraction) | 250 | Emerging | 2024.6 |
| Data-driven biomarkers better associate with strok | 2 | Emerging | 2023.5 |
| Neural mechanisms of divided feature-selective att | 2 | Established | 2021.0 |
| bendik-eeg-henriksen/nor-casehold (dataset) | 2 | Emerging | 2026.0 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Faster R-CNN: Towards Real-Time Obj | brain-bzh/reve-positions (feature-e | 0.98 |
| Data-driven biomarkers better assoc | Neural mechanisms of divided featur | 1.00 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 5.125
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
| 1 | Synaptic Plasticity Forms and Functions. | 2020 | 0.577 | YES |
| 2 | Diverse synaptic plasticity mechanisms orchestrate | 2015 | 0.475 | YES |
| 3 | A continual learning survey: Defying forgetting in | 2021 | 0.396 | — |
| 4 | Reinforcement Learning in Multidimensional Environ | 2015 | 0.512 | YES |
| 5 | Paying attention to attention in depression | 2019 | 0.567 | YES |
| 6 | Attention is not not Explanation | 2019 | 0.525 | YES |
| 7 | Neural Mechanisms of Sustained Attention Are Rhyth | 2018 | 0.556 | YES |
| 8 | Quoron/EEG-semantic-text-relevance (dataset) | 2025 | 0.453 | — |
| 9 | gasparyanartur/things-eeg2 (dataset) | 2026 | 0.535 | — |
| 10 | braindecode/isruc-sleep (dataset) | 2026 | 0.528 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 23
**Frequent 2-itemsets:** 55
**Frequent 3-itemsets:** 22
**Association rules:** 27

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.298 |
| [Emerging] AND (Very Recent work) | 0.225 |
| (Very Recent work) AND research in Computer Science | 0.186 |
| [Emerging] AND research in Neuroscience | 0.171 |
| using Neuroimaging AND research in Neuroscience | 0.169 |
| [Emerging] AND using Neuroimaging | 0.169 |
| using Neuroimaging AND research in Computer Science | 0.152 |
| (Foundational work) AND research in Neuroscience | 0.150 |
| [Emerging] AND studying Clinical | 0.141 |
| [Highly Cited] AND research in Neuroscience | 0.131 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| topic:psychology | topic:medicine | 0.058 | 0.78 | 5.43 |
| impact:highly_cited + topic:ne | temporal:foundational | 0.085 | 0.65 | 3.02 |
| impact:highly_cited + temporal | topic:neuroscience | 0.085 | 0.93 | 2.65 |
| method:neuroimaging + temporal | topic:neuroscience | 0.059 | 0.81 | 2.31 |
| impact:highly_cited + topic:bi | topic:neuroscience | 0.053 | 0.79 | 2.26 |
| temporal:foundational + topic: | topic:neuroscience | 0.052 | 0.77 | 2.20 |
| impact:highly_cited + method:n | topic:neuroscience | 0.058 | 0.73 | 2.08 |
| temporal:foundational | topic:neuroscience | 0.150 | 0.70 | 1.99 |
| temporal:foundational + topic: | topic:neuroscience | 0.063 | 0.69 | 1.97 |
| impact:highly_cited | topic:neuroscience | 0.131 | 0.65 | 1.84 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 82337
**High-tier pairs:** 1524
**Convergence events:** 2

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.157 | 2162 | 48y | 2162 |
| svw_002 | 0.038 | 2 | 16y | 2 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Competitive Mechanisms Subserve Attention in Macaque Areas V2 and V4' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Competitive Mechanisms Subserve Attention in Macaque Area...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 83% confidence in apriori patterns)
- **Gap node:** `04282d7cc824dfc57582d8f3abc44afe7c58fc4c` (severity: 6.0)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining 'Attention is not not Explanation' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Attention is not not Explanation + included in golden token recommended path
- **Novel because:** not yet connected to 'Computer Science' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 83% confidence in apriori patterns)
- **Gap node:** `ce177672b00ddf46e4906157a7e997ca9338b8b9` (severity: 6.0)
- **On golden path:** Yes

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Synaptic Plasticity Forms and Functions.' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Synaptic Plasticity Forms and Functions. + included in golden token recommended path
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 83% confidence in apriori patterns)
- **Gap node:** `97ab16d0e4a98f8275932f0a684e4fdcd70fb2d3` (severity: 6.0)
- **On golden path:** Yes

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Review and Classification of Emotion Recognition Based on EEG Brain...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Review and Classification of Emotion Recognition Based on...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 83% confidence in apriori patterns)
- **Gap node:** `b067b33daddbd064592e12f2a4c1cfc300a2992e` (severity: 6.0)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'From Cognitive Load Theory to Collaborative Cognitive Load Theory' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: From Cognitive Load Theory to Collaborative Cognitive Loa...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 83% confidence in apriori patterns)
- **Gap node:** `a7dacb4598eb77ea3d84dc2c2c2603de49d6acd9` (severity: 6.0)
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
| Total sources | 3122 |
| Timestamp | 2026-04-06T00:04:40.588873 |
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