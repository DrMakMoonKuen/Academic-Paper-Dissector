# 🧪 Walkthrough Example – Academic Paper Dissector

**Paper Title:** *Advancing Real-time Pandemic Forecasting Using Large Language Models (PandemicLLM)*  
**Source:** arXiv:2311.00604  
**Link:** [https://arxiv.org/abs/2311.00604](https://arxiv.org/abs/2311.00604)  
**Authors:** Zhang et al.

---

## 🧠 Academic Paper Dissector Template – Completed Example

### 1. Abstract (≤50 words)
PandemicLLM transforms pandemic forecasting into a language modeling task using multimodal inputs (e.g., genomic, policy). With a 20% accuracy improvement over LSTM baselines, it enables robust, real-time COVID-19 predictions and adaptation to new variants without retraining.

### 2. Keywords
- Pandemic forecasting  
- Large language models  
- Multi-modal learning  
- COVID-19 prediction  
- Zero-shot inference  
- Public health AI

---

## PART I: FOUNDATIONS

### 3. Introduction & Background (≤50 words)
Pandemic forecasting traditionally relies on structured models that falter with unstructured or rapidly evolving data. LLMs, with their language reasoning capability, offer a way to integrate diverse pandemic signals (e.g., policies, genomic variants) via prompt engineering.

### 4. Problem Statement
Conventional forecasting models like LSTM, ARIMA, or SEIR struggle to incorporate diverse, real-time pandemic data (e.g., genomic updates, behavioral policy shifts). These models require retraining and lack interpretability or generalizability.

### 5. Research Questions
- Can LLMs effectively forecast pandemic trends using textual prompts?  
- How do LLM-based models compare to traditional forecasting models?  
- Can zero-shot or few-shot inference generalize across variants or regions?

### 6. Research Objectives
- Build a real-time, generalizable pandemic forecasting model using LLMs.  
- Evaluate forecasting accuracy versus traditional baselines.  
- Demonstrate adaptability without retraining.

### 7. Hypotheses
- H1: Text-based LLM prompts can yield competitive pandemic forecasting accuracy.  
- H2: A well-designed prompt strategy improves zero-shot performance.  
- H3: Confidence scores from LLM outputs correlate with forecasting reliability.

---

## PART II: METHODS & RESULTS

### 8. Methodology
The authors reformulate time-series forecasting as a language problem using GPT-like models. The architecture fuses structured signals (e.g., hospitalization data) with unstructured ones (e.g., policy changes), converted into natural language prompts. A GRU encoder compresses prior data, which feeds into the LLM.

### 9. Data Strategy
- **Sources:** U.S. COVID-19 hospitalization data (HHS Protect), genomics (Nextstrain), policies (CDC, state-level mandates)  
- **Time span:** 104 weeks across all 50 U.S. states  
- **Preprocessing:** Data normalized and converted to text prompts. No fine-tuning was performed — only zero-shot or few-shot reasoning.

### 10. Results
- **Accuracy:** Achieves 56% accuracy in 1-week-ahead forecasting (20% higher than LSTM).  
- **Trustworthiness:** Confidence scores align with prediction accuracy.  
- **Adaptability:** Maintains performance across emerging variants like BQ.1, even without retraining.  
- **Ablation tests:** Show prompt design contributes significantly to performance gains.

---

## PART III: ANALYSIS & EXTENSION

### 11. Strengths
- First model to apply LLMs to pandemic forecasting.  
- Interpretable outputs via ordinal classes and confidence scores.  
- Avoids retraining, enabling scalable deployment in evolving crises.

### 12. Limitations
- Uses a 70B model, which is not practical for many public health deployments.  
- Only validated on U.S. COVID-19 data — global generalizability unknown.  
- No detailed explainability methods (e.g., attention maps) for trust audit.

### 13. Conclusion
PandemicLLM shows that LLMs can convert forecasting into a reasoning task using plain-text prompts. It balances performance, adaptability, and interpretability in a domain where data types are often misaligned. The work paves the way for prompt-based reasoning in other forecasting problems.

### 14. Proposed Follow-Up Study
**Title:** *PandemicLLM-2: A Federated Prompting System for Global Outbreak Monitoring*  
- **Goal:** Apply federated learning to incorporate global data without privacy breaches.  
- **Upgrade:** Distill the 70B model to a 7B efficient version.  
- **Addition:** Add attention heatmaps to explain which prompts drive predictions.  
- **Hypothesis:** Prompt-based federated learning increases cross-border generalizability while preserving interpretability.

---
