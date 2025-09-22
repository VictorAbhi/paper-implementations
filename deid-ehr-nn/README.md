# EHR De-identification with Neural Networks

This repository contains an implementation of the methodology from the research paper *"De-identification of electronic health record using neural network"* (Scientific Reports, 2020, University of Manitoba) for detecting Protected Health Information (PHI) in electronic health records (EHRs) using BIOES tagging. The project leverages Recurrent Neural Networks (RNNs) with GloVe and character embeddings, inspired by the paper's GRU, stacked RNNs, and CRF-based approach. This is solely for my learning purposes,

## Project Overview

- **Goal**: Automate PHI de-identification in EHRs while preserving data utility, achieving high recall and F1 scores.
- **Dataset**: Synthetic dataset with PHI elements (e.g., names, dates) due to challenges in accessing real-world health data.
- **Approach**: Implements preprocessing (BIOES tagging, vocabularies, padded sequences), fixed (GloVe) and character embeddings, and prepares for RNN training.

## Features
- Preprocesses EHR text into BIOES-tagged sequences.
- Builds vocabularies for tokens and tags, mapping to numerical indices.
- Applies GloVe embeddings (300d) and character embeddings for robustness.
- Supports padded sequences for batch processing with RNNs.

## Getting Started

### Prerequisites
- Python 3.8+
- Required libraries: `pandas`, `numpy`, `torch`, `tensorflow`, `sklearn`, `transformers`