# machine_learning
Vision–Language Models for Lung Disease Detection in 3D CT Scans

Multimodal pipelines (CNN, CNN+BioViL, CNN+MedCLIP) for classifying lung conditions — COVID-19, Viral Pneumonia, Lung Opacity, and Normal — from CT scan slices, with segmentation-aware inputs, robust evaluation (ROC, confusion matrices), and Out-of-Distribution (OOD) stress tests.
This repository is distilled from our course project report and results.

🔎 Overview

**Problem:** Early, accurate detection of lung pathologies in CT is hard; radiologist capacity is limited.

Approach:
**Baseline:** two-channel CNN (stacked CT slice + lung mask).
Hybrid 1: CNN + BioViL (vision–language embeddings fused with CNN features).
Hybrid 2: CNN + MedCLIP (contrastive visual embeddings fused with CNN features).

**Datasets:**
COV19-CT-DB (CT slices + segmentation masks + metadata).
COVID-19 Chest X-ray (for auxiliary analysis/experiments).

**Highlights:**
Hybrid CNN+BioViL improves accuracy and per-class AUC versus CNN baseline.
Analysis includes OOD robustness (noise/blur/brightness), uncertainty, and double-descent observations.
