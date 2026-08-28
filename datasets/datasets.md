# Datasets

The paper this repository accompanies is a literature review/synthesis, so it does not generate a new dataset of its own. Instead, it draws on several existing datasets and benchmark suites that are directly used in the LLM performance-drift literature it reviews. These are listed below, each verified against its official source repository or publication.

- **ChatLog**
  Source: Tu, S., Li, C., Yu, J., Wang, X., Hou, L., & Li, J. (2023). Tsinghua University.
  [Paper (arXiv:2304.14106)](https://arxiv.org/abs/2304.14106)
  A continuously updated dataset recording ChatGPT's responses to 21 fixed NLP benchmark tasks on a monthly cadence, plus 1,000 fixed long-form generation prompts recorded daily. Used in this paper as the primary example of continuous, high-frequency longitudinal drift monitoring (Section 4.1).

- **HELM (Holistic Evaluation of Language Models) Benchmark Data**
  Source: Stanford Center for Research on Foundation Models (CRFM)
  [Official repository](https://github.com/stanford-crfm/helm) · [Paper (arXiv:2211.09110)](https://arxiv.org/abs/2211.09110)
  A standardized suite of scenarios and metrics (accuracy, calibration, robustness, fairness, bias, toxicity, efficiency) with publicly released raw prompts and completions. Used in this paper as an example of reusable, standardized evaluation infrastructure suited to disaggregated drift tracking (Section 4.2).

- **BIG-bench (Beyond the Imitation Game Benchmark)**
  Source: Google Research, collaborative multi-institution benchmark
  [Official repository](https://github.com/google/BIG-bench) · [Paper (arXiv:2206.04615)](https://arxiv.org/abs/2206.04615)
  A collaboratively assembled benchmark of 204 diverse tasks probing capabilities believed to lie beyond then-current model abilities. Cited in this paper as an example of shared, static benchmark infrastructure relevant to (and vulnerable to) the benchmark-contamination concerns discussed in Section 3.3.

**Note:** No new dataset was collected as part of this paper; it is a review synthesizing existing empirical drift-tracking datasets and benchmark infrastructure rather than original data collection.
