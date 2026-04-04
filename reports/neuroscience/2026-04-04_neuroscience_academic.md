# DCFN Technical Report: Neuroscience

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3172

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Neuroscience |
| Sources Analyzed | 3172 |
| Graph Nodes | 3185 |
| Graph Edges | 12575 |
| Knowledge Gaps (total) | 3106 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 12 |
| Convergence Events | 4 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3172

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
| Well-grounded (≥0.7) | 1036 |
| Partially grounded (0.4–0.7) | 2052 |
| Weakly grounded (0.2–0.4) | 84 |
| Ungrounded (<0.2) | 0 |
| **Mean grounding score** | **0.691** |

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
| LOW threshold | < 0.4699974091235616 (30th percentile) |
| HIGH threshold | ≥ 0.5161617946596513 (80th percentile) |
| Concentration p25/p50/p75 | 0.5104303910791614 / 0.5592476660422423 / 0.6248085473895879 |
| Distinctiveness p25/p50/p75 | 0.6698918874065758 / 0.7065813229279474 / 0.7569246525007766 |
| Stability p25/p50/p75 | 0.2638969880891921 / 0.2800767525530179 / 0.2971246438953393 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3185 |
|   — CONCEPT | 13 |
|   — DOCUMENT | 3172 |
| Total Edges | 12575 |
|   — MIRRORS | 5410 |
|   — CONTAINS | 4765 |
|   — EXTENDS | 1548 |
|   — ENABLES | 812 |
|   — DEPENDS_ON | 40 |
| Density | 0.001240 |
| Connected Components | 196 |

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
| Biology | 1 | 0.00 | 0 |
| Medicine | 1 | 0.00 | 0 |
| Psychology | 1 | 0.00 | 0 |

### 5.2 Forward Cascade

**Cascades analyzed:** 5

| Source | Implications | Longest Chain | High Conf | Blocked |
|--------|-------------|--------------|----------|---------|
| Mirror Neurons and Pain: A Scoping Review of  | 0 | 0 | 0 | 0 |
| D-MEM: Dopamine-Gated Agentic Memory via Rewa | 0 | 0 | 0 | 0 |
| Span capacity and age-related differences in  | 0 | 0 | 0 | 0 |
| BDNF and miRNAs in acupuncture-regulated neur | 0 | 0 | 0 | 0 |
| Memory consolidation during sleep: a facilita | 0 | 0 | 0 | 0 |

### 5.3 Entropy Detection

**Total entropy nodes:** 3106
**Critical (≥7):** 0 | **High (5-6):** 1370 | **Low (<5):** 1736

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3106 |
| STALE | 3009 |
| ORPHAN | 193 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Synaptic Plasticity Forms and Functions. | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | 20 years of the default mode network: A revie | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Review and Classification of Emotion Recognit | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | From Cognitive Load Theory to Collaborative C | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Rehabilitation robots for the treatment of se | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Dopamine reward prediction error coding | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Neuroplasticity of Language Networks in Aphas | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Training the Emotional Brain: Improving Affec | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | A Review of Transcranial Magnetic Stimulation | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | Neural functions of calcineurin in synaptic p | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Neural Correlates of Verbal Working Memory: A | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | The Implications of Microglial Regulation in  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Dopamine neurons share common response functi | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Neural ensemble dynamics underlying a long-te | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Cognitive-Load Theory: Methods to Manage Work | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Development of Spatial and Verbal Working Mem | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | MicroRNAs in learning, memory, and neurologic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Memory Consolidation Is Linked to Spindle-Med | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Neural ageing and synaptic plasticity: priori | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Remembering to Forget: A Dual Role for Sleep  | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 12 total (6 emerging, 6 established)
**Structural mirrors:** 35

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Dissociable Intrinsic Connectivity Networks for Sa | 537 | Established | 2015.2 |
| Predictive Reward Signal of Dopamine Neurons | 488 | Established | 2018.4 |
| Faster R-CNN: Towards Real-Time Object Detection w | 1696 | Established | 2018.9 |
| A Cognitive Load Theory Approach to Defining and M | 2 | Emerging | 2023.0 |
| Self–other relations in social development and aut | 21 | Established | 2017.1 |
| Cognitive Load Theory: Emerging Trends and Innovat | 2 | Emerging | 2024.5 |
| The Role of Smad2 in Adult Neuroplasticity as Seen | 14 | Established | 2014.2 |
| Data-driven biomarkers outperform theory-based bio | 2 | Emerging | 2023.5 |
| unitreerobotics/G1_WBT_Brainco_Collect_Plates_Into | 17 | Established | 2018.8 |
| BrainDelay/BatVenom-V7 (text-generation) | 61 | Emerging | 2024.7 |
| LibreYOLO/brain-tumor-m2pbp (dataset) | 61 | Emerging | 2025.2 |
| brain-bzh/reve-positions (feature-extraction) | 91 | Emerging | 2024.9 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Dissociable Intrinsic Connectivity  | Predictive Reward Signal of Dopamin | 0.76 |
| Dissociable Intrinsic Connectivity  | Faster R-CNN: Towards Real-Time Obj | 0.99 |
| Dissociable Intrinsic Connectivity  | Self–other relations in social deve | 0.65 |
| Dissociable Intrinsic Connectivity  | The Role of Smad2 in Adult Neuropla | 0.98 |
| Dissociable Intrinsic Connectivity  | unitreerobotics/G1_WBT_Brainco_Coll | 0.81 |
| Dissociable Intrinsic Connectivity  | BrainDelay/BatVenom-V7 (text-genera | 0.47 |
| Dissociable Intrinsic Connectivity  | LibreYOLO/brain-tumor-m2pbp (datase | 0.51 |
| Predictive Reward Signal of Dopamin | Faster R-CNN: Towards Real-Time Obj | 0.72 |
| Predictive Reward Signal of Dopamin | Self–other relations in social deve | 0.98 |
| Predictive Reward Signal of Dopamin | The Role of Smad2 in Adult Neuropla | 0.82 |
| Predictive Reward Signal of Dopamin | unitreerobotics/G1_WBT_Brainco_Coll | 0.98 |
| Predictive Reward Signal of Dopamin | BrainDelay/BatVenom-V7 (text-genera | 0.89 |
| Predictive Reward Signal of Dopamin | LibreYOLO/brain-tumor-m2pbp (datase | 0.94 |
| Predictive Reward Signal of Dopamin | brain-bzh/reve-positions (feature-e | 0.78 |
| Faster R-CNN: Towards Real-Time Obj | Self–other relations in social deve | 0.60 |
| Faster R-CNN: Towards Real-Time Obj | The Role of Smad2 in Adult Neuropla | 0.97 |
| Faster R-CNN: Towards Real-Time Obj | unitreerobotics/G1_WBT_Brainco_Coll | 0.78 |
| Faster R-CNN: Towards Real-Time Obj | BrainDelay/BatVenom-V7 (text-genera | 0.45 |
| Faster R-CNN: Towards Real-Time Obj | LibreYOLO/brain-tumor-m2pbp (datase | 0.47 |
| Self–other relations in social deve | The Role of Smad2 in Adult Neuropla | 0.75 |
| Self–other relations in social deve | unitreerobotics/G1_WBT_Brainco_Coll | 0.97 |
| Self–other relations in social deve | BrainDelay/BatVenom-V7 (text-genera | 0.94 |
| Self–other relations in social deve | LibreYOLO/brain-tumor-m2pbp (datase | 0.98 |
| Self–other relations in social deve | brain-bzh/reve-positions (feature-e | 0.83 |
| The Role of Smad2 in Adult Neuropla | unitreerobotics/G1_WBT_Brainco_Coll | 0.89 |
| The Role of Smad2 in Adult Neuropla | BrainDelay/BatVenom-V7 (text-genera | 0.58 |
| The Role of Smad2 in Adult Neuropla | LibreYOLO/brain-tumor-m2pbp (datase | 0.62 |
| The Role of Smad2 in Adult Neuropla | brain-bzh/reve-positions (feature-e | 0.49 |
| Data-driven biomarkers outperform t | brain-bzh/reve-positions (feature-e | 0.52 |
| unitreerobotics/G1_WBT_Brainco_Coll | BrainDelay/BatVenom-V7 (text-genera | 0.88 |
| unitreerobotics/G1_WBT_Brainco_Coll | LibreYOLO/brain-tumor-m2pbp (datase | 0.91 |
| unitreerobotics/G1_WBT_Brainco_Coll | brain-bzh/reve-positions (feature-e | 0.79 |
| BrainDelay/BatVenom-V7 (text-genera | LibreYOLO/brain-tumor-m2pbp (datase | 0.98 |
| BrainDelay/BatVenom-V7 (text-genera | brain-bzh/reve-positions (feature-e | 0.97 |
| LibreYOLO/brain-tumor-m2pbp (datase | brain-bzh/reve-positions (feature-e | 0.90 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.703
**Confidence:** HIGH
**Entropy nodes resolved:** 1

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
| 1 | 20 years of the default mode network: A review and | 2023 | 0.526 | YES |
| 2 | Default Mode Dynamics for Global Functional Integr | 2015 | 0.282 | — |
| 3 | Computer Science | None | 0.368 | — |
| 4 | BrainForge/Devstral-2-123B-Instruct-2512 | 2026 | 0.505 | — |
| 5 | bendik-eeg-henriksen/norwegian-legal-bert (fill-ma | 2026 | 0.507 | — |
| 6 | ACE-Brain/ACE-Brain-0-8B (image-text-to-text) | 2026 | 0.506 | — |
| 7 | PrunaAI/cognitivecomputations-Dolphin-2.9.1-Phi-3- | 2026 | 0.502 | — |
| 8 | mradermacher/HuatuoGPT-Vision-7B-Brainseg-SFT-224- | 2026 | 0.502 | — |
| 9 | vibhansh/Veda-8B-v1-Cognitive (text-generation) | 2026 | 0.502 | — |
| 10 | BrainDelay/DoubleC-V1 (text-generation) | 2026 | 0.502 | — |

## 6. Supplementary Analyses

### 6.1 Co-Occurrence Patterns (Apriori)

**Frequent 1-itemsets:** 23
**Frequent 2-itemsets:** 51
**Frequent 3-itemsets:** 22
**Association rules:** 27

**Parameters:** min_support = 0.05, min_confidence = 0.60

**Top Frequent Patterns:**

| Pattern | Support |
|---------|---------|
| [Emerging] AND research in Computer Science | 0.292 |
| [Emerging] AND (Very Recent work) | 0.225 |
| (Very Recent work) AND research in Computer Science | 0.181 |
| [Emerging] AND research in Neuroscience | 0.171 |
| using Neuroimaging AND research in Neuroscience | 0.169 |
| [Emerging] AND using Neuroimaging | 0.166 |
| using Neuroimaging AND research in Computer Science | 0.150 |
| (Foundational work) AND research in Neuroscience | 0.148 |
| [Emerging] AND studying Clinical | 0.141 |
| [Emerging] AND (Established work) | 0.132 |

**Top Association Rules (by lift):**

| Antecedent | Consequent | Support | Confidence | Lift |
|------------|-----------|---------|------------|------|
| impact:highly_cited + topic:ne | temporal:foundational | 0.083 | 0.65 | 2.93 |
| impact:highly_cited + temporal | topic:neuroscience | 0.083 | 0.94 | 2.69 |
| method:neuroimaging + temporal | topic:neuroscience | 0.058 | 0.81 | 2.32 |
| impact:highly_cited + topic:bi | topic:neuroscience | 0.052 | 0.80 | 2.28 |
| temporal:foundational + topic: | topic:neuroscience | 0.052 | 0.77 | 2.21 |
| impact:highly_cited + method:n | topic:neuroscience | 0.057 | 0.73 | 2.10 |
| temporal:foundational + topic: | topic:neuroscience | 0.062 | 0.69 | 1.99 |
| temporal:foundational | topic:neuroscience | 0.148 | 0.67 | 1.92 |
| impact:highly_cited | topic:neuroscience | 0.129 | 0.67 | 1.91 |
| impact:highly_cited + topic:co | topic:neuroscience | 0.063 | 0.61 | 1.75 |

### 6.2 Synchronicity Detection (SVW)

**Candidate pairs:** 31973
**High-tier pairs:** 671
**Convergence events:** 4

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.165 | 2150 | 48y | 2150 |
| svw_003 | 0.090 | 2 | 4y | 2 |
| svw_004 | 0.051 | 2 | 7y | 2 |
| svw_002 | 0.025 | 2 | 16y | 2 |

### 6.3 Generated Hypotheses

**Total generated:** 5

**H01** [MEDIUM]
- **Hypothesis:** Re-examining 'Synaptic Plasticity Forms and Functions.' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Synaptic Plasticity Forms and Functions.
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `97ab16d0e4a98f8275932f0a684e4fdcd70fb2d3` (severity: 6)
- **On golden path:** No

**H02** [MEDIUM]
- **Hypothesis:** Re-examining '20 years of the default mode network: A review and synthesis.' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: 20 years of the default mode network: A review and synthe... + included in golden token recommended path
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `74e9cad6e3d8b4187216aaaaa171d808e48d34f0` (severity: 6)
- **On golden path:** Yes

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'Review and Classification of Emotion Recognition Based on EEG Brain...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Review and Classification of Emotion Recognition Based on...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `b067b33daddbd064592e12f2a4c1cfc300a2992e` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'From Cognitive Load Theory to Collaborative Cognitive Load Theory' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: From Cognitive Load Theory to Collaborative Cognitive Loa...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `a7dacb4598eb77ea3d84dc2c2c2603de49d6acd9` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Rehabilitation robots for the treatment of sensorimotor deficits: a...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Rehabilitation robots for the treatment of sensorimotor d...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `7f42ce61353f84a3bff2698a9ca0c23a04fec278` (severity: 6)
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
| Total sources | 3172 |
| Timestamp | 2026-04-04T03:11:39.396478 |
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