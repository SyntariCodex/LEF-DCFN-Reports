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
| Graph Edges | 12564 |
| Knowledge Gaps (total) | 3105 |
| Knowledge Gaps (critical) | 0 |
| Research Clusters | 11 |
| Convergence Events | 3 |
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
| Partially grounded (0.4–0.7) | 2052 |
| Weakly grounded (0.2–0.4) | 83 |
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
| LOW threshold | < 0.46988291961123235 (30th percentile) |
| HIGH threshold | ≥ 0.5157966437434796 (80th percentile) |
| Concentration p25/p50/p75 | 0.5101988902748678 / 0.5585964491707082 / 0.627219872008998 |
| Distinctiveness p25/p50/p75 | 0.6697310606917876 / 0.7065941608555322 / 0.7568082947047077 |
| Stability p25/p50/p75 | 0.26373586716774045 / 0.28031565836542593 / 0.2970518299515551 |

## 4. Concept Graph

### 4.1 Structure

| Metric | Value |
|--------|-------|
| Total Nodes | 3184 |
|   — CONCEPT | 13 |
|   — DOCUMENT | 3171 |
| Total Edges | 12564 |
|   — MIRRORS | 5399 |
|   — CONTAINS | 4764 |
|   — EXTENDS | 1549 |
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

**Total entropy nodes:** 3105
**Critical (≥7):** 0 | **High (5-6):** 1379 | **Low (<5):** 1726

**Issue Distribution:**

| Type | Count |
|------|-------|
| DECAYED | 3105 |
| STALE | 3009 |
| ORPHAN | 193 |

**Complete Entropy Node List:**

| # | Title | Severity | Issues | Bridge Conf | Upstream | Downstream |
|---|-------|----------|--------|------------|----------|------------|
| 1 | Synaptic Plasticity Forms and Functions. | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 2 | Review and Classification of Emotion Recognit | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 3 | From Cognitive Load Theory to Collaborative C | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 4 | Casting a Wide Net: Role of Perineuronal Nets | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 5 | Dopamine reward prediction error coding | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 6 | Training the Emotional Brain: Improving Affec | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 7 | A Review of Transcranial Magnetic Stimulation | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 8 | Neural functions of calcineurin in synaptic p | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 9 | Neural Correlates of Verbal Working Memory: A | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 10 | The Implications of Microglial Regulation in  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 11 | Dopamine neurons share common response functi | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 12 | Cognitive-Load Theory: Methods to Manage Work | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 13 | Development of Spatial and Verbal Working Mem | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 14 | MicroRNAs in learning, memory, and neurologic | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 15 | Memory Consolidation Is Linked to Spindle-Med | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 16 | Neural ageing and synaptic plasticity: priori | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 17 | Remembering to Forget: A Dual Role for Sleep  | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 18 | Phasic Dopamine Release in the Rat Nucleus Ac | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 19 | Default mode network can support the level of | 6/9 | STALE, DECAYED | — | 0 | 0 |
| 20 | Distant from input: Evidence of regions withi | 6/9 | STALE, DECAYED | — | 0 | 0 |

### 5.4 Branch Cataloging

**Clusters:** 11 total (5 emerging, 6 established)
**Structural mirrors:** 28

| Cluster | Size | Status | Avg Year |
|---------|------|--------|----------|
| LibreYOLO/brain-tumor-m2pbp (dataset) | 621 | Established | 2016.4 |
| Predictive Reward Signal of Dopamine Neurons | 479 | Established | 2018.5 |
| Faster R-CNN: Towards Real-Time Object Detection w | 1682 | Established | 2018.8 |
| A Cognitive Load Theory Approach to Defining and M | 2 | Emerging | 2023.0 |
| Self–other relations in social development and aut | 21 | Established | 2017.1 |
| Cognitive Load Theory: Emerging Trends and Innovat | 2 | Emerging | 2024.5 |
| The Role of Smad2 in Adult Neuroplasticity as Seen | 14 | Established | 2014.2 |
| Data-driven biomarkers better associate with strok | 2 | Emerging | 2023.5 |
| unitreerobotics/G1_WBT_Brainco_Collect_Plates_Into | 17 | Established | 2018.8 |
| BrainDelay/BatVenom-V7 (text-generation) | 60 | Emerging | 2024.7 |
| brain-bzh/reve-positions (feature-extraction) | 91 | Emerging | 2024.9 |

**Structural Mirrors:**

| Cluster A | Cluster B | Similarity |
|-----------|-----------|------------|
| LibreYOLO/brain-tumor-m2pbp (datase | Predictive Reward Signal of Dopamin | 0.93 |
| LibreYOLO/brain-tumor-m2pbp (datase | Faster R-CNN: Towards Real-Time Obj | 0.93 |
| LibreYOLO/brain-tumor-m2pbp (datase | Self–other relations in social deve | 0.83 |
| LibreYOLO/brain-tumor-m2pbp (datase | The Role of Smad2 in Adult Neuropla | 0.96 |
| LibreYOLO/brain-tumor-m2pbp (datase | unitreerobotics/G1_WBT_Brainco_Coll | 0.96 |
| LibreYOLO/brain-tumor-m2pbp (datase | BrainDelay/BatVenom-V7 (text-genera | 0.73 |
| LibreYOLO/brain-tumor-m2pbp (datase | brain-bzh/reve-positions (feature-e | 0.64 |
| Predictive Reward Signal of Dopamin | Faster R-CNN: Towards Real-Time Obj | 0.72 |
| Predictive Reward Signal of Dopamin | Self–other relations in social deve | 0.97 |
| Predictive Reward Signal of Dopamin | The Role of Smad2 in Adult Neuropla | 0.80 |
| Predictive Reward Signal of Dopamin | unitreerobotics/G1_WBT_Brainco_Coll | 0.98 |
| Predictive Reward Signal of Dopamin | BrainDelay/BatVenom-V7 (text-genera | 0.88 |
| Predictive Reward Signal of Dopamin | brain-bzh/reve-positions (feature-e | 0.79 |
| Faster R-CNN: Towards Real-Time Obj | Self–other relations in social deve | 0.55 |
| Faster R-CNN: Towards Real-Time Obj | The Role of Smad2 in Adult Neuropla | 0.98 |
| Faster R-CNN: Towards Real-Time Obj | unitreerobotics/G1_WBT_Brainco_Coll | 0.78 |
| Faster R-CNN: Towards Real-Time Obj | BrainDelay/BatVenom-V7 (text-genera | 0.46 |
| Self–other relations in social deve | The Role of Smad2 in Adult Neuropla | 0.67 |
| Self–other relations in social deve | unitreerobotics/G1_WBT_Brainco_Coll | 0.95 |
| Self–other relations in social deve | BrainDelay/BatVenom-V7 (text-genera | 0.94 |
| Self–other relations in social deve | brain-bzh/reve-positions (feature-e | 0.85 |
| The Role of Smad2 in Adult Neuropla | unitreerobotics/G1_WBT_Brainco_Coll | 0.86 |
| The Role of Smad2 in Adult Neuropla | BrainDelay/BatVenom-V7 (text-genera | 0.55 |
| The Role of Smad2 in Adult Neuropla | brain-bzh/reve-positions (feature-e | 0.46 |
| Data-driven biomarkers better assoc | brain-bzh/reve-positions (feature-e | 0.51 |
| unitreerobotics/G1_WBT_Brainco_Coll | BrainDelay/BatVenom-V7 (text-genera | 0.88 |
| unitreerobotics/G1_WBT_Brainco_Coll | brain-bzh/reve-positions (feature-e | 0.79 |
| BrainDelay/BatVenom-V7 (text-genera | brain-bzh/reve-positions (feature-e | 0.98 |

### 5.5 Golden Token Pathfinding

**Path length:** 10
**Composite score:** 5.043
**Confidence:** HIGH
**Entropy nodes resolved:** 0

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
| 1 | bendik-eeg-henriksen/norwegian-legal-bert (fill-ma | 2026 | 0.507 | — |
| 2 | ACE-Brain/ACE-Brain-0-8B (image-text-to-text) | 2026 | 0.506 | — |
| 3 | BrainForge/Devstral-2-123B-Instruct-2512 | 2026 | 0.505 | — |
| 4 | braindecode/labram-pretrained | 2026 | 0.505 | — |
| 5 | braindecode/eegpt-pretrained | 2026 | 0.505 | — |
| 6 | joon0890/BrainMVP-16k (dataset) | 2026 | 0.503 | — |
| 7 | dexmac/progressive-cognitive-results (dataset) | 2026 | 0.503 | — |
| 8 | amhapankar/my-trading-brain (dataset) | 2026 | 0.503 | — |
| 9 | Forainest789/NATVIEW_EEGFMRI_processed (dataset) | 2026 | 0.503 | — |
| 10 | shankar18143/SAM_brain (dataset) | 2026 | 0.503 | — |

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
| [Emerging] AND (Established work) | 0.133 |

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

**Candidate pairs:** 31801
**High-tier pairs:** 669
**Convergence events:** 3

**Parameters:** similarity threshold = 0.40, zero citation linkage required

**Convergence Events:**

| Event | Score | Groups | Time Window | Papers |
|-------|-------|--------|------------|--------|
| svw_003 | 0.261 | 7 | 17y | 7 |
| svw_001 | 0.165 | 2156 | 39y | 2156 |
| svw_002 | 0.027 | 2 | 15y | 2 |

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
- **Hypothesis:** Re-examining 'Review and Classification of Emotion Recognition Based on EEG Brain...' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Review and Classification of Emotion Recognition Based on...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `b067b33daddbd064592e12f2a4c1cfc300a2992e` (severity: 6)
- **On golden path:** No

**H03** [MEDIUM]
- **Hypothesis:** Re-examining 'From Cognitive Load Theory to Collaborative Cognitive Load Theory' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: From Cognitive Load Theory to Collaborative Cognitive Loa...
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `a7dacb4598eb77ea3d84dc2c2c2603de49d6acd9` (severity: 6)
- **On golden path:** No

**H04** [MEDIUM]
- **Hypothesis:** Re-examining 'Casting a Wide Net: Role of Perineuronal Nets in Neural Plasticity' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Casting a Wide Net: Role of Perineuronal Nets in Neural P...
- **Novel because:** not yet connected to 'Psychology' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `b49714edbef46eb488b64b25f061c3f37da86742` (severity: 6)
- **On golden path:** No

**H05** [MEDIUM]
- **Hypothesis:** Re-examining 'Dopamine reward prediction error coding' with contemporary methods will produce findings that substantially update or contradict current consensus in this area
- **Grounded in:** entropy gap node: Dopamine reward prediction error coding
- **Novel because:** not yet connected to 'Medicine' despite logical dependency in prerequisite chain
- **Suggested method:** machine learning (co-occurs with similar gaps at 81% confidence in apriori patterns)
- **Gap node:** `408e947bde841889d0ccf3062bf0769aa635839b` (severity: 6)
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
| Timestamp | 2026-04-04T00:55:29.599280 |
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