# DCFN Technical Report: Neuroscience

**How This Analysis Was Conducted**

**Engine:** DCFN v0.3.0-prototype — Living Eden Frameworks LLC
**Date:** April 04, 2026
**Sources:** 3171

---

*This document is the methodology receipt for the accompanying Research Intelligence Article. It documents every parameter, threshold, and result produced by the DCFN pipeline. For findings, interpretation, and gap-bridging proposals, see the Article.*

## 1. Pipeline Summary

| Metric | Value |
|--------|-------|
| Domain | Neuroscience |
| Sources Analyzed | 3171 |
| Graph Nodes | 3184 |
| Graph Edges | 12582 |
| Knowledge Gaps (total) | 3105 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 11 |
| Convergence Events | 2 |
| Generated Hypotheses | 5 |
| Cross-Domain Bridges | 0 |
| Golden Path Length | 10 |
| Golden Path Confidence | HIGH |

**Cognitive abilities exercised:** 10/10 — Perception, Generation, Attention, Learning, Memory, Reasoning, Metacognition, Executive Functions, Problem Solving, Social Cognition

## 2. Data Collection

**Total sources:** 3171

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
| Partially grounded (0.4–0.7) | 2051 |
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
| LOW threshold | < 0.46923697981477586 (30th percentile) |
| HIGH threshold | ≥ 0.5153342398617358 (80th percentile) |
| Concentration p25/p50/p75 | 0.50955632714733 / 0.5586032601441989 / 0.6236272819471687 |
| Distinctiveness p25/p50/p75 | 0.6693189356237579 / 0.7068295842927124 / 0.755991874102635 |
| Stability p25/p50/p75 | 0.2648940432828669 / 0.2814301165327723 / 0.29714299147728107 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3184 |
|   — CONCEPT | 13 |
|   — DOCUMENT | 3171 |
| Total Edges | 12582 |
|   — MIRRORS | 5421 |
|   — CONTAINS | 4766 |
|   — EXTENDS | 1543 |
|   — ENABLES | 812 |
|   — DEPENDS_ON | 40 |
| Density | 0.001241 |
| Connected Components | 195 |

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

**Total entropy nodes:** 3105
**Critical (≥7):** 0 | **High (5-6):** 1365 | **Low (<5):** 1740

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3105 |
| STALE | 3009 |
| ORPHAN | 192 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Synaptic Plasticity Forms and Functions. | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | 20 years of the default mode network: A revie | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | Review and Classification of Emotion Recognit | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | From Cognitive Load Theory to Collaborative C | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Microglia regulation of synaptic plasticity a | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Dopamine reward prediction error coding | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | Diverse synaptic plasticity mechanisms orches | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Neuroplasticity of Language Networks in Aphas | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | Training the Emotional Brain: Improving Affec | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | A Review of Transcranial Magnetic Stimulation | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Dopamine neurons share common response functi | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Neural ensemble dynamics underlying a long-te | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Cognitive-Load Theory: Methods to Manage Work | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | Development of Spatial and Verbal Working Mem | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Memory Consolidation Is Linked to Spindle-Med | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Neural ageing and synaptic plasticity: priori | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Remembering to Forget: A Dual Role for Sleep  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Phasic Dopamine Release in the Rat Nucleus Ac | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Default mode network can support the level of | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Distant from input: Evidence of regions withi | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 11 total (6 emerging, 5 established)
**Structural mirrors:** 29

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| Dissociable Intrinsic Connectivity Networks for Sa | 543 | Established | 2015.5 |
| Predictive Reward Signal of Dopamine Neurons | 419 | Established | 2018.3 |
| Faster R-CNN: Towards Real-Time Object Detection w | 1758 | Established | 2018.8 |
| Cognitive Architecture and Instructional Design: 2 | 51 | Established | 2019.8 |
| A Cognitive Load Theory Approach to Defining and M | 2 | Emerging | 2023.0 |
| Cognitive Load Theory: Emerging Trends and Innovat | 2 | Emerging | 2024.5 |
| Data-driven biomarkers outperform theory-based bio | 2 | Emerging | 2023.5 |
| unitreerobotics/G1_WBT_Brainco_Collect_Plates_Into | 17 | Established | 2018.8 |
| BrainDelay/BatVenom-V7 (text-generation) | 55 | Emerging | 2024.9 |
| LibreYOLO/brain-tumor-m2pbp (dataset) | 52 | Emerging | 2025.2 |
| brain-bzh/reve-positions (feature-extraction) | 91 | Emerging | 2024.9 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| Dissociable Intrinsic Connectivity  | Predictive Reward Signal of Dopamin | 0.82 |
| Dissociable Intrinsic Connectivity  | Faster R-CNN: Towards Real-Time Obj | 1.00 |
| Dissociable Intrinsic Connectivity  | Cognitive Architecture and Instruct | 0.69 |
| Dissociable Intrinsic Connectivity  | unitreerobotics/G1_WBT_Brainco_Coll | 0.85 |
| Dissociable Intrinsic Connectivity  | BrainDelay/BatVenom-V7 (text-genera | 0.50 |
| Dissociable Intrinsic Connectivity  | LibreYOLO/brain-tumor-m2pbp (datase | 0.54 |
| Dissociable Intrinsic Connectivity  | brain-bzh/reve-positions (feature-e | 0.44 |
| Predictive Reward Signal of Dopamin | Faster R-CNN: Towards Real-Time Obj | 0.79 |
| Predictive Reward Signal of Dopamin | Cognitive Architecture and Instruct | 0.98 |
| Predictive Reward Signal of Dopamin | unitreerobotics/G1_WBT_Brainco_Coll | 0.99 |
| Predictive Reward Signal of Dopamin | BrainDelay/BatVenom-V7 (text-genera | 0.87 |
| Predictive Reward Signal of Dopamin | LibreYOLO/brain-tumor-m2pbp (datase | 0.92 |
| Predictive Reward Signal of Dopamin | brain-bzh/reve-positions (feature-e | 0.77 |
| Faster R-CNN: Towards Real-Time Obj | Cognitive Architecture and Instruct | 0.66 |
| Faster R-CNN: Towards Real-Time Obj | unitreerobotics/G1_WBT_Brainco_Coll | 0.83 |
| Faster R-CNN: Towards Real-Time Obj | BrainDelay/BatVenom-V7 (text-genera | 0.49 |
| Faster R-CNN: Towards Real-Time Obj | LibreYOLO/brain-tumor-m2pbp (datase | 0.51 |
| Faster R-CNN: Towards Real-Time Obj | brain-bzh/reve-positions (feature-e | 0.44 |
| Cognitive Architecture and Instruct | unitreerobotics/G1_WBT_Brainco_Coll | 0.95 |
| Cognitive Architecture and Instruct | BrainDelay/BatVenom-V7 (text-genera | 0.92 |
| Cognitive Architecture and Instruct | LibreYOLO/brain-tumor-m2pbp (datase | 0.98 |
| Cognitive Architecture and Instruct | brain-bzh/reve-positions (feature-e | 0.83 |
| Data-driven biomarkers outperform t | brain-bzh/reve-positions (feature-e | 0.51 |
| unitreerobotics/G1_WBT_Brainco_Coll | BrainDelay/BatVenom-V7 (text-genera | 0.86 |
| unitreerobotics/G1_WBT_Brainco_Coll | LibreYOLO/brain-tumor-m2pbp (datase | 0.90 |
| unitreerobotics/G1_WBT_Brainco_Coll | brain-bzh/reve-positions (feature-e | 0.79 |
| BrainDelay/BatVenom-V7 (text-genera | LibreYOLO/brain-tumor-m2pbp (datase | 0.97 |
| BrainDelay/BatVenom-V7 (text-genera | brain-bzh/reve-positions (feature-e | 0.98 |
| LibreYOLO/brain-tumor-m2pbp (datase | brain-bzh/reve-positions (feature-e | 0.90 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 4.655
**Confidence:** HIGH
**Entropy nodes resolved:** 3

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
| 3 | Default mode network can support the level of deta | 2018 | 0.478 | YES |
| 4 | Distant from input: Evidence of regions within the | 2018 | 0.478 | YES |
| 5 | Computer Science | None | 0.368 | — |
| 6 | BrainForge/Devstral-2-123B-Instruct-2512 | 2026 | 0.504 | — |
| 7 | bendik-eeg-henriksen/norwegian-legal-bert (fill-ma | 2026 | 0.507 | — |
| 8 | ACE-Brain/ACE-Brain-0-8B (image-text-to-text) | 2026 | 0.506 | — |
| 9 | PrunaAI/cognitivecomputations-Dolphin-2.9.1-Phi-3- | 2026 | 0.502 | — |
| 10 | mradermacher/HuatuoGPT-Vision-7B-Brainseg-SFT-224- | 2026 | 0.502 | — |

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
| (Very Recent work) AND research in Computer Science | 0.182 |
| [Emerging] AND research in Neuroscience | 0.171 |
| using Neuroimaging AND research in Neuroscience | 0.169 |
| [Emerging] AND using Neuroimaging | 0.166 |
| using Neuroimaging AND research in Computer Science | 0.150 |
| (Foundational work) AND research in Neuroscience | 0.148 |
| [Emerging] AND studying Clinical | 0.140 |
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

**Candidate pairs:** 31394
**High-tier pairs:** 659
**Convergence events:** 2

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_001 | 0.165 | 2158 | 48y | 2158 |
| svw_002 | 0.150 | 2 | 2y | 2 |

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
- **Hypothesis:** Re-examining 'Microglia regulation of synaptic plasticity and learning and memory' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Microglia regulation of synaptic plasticity and learning ...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `7fb4e04a32b408cb7dd65bb228533034f1c811c2` (severity: 6)
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
| Total sources | 3171 |
| Timestamp | 2026-04-04T02:09:32.472847 |
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