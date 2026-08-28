# Tools and Libraries

Software tools and frameworks directly relevant to LLM performance-drift monitoring, evaluation, and contamination detection — several of which are discussed in the accompanying paper. Each was verified against its official GitHub repository.

- **HELM (Holistic Evaluation of Language Models)**
  Stanford Center for Research on Foundation Models (CRFM)
  [GitHub repository](https://github.com/stanford-crfm/helm)
  A standardized evaluation framework covering accuracy, calibration, robustness, fairness, bias, toxicity, and efficiency under fixed prompting protocols. Discussed in the paper (Section 4.2) as infrastructure reusable for longitudinal drift tracking across successive model releases.

- **FastChat**
  LMSYS (Large Model Systems Organization)
  [GitHub repository](https://github.com/lm-sys/FastChat)
  Open platform for training, serving, and evaluating LLM-based chatbots; powers Chatbot Arena and includes the MT-Bench evaluation harness. Directly implements the LLM-as-judge and pairwise preference methodology discussed in the paper (Section 4.3), based on Zheng et al. (2023).

- **FastChat LLM Judge (MT-Bench)**
  LMSYS
  [GitHub repository](https://github.com/lm-sys/FastChat/tree/main/fastchat/llm_judge)
  The specific sub-package implementing MT-Bench's multi-turn question set and GPT-4-based automated grading pipeline. Used as the reference implementation for the LLM-as-judge preference-tracking approach described in Section 4.3.

- **LLM Decontaminator**
  LMSYS
  [GitHub repository](https://github.com/lm-sys/llm-decontaminator)
  A tool that uses embedding similarity search plus LLM-based judgment to detect rephrased/near-duplicate benchmark contamination in training data, going beyond simple n-gram overlap. Directly relevant to the benchmark-contamination confound discussed in the paper (Section 3.3, citing Xu et al., 2024).

- **BIG-bench**
  Google Research (collaborative benchmark)
  [GitHub repository](https://github.com/google/BIG-bench)
  Command-line tools and task framework for running the 200+ task BIG-bench evaluation suite via SeqIO. Cited in the paper as an example of standardized, shared evaluation infrastructure (Section 2.3) and as a benchmark subject to the contamination risks discussed in Section 3.3.

**Note on scope:** The paper is a literature review rather than an implementation paper, so it does not release its own software. The tools above are the concrete, verifiable implementations of the monitoring and evaluation methodologies the paper surveys.
