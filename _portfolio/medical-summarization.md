---
title: "Medical Question Summarization with Flan-T5-Large & LoRA"
excerpt: "Using NLP to summarize medical reports efficiently."
header:
  image: "/assets/images/portfolio/medical-summarization/medical-sum-arch.png"
  teaser: "/assets/images/portfolio/medical-summarization/medical-sum-arch.png"
  overlay_color: "rgb(43, 0, 255)"
  overlay_filter: 0.5
  caption: "Medical Summarization Project"
sidebar:
  - title: "Role"
    text: "AI Researcher & Developer"
  - title: "Technologies"
    text: "Python, Transformers, LoRA, Hugging Face"
  - title: "Dataset"
    text: "MEQSum (1,000 medical questions)"
  - title: "Model"
    text: "Flan-T5-Large (770M params)"
  - title: "Results"
    text: "ROUGE-L: 0.7288 (vs 0.2375 baseline)"
  - title: "Code"
    text: "[GitHub Repository](https://github.com/desire-del/clinical_text_sum/tree/main)"
  - title: "Demo"
    text: "[Hugging Face Space](https://huggingface.co/spaces/autodidacte228/meq-sum-T5-lora)"
gallery:
  - url: assets/images/portfolio/medical-summarization/medical-sum-arch.png
    image_path: assets/images/portfolio/medical-summarization/medical-sum-arch.png
    alt: "Model architecture"
  - url: assets/images/portfolio/medical-summarization/result.png
    image_path: assets/images/portfolio/medical-summarization/result.png
    alt: "Evaluation results"
badges:
  - label: "Python"
    url: "https://www.python.org/"
    class: "blue"
  - label: "Transformers"
    url: "https://huggingface.co/docs/transformers/index"
    class: "yellowgreen"
  - label: "LoRA"
    url: "https://arxiv.org/abs/2106.09685"
    class: "orange"
  - label: "Flan-T5"
    url: "https://huggingface.co/google/flan-t5-large"
    class: "blueviolet"
---

## Project Overview

This project fine-tunes **Flan-T5-Large** using **LoRA (Low-Rank Adaptation)** for abstractive summarization of complex medical questions from the [MEQSum dataset](https://huggingface.co/datasets/albertvillanova/meqsum). The system generates concise, accurate summaries that retain core clinical intent while reducing trainable parameters by ~98%.

{% include badge-list.html badges=page.badges %}

## Key Contributions

- Implemented parameter-efficient fine-tuning with LoRA adapters
- Achieved **3× ROUGE score improvement** over baseline T5
- Deployed interactive demo on Hugging Face Spaces
- Optimized for clinical domain specificity

## Technical Approach

### Model Architecture
![Flan-T5 Architecture]({{ site.url }}{{ site.baseurl }}/assets/images/portfolio/medical-summarization/flan_T5.png){: .align-center}

1. **LoRA Adaptation**:
   - Trains only small low-rank matrices (query/key/value attention)
   - VRAM requirements reduced by 80% compared to full fine-tuning

2. **Flan-T5-Large**:
   - Instruction-tuned variant (512 token context)
   - Pre-trained on diverse NLP tasks

## Results & Impact

| Metric    | Baseline | Our Model | Improvement |
|-----------|----------|-----------|-------------|
| ROUGE-1   | 0.2529   | 0.7363    | +191%       |
| ROUGE-L   | 0.2375   | 0.7288    | +207%       |

**Clinical Impact**: Enables faster triage of patient questions by summarizing to essential medical intent.

## Project Links

- :octocat: [GitHub Repository](https://github.com/desire-del/clinical_text_sum/tree/main)
- 🤗 [Hugging Face Model](https://huggingface.co/spaces/autodidacte228/meqsum-lora-T5-finetuned)
- 🚀 [Live Demo](https://huggingface.co/spaces/autodidacte228/meq-sum-T5-lora)

{% include gallery caption="Project architecture and evaluation results" %}