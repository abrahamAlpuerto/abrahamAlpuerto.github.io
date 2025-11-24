---
layout: page
title: Quantitative Stock Forecasting Engine
description: LSTM & Attention-based model for time-series analysis
img: assets/img/stock/thumbnail.jpg
importance: 1
category: work
---

**Role:** Lead Quantitative Researcher & Co-Trader

This project is a specialized time-series forecasting model designed to identify and predict price changes in the equity market. Developed as a collaborative initiative, this engine was deployed within a private trading group consisting of myself and close associates to automate and validate trading signals.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/pipeline.jpg" title="Data Pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/model_arch.jpg" title="LSTM Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: The data processing pipeline. Right: The LSTM/Attention model architecture.
</div>

### Live Performance & Results
Unlike purely theoretical models, this engine was put to the test with real capital.
* **Return on Investment:** Achieved a **660% return** on my own personal capital over a 2-month period, growing a test account from **$300 to $2,000**.
* **Group Deployment:** The model's signals were utilized by a small team of peer traders, allowing us to crowdsource strategy validation and execute coordinated entries on volatile equities.

### Technical Architecture
The core of the system is a custom deep learning model built with **TensorFlow** and **Keras**.
* **Model Architecture:** Utilizes **Long Short-Term Memory (LSTM)** networks combined with **Attention mechanisms** to capture temporal dependencies and weigh the importance of specific time steps.
* **Feature Engineering:** The system aggregates over a decade of daily time-series data, creating **18 distinct predictive indicators** to enrich the feature space beyond simple price/volume data.

### Data Pipeline
Handling financial data requires precision. I engineered a pipeline to:
1.  Aggregate daily time-series data for **50+ equities**.
2.  Clean and preprocess data to handle missing ticks and splits.
3.  Perform rigorous backtesting to validate strategy performance against market benchmarks.