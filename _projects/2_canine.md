---
layout: page
title: Comparative ML Architecture Analysis
description: Benchmarking CNNs vs. Classical PCA-KNN on custom datasets
img: assets/img/canine/thumbnail.jpg
importance: 2
category: work
repositories:
  - https://github.com/abrahamAlpuerto/IML_Project
---

[cite_start]This project focused on the classification of a custom-collected dataset of over 2,000 images[cite: 57]. [cite_start]Leveraging fundamental machine learning techniques, I conducted a rigorous study to explore the trade-offs between deep learning (CNNs) and classical methods (PCA + KNN) for image classification[cite: 51, 55].

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/canine/dataset_sample.jpg" title="Dataset Sample" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/canine/pca_viz.jpg" title="PCA Visualization" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/canine/confusion.jpg" title="Confusion Matrix" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [cite_start]Images were resized to 256x256 pixels to optimize computational efficiency[cite: 61]. [cite_start]The study compared CNNs against KNN, GMM, and FCNN[cite: 54, 55].
</div>

### Technical Approach
I implemented two distinct pipelines to compare performance:
1.  [cite_start]**Deep Learning:** A custom 5-layer **Convolutional Neural Network (CNN)** built in PyTorch[cite: 172].
2.  [cite_start]**Classical ML:** Dimensionality reduction using **Principal Component Analysis (PCA)** followed by **K-Nearest Neighbors (KNN)**[cite: 53, 54].

[cite_start]For the classical approach, I found that retaining **60% of the variance** via PCA yielded the optimal balance for the KNN algorithm[cite: 244].

### Results & Engineering Trade-offs
[cite_start]While the CNN achieved the highest accuracy, the comparative analysis revealed that a PCA-optimized KNN model could achieve near-SOTA performance with significantly lower computational overhead[cite: 240, 245].

| Model | Test Accuracy | Training Time |
|-------|---------------|---------------|
| **CNN** | [cite_start]**97.02%** [cite: 350] | [cite_start]35 minutes [cite: 350] |
| CNN + Augmentation | [cite_start]95.62% [cite: 350] | [cite_start]2.5 hours [cite: 350] |
| **KNN (k=1)** | [cite_start]**93.03%** [cite: 350] | [cite_start]**< 1 minute** [cite: 350] |
| GMM | [cite_start]64.02% [cite: 350] | [cite_start]< 1 minute [cite: 350] |

[cite_start]Overall, the KNN provided the best balance of accuracy (93%), ease of implementation, and minimal hyper-parameter tuning compared to the computationally expensive CNN[cite: 357].