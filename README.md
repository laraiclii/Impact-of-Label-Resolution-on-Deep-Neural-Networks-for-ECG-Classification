**Assessing the Influence of Diagnostic Label Resolution on Deep Neural Network Performance in ECG Classification**

This project investigates how the resolution of diagnostic labels—ranging from detailed 44-class disease codes to clinically meaningful severity tiers—affects the performance of deep learning models for ECG classification. In collaboration with a cardiologist, we mapped conditions into both 3-tier and 4-tier severity groupings and trained identical 1D ResNet models on the SPH dataset, with external evaluation on PTB-XL.

Findings show that severity-based labels improve robustness, interpretability, and generalization across datasets, making them particularly valuable for general practitioners, where the priority is assessing urgency rather than naming every condition.

The repository provides:
ECG_classification.ipynb — preprocessing, training, and evaluation pipeline (fully reproducible)
Pretrained models — fine-grained and severity-tiered
Bachelor’s thesis — complete paper of the study and its implications


