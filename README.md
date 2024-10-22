# Uncertainty-Aware Segmentation Quality Prediction: Bayesian Modeling with Comprehensive Evaluation and Interpretation

Image segmentation is crucial in computational biomedical image analysis, often evaluated using metrics like the Dice coefficient during training and validation. However, assessing segmentation quality in clinical settings without manual annotations poses significant challenges, creating barriers to model adoption when reliability indicators are absent.

This project introduces two segmentation quality prediction frameworks:

**Framework 1:** Processes predicted segmentation and uncertainty maps.

**Framework 2:** Integrates the original input image, uncertainty maps, and predicted segmentation maps.

We implement Bayesian versions of two benchmark semantic segmentation models—SwinUNet and Feature Pyramid Network (FPN) with ResNet50—utilizing three Bayesian modeling approaches: Monte Carlo Dropout (MCD), Ensemble, and Test Time Augmentation (TTA).

We evaluate four uncertainty estimates:

1. Confidence Map

2. Entropy

3. Mutual Information

4. Expected Pairwise Kullback-Leibler (EPKL) Divergence

These are assessed on 2D skin lesion and 3D liver segmentation datasets, with a focus on their correlation with segmentation quality metrics. Additionally, we propose an aggregation strategy that combines multiple uncertainty estimates into a single score per image, providing a more robust assessment of segmentation quality compared to individual evaluations.

For model interpretability, we employ gradient-based methods like Grad-CAM and feature embedding analysis through UMAP, ensuring a comprehensive understanding of the model's behavior and reliability.
