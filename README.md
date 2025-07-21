# 🫀 ECG Label Granularity & Deep Learning  
**Assessing the Influence of Diagnostic Label Resolution on Deep Neural Network Performance in ECG Classification**

---

## 📌 Overview

This study explores how varying levels of diagnostic label granularity—from detailed disease-specific codes to broader severity-based categories—impact the performance, generalizability, and interpretability of deep learning models for electrocardiogram (ECG) classification.

We employed a 1D ResNet architecture trained on the SPH dataset (25,770 ECG recordings) and evaluated its generalization on the external PTB-XL dataset using three distinct labeling strategies:

- **Fine-grained (44-class):** American Heart Association (AHA) diagnostic codes  
- **Coarse-grained (3-tier):** `Normal`, `Monitor`, `Serious`  
- **Intermediate (4-tier):** `Normal`, `Mild`, `Moderate`, `Serious`

---

## 💡 Key Findings

- 🥇 **3-tier labeling** yielded the most robust performance:  
  - 87% internal accuracy (F1 = 0.87)  
  - 60.5% external accuracy (PTB-XL)
  
- 🧠 **4-tier classification** maintained interpretability and clinical relevance, with only a 2% drop in internal accuracy compared to the 3-tier model.

- 🚨 **44-class labeling** exhibited severe generalization issues, particularly with rare pathologies (external F1 = 0), likely due to overfitting and class imbalance.

- 🔍 **Grad-CAM analysis** revealed that:  
  - Tiered models consistently attended to diagnostically relevant waveform segments.  
  - Fine-grained models often focused on noisy or irrelevant signal components.

---

## 🏥 Implications for Clinical Practice

The results support the implementation of a **hierarchical two-stage diagnostic framework**:

1. **Initial triage** in primary care settings using coarse severity labels to prioritize urgency.
2. **Detailed diagnosis** using fine-grained labels when additional precision is clinically warranted.

This approach enhances model robustness, mitigates overfitting, and improves interpretability—making it well-suited for deployment in **AI-assisted Holter monitors for primary care workflows**.

