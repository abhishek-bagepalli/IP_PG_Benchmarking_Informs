# LLM Risk Benchmarking Framework

A comprehensive framework for evaluating vulnerabilities in open-source Large Language Models (LLMs), developed in collaboration with Prediction Guard.

## Overview

As Large Language Models (LLMs) become increasingly integrated into enterprise applications, understanding and mitigating risks such as prompt sensitivity, prompt injection, factual inconsistency, and toxic outputs becomes crucial. This framework addresses the gap in traditional evaluations that primarily focus on accuracy and fluency, providing a more holistic approach to risk assessment.

## Project Goals

- Quantify LLM reliability using adversarial prompt variations (e.g., synonyms, typos)
- Use open datasets like SQuAD and Jigsaw for evaluation
- Introduce custom metrics like Prompt Deviation Rate (PDR)
- Compare semantic drift using LLM-as-a-Judge and embedding-based cosine similarity
- Benchmark performance of 8B vs. 70B models in terms of safety, cost, and factuality

## Key Features

- **Adversarial Testing**: Comprehensive test cases targeting model robustness through:
  - Synonym substitutions
  - Typo variations
  - Injection attacks

- **Model Evaluation**: Benchmarking of prominent LLaMA-based models:
  - Hermes-2-Pro-LLaMA-3-8B
  - Hermes-3-LLaMA-3.1-70B

- **Innovative Metrics**:
  - Prompt Deviation Rate (PDR)
  - Embedding-based semantic drift assessment
  - LLM-as-a-judge evaluation methods
  - Google's Perspective API for toxicity evaluation
  - Human-aligned test sets for factual consistency

## Technologies Used

- Python 3.10+
- Transformers (Hugging Face)
- Sentence Transformers
- Open-source LLaMA models
- Perspective API for toxicity detection
- OpenAI API (optional for LLM-as-a-Judge comparison)

## Key Findings

- The smaller 8B model (Hermes-2-Pro) demonstrates:
  - Superior factual accuracy
  - Better resilience to prompt injection
  - More suitable for high-risk enterprise settings

- The larger 70B model shows:
  - Higher recall for toxicity detection
  - Better performance for moderation and safety layers

## Cost Efficiency

The framework leverages:
- Open-source models
- Cloud GPUs (e.g., A100s at $3.40/hour)
- 95% cost reduction compared to API-based pipelines (e.g., GPT-3.5 Turbo)

## How to Use

1. Clone the repository
2. Run the `SQuAD.ipynb` notebook
3. Evaluate LLM responses to original and adversarially modified prompts
4. Analyze PDR and similarity metrics to assess model robustness

## Use Cases

- Enterprise risk assessment
- Model selection for specific applications
- Safety layer development
- Cost-effective evaluation pipelines for startups and enterprises

## Citation

If you use this framework, please cite our INFORMS Analytics+ 2025 project or contact abagepal@purdue.edu

## Acknowledgments

- Prediction Guard for collaboration
- Google's Perspective API for toxicity evaluation
- The open-source community for model contributions 
