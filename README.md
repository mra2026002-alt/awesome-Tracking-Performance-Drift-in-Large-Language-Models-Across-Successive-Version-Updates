# Awesome Tracking Performance Drift in Large Language Models Across Successive Version Updates

A curated collection of research papers, datasets, tools, implementations, and learning resources on tracking performance ("behavior") drift in large language models across successive version updates — built from an AI-assisted literature review, an independent citation-integrity audit, and manually verified external resources.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Curated Research Papers](#curated-research-papers)
  - [Survey and Review Papers](#survey-and-review-papers)
  - [Foundational Papers](#foundational-papers)
  - [Recent Research Papers](#recent-research-papers)
  - [Methods / Algorithms](#methods--algorithms)
  - [Evaluation Methods / Benchmarks](#evaluation-methods--benchmarks)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

## Overview

Large language models (LLMs) deployed as commercial services are updated frequently, but the substance of these updates is rarely disclosed to downstream users. A growing body of empirical work shows that model behavior on identical prompts can shift markedly between versions — sometimes improving on one task while degrading on another within the same release cycle. This phenomenon, known as "performance drift" or "behavior drift," connects to a decades-old body of work on concept drift in classical machine learning, but LLM-specific drift introduces new challenges: drift can arise from weight-level retraining and fine-tuning, system-level changes such as hidden system prompts or moderation layers, or even from the degradation of the benchmarks used to measure it (benchmark contamination).

Tracking drift matters because it is simultaneously a reproducibility problem (a benchmark score reported today may not describe the model a reader encounters months later), an engineering-reliability problem (production systems relying on specific model behaviors can silently break), and a governance problem (without disclosure norms similar to model cards, external stakeholders cannot audit what changed or why). This repository organizes the literature and tooling around this problem — covering longitudinal benchmark replays, holistic multi-metric evaluation frameworks, LLM-as-judge preference tracking, and contamination-resistant benchmarking — with the goal of supporting rigorous, versioned tracking of LLM behavior over time.

## AI-Assisted Research Paper

**Tracking Performance Drift in Large Language Models Across Successive Version Updates**

This paper synthesizes the emerging literature on LLM performance drift, developing a taxonomy of drift sources (weight-level, system-level, and evaluation-level), surveying current monitoring approaches (longitudinal benchmark replays, HELM-style holistic evaluation, LLM-as-judge tracking, and model-card-style disclosure), and identifying research gaps including the need for contamination-resistant benchmarks, formal drift-detection statistics, and causal attribution methods.

[View Paper](paper/Ai_Assisted_Research_Paper.pdf)

## Citation Integrity Audit

All references and factual claims cited in the accompanying research paper were manually cross-checked for accuracy, including verifying author names, publication years, venues, and DOIs against original sources such as arXiv, Crossref, and Google Scholar. No AI-generated citation was accepted without independent verification.

[View Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

## Curated Research Papers

See [references/references.md](references/references.md) for the full list with descriptions and links. Summary by category:

### Survey and Review Papers
- A Survey on Concept Drift Adaptation (Gama et al., 2014)
- Benchmark Data Contamination of Large Language Models: A Survey (Xu et al., 2024)

### Foundational Papers
- Model Cards for Model Reporting (Mitchell et al., 2019)
- Training Language Models to Follow Instructions with Human Feedback (Ouyang et al., 2022)

### Recent Research Papers
- How Is ChatGPT's Behavior Changing Over Time? (Chen et al., 2023)
- ChatLog: Recording and Analyzing ChatGPT Across Time (Tu et al., 2023)
- An Empirical Study of Catastrophic Forgetting in Large Language Models During Continual Fine-tuning (Luo et al., 2023)
- A Longitudinal Study on Artificial Intelligence Adoption (Polyportis, 2024)

### Methods / Algorithms
- Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena (Zheng et al., 2023)

### Evaluation Methods / Benchmarks
- Holistic Evaluation of Language Models (Liang et al., 2022)
- Beyond the Imitation Game: Quantifying and Extrapolating the Capabilities of Language Models (Srivastava et al., 2022)

## Datasets

See [datasets/datasets.md](datasets/datasets.md) for full details, sources, and links: ChatLog, HELM benchmark data, and BIG-bench.

## Tools and Libraries

See [tools/tools.md](tools/tools.md) for full details and links: HELM, FastChat, FastChat LLM Judge (MT-Bench), LLM Decontaminator, and BIG-bench.

## GitHub Implementations

See [implementations/github-repositories.md](implementations/github-repositories.md) for full details and links: ChatLog, HELM, FastChat / LLM Judge, LLM Decontaminator, and BIG-bench.

## Tutorials and Learning Resources

- ## Tutorials and Learning Resources

Authoritative learning material for understanding LLM evaluation, benchmarking, and performance drift — each verified as a genuine, currently accessible resource.

- **Hugging Face LLM Course — Evaluation Chapter**
  [huggingface.co/learn/llm-course/en/chapter11/5](https://huggingface.co/learn/llm-course/en/chapter11/5)
  A free, official tutorial covering standard automatic benchmarks (MMLU, TruthfulQA, etc.), their limitations, and how to build custom evaluations — foundational background for understanding what a drift study is actually measuring.

- **Hugging Face Open-Source AI Cookbook — Using LLM-as-a-Judge**
  [huggingface.co/learn/cookbook/llm_judge](https://huggingface.co/learn/cookbook/llm_judge)
  A hands-on, code-along notebook explaining how to set up an LLM-as-judge evaluation pipeline correctly, directly implementing the methodology from Zheng et al. (2023) referenced in the accompanying paper.

- **HELM (Holistic Evaluation of Language Models) — Official Documentation**
  [crfm-helm.readthedocs.io](https://crfm-helm.readthedocs.io/)
  Stanford CRFM's official documentation for installing and running the HELM benchmark suite, the standardized multi-metric evaluation framework discussed in Section 4.2 of the accompanying paper.

- **Stanford CS336: Language Modeling from Scratch**
  [cs336.stanford.edu](https://cs336.stanford.edu/)
  A graduate-level Stanford course (taught by Percy Liang, Tatsu Hashimoto, and others) walking through the full LLM lifecycle — data, training, and evaluation — providing the technical grounding needed to understand *why* successive model versions can behave differently.

- **Mistral AI — Guide to Evaluating LLMs**
  [docs.mistral.ai/guides/evaluation](https://docs.mistral.ai/guides/evaluation/)
  An official, practitioner-oriented guide covering metrics-based, LLM-based, and human-based evaluation methods with runnable Python notebooks, useful for understanding the practical toolkit behind longitudinal benchmark replay (Section 4.1 of the paper).

## License

This repository's original content (the AI-assisted research paper, citation integrity audit, and curation write-ups) is released under the MIT License. See [LICENSE](License) for full terms and scope, including which external content it does not cover.
