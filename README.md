# EEG-Based Emotion Recognition with Hybrid GNN Models

## Overview

This project explores emotion recognition using physiological signals, specifically **Electroencephalogram (EEG)** data. It aims to test and enhance hybrid architectures that integrate **Graph Neural Networks (GNNs)** with **Transformers** and **Recurrent Neural Networks (RNNs)** for improved emotion classification. By leveraging GNNs' ability to capture spatial relationships between EEG channels, combined with the temporal strengths of RNNs and the contextual power of Transformers, the project sets a foundation for advanced emotion recognition techniques.

## Objectives

- Implement and evaluate **GNN-based models** on the **DEAP dataset**, transforming EEG signals into graph structures.
- Integrate **hybrid architectures** combining GNNs with RNNs and Transformers.
- Address challenges such as data variability, noise, and the scalability of EEG-based systems.
- Benchmark the performance of hybrid models compared to standalone architectures.

## Dataset

The project uses the [DEAP dataset](https://www.eecs.qmul.ac.uk/mmv/datasets/deap/), a widely used dataset for EEG-based emotion recognition. DEAP consists of:
- **32 EEG channels** recorded from 32 participants.
- Emotional states rated on **Valence**, **Arousal**, **Dominance**, and **Liking** scales.

### Preprocessing Steps:
1. Select the first **32 EEG channels**.
2. Extract **statistical features** (mean, standard deviation, kurtosis, skewness).
3. Compute **frequency band powers** (delta, theta, alpha, beta, gamma) using the Welch method.
4. Transform EEG signals into graph representations, with nodes representing EEG channels.

## Models

### 1. **Graph Neural Networks (GNNs)**  
- Captures spatial dependencies between EEG channels.
- Implements **GCNConv** layers with global pooling.

### 2. **Hybrid Models**  
- **GNN + RNN**: Combines GNNs with RNNs to capture temporal dependencies in the EEG data.
- **GNN + Transformer**: Leverages Transformers for contextual learning alongside spatial relationships modeled by GNNs.

### 3. **Baseline Models**  
- Standalone RNNs and Transformers are evaluated for comparison.

## Results

- **GNN-based models** demonstrated improved performance in capturing spatial relationships in EEG data.
- **Hybrid architectures** combining GNNs with RNNs/Transformers achieved higher accuracy and robustness in emotion classification.
- Key challenges addressed include **graph representation of EEG data** and handling **data imbalance** in emotional labels.

## Usage

### 1. Clone the Repository:
```bash
git clone https://github.com/kdalampekis/Deap_dataset
cd notebooks
