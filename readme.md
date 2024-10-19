# Generative Adversarial Networks for Time Series Synthetic Data Generation for CNC Machines

## Description
This project implements a **transformer-based Generative Adversarial Network (GAN)** for generating synthetic time-series data related to the performance of CNC machines. The generated data includes attributes like movement (X, Y, Z coordinates), force, and velocity of the spindle, which can be used to analyze and predict the machine's energy requirements. By synthesizing this data, it becomes possible to improve energy efficiency and predict future performance trends without needing constant physical measurements from the machine.

## Features

- **Transformer-based GAN** for realistic time-series data generation.

- **Metrics for evaluation**:
  - **Descriptive**: Comparison of statistical properties between real and synthetic data. The goal is to compute  how well the discriminator can distinguish between real and synthetic data. The discriminative score is defined as the absolute difference between the classification accuracy and 0.5. An accuracy close to 0.5 indicates that the discriminator cannot distinguish real from synthetic data, which is ideal in a well-trained GAN.
  - **Predictive**: Assessment of the ability to predict future machine performance using synthetic data. The predictive score is a critical metric for assessing and validating the effectiveness of generative models, particularly in time-series contexts. It helps ensure that the synthetic data produced is reliable and representative of the original data,
  - **Frechet Inception Score (FIS)**: For assessing the quality of the generated data. It measure the similarity between the real and synthetic datsets.

- **Visualizations**:
  - **PCA (Principal Component Analysis)**
  - **t-SNE (t-distributed Stochastic Neighbor Embedding)**

- **Model Performance Tracking**: We are utilising the weights and biases library to track the performance of our model. With this, we are getting a dashboard with all the evaluation metrics and other performance measures.

## Structure:

The code is structured into following main components:

model: Contains the transformer-based GAN architecture.
metrics: Implements the evaluation metrics (descriptive, predictive, and Frechet Inception Score).
main: This script serves as the entry point for the project, orchestrating the entire pipeline for synthetic data generation, evaluation, and visualization.


To run the project locally, follow these steps:

1. Clone the repository:
   
   git clone <repository-url>
   cd <project-folder>

2. Modify the configuration files if needed (for custom datasets, hyperparameters, etc.).

3. Run the main script:

    python main.py  


This will generate synthetic data, evaluate it against the real data using the metrics mentioned above and produce visualizations (PCA and t-SNE) comparing the datasets.
