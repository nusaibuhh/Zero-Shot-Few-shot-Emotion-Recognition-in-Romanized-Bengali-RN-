# Zero-Shot-Few-shot-Emotion-Recognition-in-Romanized-Bengali-RN-


This repository contains the benchmarking suite, fine-tuning pipelines, and architectural experiments for evaluating Natural Language Inference (NLI) and transformer-based emotion classification models on code-mixed, low-resource Banglish text.

---

## 📊 Evaluation & Benchmarking

### 1. Zero-Shot Benchmarking
We systematically evaluated **9 pretrained NLI and emotion classification models** to identify critical failure modes in handling code-mixed, low-resource linguistic inputs. The evaluated architectures include:
* **DeBERTa** variants
* **BART-MNLI**
* **XLM-RoBERTa**
* **DistilBERT** variants

#### Key Findings:
* **Performance Ceiling:** The top-performing zero-shot NLI model achieved a peak accuracy of only **36.8%**.
* **Systematic Bias:** Majority-class bias was highly prevalent on unfamiliar linguistic input. Most models heavily defaulted to mislabeling Banglish text as `"neutral"` or `"surprise"`.

### 2. Cross-Lingual Fine-Tuning
To mitigate zero-shot limitations, we fine-tuned **XLM-RoBERTa** and **DistilBERT** on a combined English-Bengali dataset.

| Phase | Top Model Accuracy |
| :--- | :--- |
| **Zero-Shot Baseline** | 36.8% |
| **Cross-Lingual Fine-Tuned** | **48.1%** |

> ⚠️ **Note:** While fine-tuning yielded a notable performance increase, a significant accuracy gap persists for low-sample emotion classes.

---

## 🚀 Active Development: Next-Gen Architectures

To address the performance bottlenecks inherent in low-sample emotion classes, current development focuses on moving past standard fine-tuning workflows via:
* **Self-Supervised Learning:** Leveraging unlabelled data to build more robust cross-lingual representations.
* **Contextual Learning Paradigms:** Enhancing structural understanding of code-mixed syntax.
* **Kolmogorov-Arnold Network (KAN) Architectures:** Exploring KAN-based neural layers to optimize weight-function learning for non-linear, low-resource linguistic inputs.
