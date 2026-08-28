# References

Verified scholarly references cited in *Tracking Performance Drift in Large Language Models Across Successive Version Updates*. Each entry was checked against its official arXiv listing, DOI, or publisher record — see [Citation Integrity Audit](../citation-audit/Citation_Integrity_Audit.pdf) for verification details.

## Survey and Review Papers

- **A Survey on Concept Drift Adaptation**
  Gama, J., Žliobaitė, I., Bifet, A., Pechenizkiy, M., & Bouchachia, A., 2014, ACM Computing Surveys
  [DOI](https://doi.org/10.1145/2523813)
  Foundational survey of concept-drift detection methods from classical ML, used as the conceptual framework for the paper's drift taxonomy.

- **Benchmark Data Contamination of Large Language Models: A Survey**
  Xu, C., Guan, S., Greene, D., & Kechadi, M.-T., 2024, arXiv:2406.04244
  [arXiv](https://arxiv.org/abs/2406.04244)
  Surveys contamination detection/mitigation methods, central to the paper's discussion of measurement-level drift confounds.

## Foundational Papers

- **Model Cards for Model Reporting**
  Mitchell, M., Wu, S., Zaldivar, A., Barnes, P., Vasserman, L., Hutchinson, B., Spitzer, E., Raji, I. D., & Gebru, T., 2019, FAT* '19 (ACM)
  [DOI](https://doi.org/10.1145/3287560.3287596) · [arXiv](https://arxiv.org/abs/1810.03993)
  Introduces the model-card documentation standard the paper proposes extending into a versioned drift-disclosure norm.

- **Training Language Models to Follow Instructions with Human Feedback**
  Ouyang, L. et al., 2022, Advances in Neural Information Processing Systems 35
  [arXiv](https://arxiv.org/abs/2203.02155)
  Formalizes RLHF (InstructGPT), used to frame drift as partly an intended effect of alignment tuning.

## Recent Research Papers

- **How Is ChatGPT's Behavior Changing Over Time?**
  Chen, L., Zaharia, M., & Zou, J., 2023, arXiv:2307.09009
  [arXiv](https://arxiv.org/abs/2307.09009)
  The founding empirical study of LLM drift; documents large, task-dependent behavior shifts between GPT-3.5/GPT-4 snapshots.

- **ChatLog: Recording and Analyzing ChatGPT Across Time**
  Tu, S., Li, C., Yu, J., Wang, X., Hou, L., & Li, J., 2023, arXiv:2304.14106
  [arXiv](https://arxiv.org/abs/2304.14106)
  Continuous monthly/daily monitoring dataset extending single-snapshot drift comparisons into a time series.

- **An Empirical Study of Catastrophic Forgetting in Large Language Models During Continual Fine-tuning**
  Luo, Y., Yang, Z., Meng, F., Li, Y., Zhou, J., & Zhang, Y., 2023, arXiv:2308.08747
  [arXiv](https://arxiv.org/abs/2308.08747)
  Demonstrates weight-level forgetting during fine-tuning, supporting the paper's taxonomy of drift sources.

- **A Longitudinal Study on Artificial Intelligence Adoption: Understanding the Drivers of ChatGPT Usage Behavior Change in Higher Education**
  Polyportis, A., 2024, Frontiers in Artificial Intelligence, 6, 1324398
  [DOI](https://doi.org/10.3389/frai.2023.1324398)
  Longitudinal user-behavior study cited as adjacent evidence of shifting real-world engagement with LLM tools over time.

## Methods / Algorithms

- **Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena**
  Zheng, L. et al., 2023, NeurIPS 2023 Datasets and Benchmarks Track
  [arXiv](https://arxiv.org/abs/2306.05685)
  Validates and catalogues biases in LLM-as-judge evaluation, a method the paper discusses for preference-based drift tracking.

## Evaluation Methods / Benchmarks

- **Holistic Evaluation of Language Models**
  Liang, P. et al., 2022/2023, arXiv:2211.09110; also Transactions on Machine Learning Research, 2023
  [arXiv](https://arxiv.org/abs/2211.09110)
  Standardized, multi-metric evaluation infrastructure (HELM), proposed as reusable for longitudinal drift tracking.

- **Beyond the Imitation Game: Quantifying and Extrapolating the Capabilities of Language Models**
  Srivastava, A. et al., 2022, arXiv:2206.04615; also Transactions on Machine Learning Research, 2023
  [arXiv](https://arxiv.org/abs/2206.04615)
  Large collaborative benchmark (BIG-bench) cited as an example of shared evaluation infrastructure relevant to drift measurement.
