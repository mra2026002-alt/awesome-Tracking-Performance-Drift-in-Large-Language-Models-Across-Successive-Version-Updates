# GitHub Implementations

Existing, actively maintained GitHub repositories that implement the drift-monitoring, evaluation, and contamination-detection methodologies discussed in the accompanying paper. Each was selected based on documentation quality, maintenance activity, and direct connection to a cited research paper (not just search ranking or star count), per the evaluation criteria in the course instructions.

- **ChatLog**
  [github.com/THU-KEG/ChatLog](https://github.com/THU-KEG/ChatLog/)
  Official code and data release for Tu et al. (2023), "ChatLog: Recording and Analyzing ChatGPT Across Time." Implements the paper's monthly/daily fixed-prompt replay methodology for tracking ChatGPT's behavior over time, including the stable-feature extraction pipeline used for cross-version detection robustness. Directly implements the continuous-monitoring approach described in Section 4.1 of the accompanying paper.

- **HELM (Holistic Evaluation of Language Models)**
  [github.com/stanford-crfm/helm](https://github.com/stanford-crfm/helm)
  Official implementation from Stanford CRFM of the standardized multi-metric evaluation framework introduced by Liang et al. (2022). Actively maintained with extensive documentation, reproducible scenario/metric configs, and public leaderboards. Implements the disaggregated, multi-dimensional evaluation approach discussed in Section 4.2 and proposed as a drift-tracking default in Section 6.4.

- **FastChat / LLM Judge (MT-Bench)**
  [github.com/lm-sys/FastChat](https://github.com/lm-sys/FastChat)
  Official implementation from LMSYS of the MT-Bench and Chatbot Arena evaluation methodology from Zheng et al. (2023). Includes the `fastchat/llm_judge` module implementing the GPT-4-as-judge grading pipeline. Directly implements the LLM-as-judge preference-tracking approach discussed in Section 4.3, including reference code for reproducing the paper's reported judge-agreement statistics.

- **LLM Decontaminator**
  [github.com/lm-sys/llm-decontaminator](https://github.com/lm-sys/llm-decontaminator)
  Official implementation of the embedding-similarity-plus-LLM-judgment contamination detection method (Yang et al., 2023), cited in the benchmark-contamination survey (Xu et al., 2024) that the paper draws on in Section 3.3. Provides a working, documented alternative to simple n-gram overlap detection, directly relevant to the paper's discussion of contamination-resistant benchmarking (Section 6.1).

- **BIG-bench**
  [github.com/google/BIG-bench](https://github.com/google/BIG-bench)
  Official Google Research repository for the collaborative benchmark introduced by Srivastava et al. (2022). Contains 200+ documented tasks, evaluation scripts, and a SeqIO-based task-running framework. Cited in the paper (Section 2.3) as an example of shared, reproducible evaluation infrastructure, and discussed as a benchmark vulnerable to the contamination dynamics covered in Section 3.3.

**Selection notes:** All five repositories are official releases maintained by the original paper authors or their labs (not third-party forks or reimplementations), each includes real documentation and reproducible instructions, and each is directly cited or discussed in the accompanying paper rather than being a generic, loosely related tool.
