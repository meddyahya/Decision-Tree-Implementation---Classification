# Decision Tree Classification from Scratch

This repository contains a **from-scratch implementation** of the **ID3 decision tree algorithm** for classification, including handling of both categorical and continuous features, adaptive threshold selection using statistical criteria, and pruning techniques to improve generalization.

Unlike using library implementations (e.g., scikit-learn), this project builds the classifier manually, offering insight into the core logic of decision trees.

## Table of Contents

- [About](#about)  
- [Key Features](#key-features)  
- [Results](#results)
- [Installation](#installation)

  ## About

Decision trees are powerful yet interpretable classification models. This project implements the **ID3 algorithm** from first principles, including:

- Entropy and information gain for splits  
- Threshold selection for continuous attributes  
- Handling of discrete/categorical attributes  
- Pre-pruning and post-pruning to reduce overfitting

The model is applied to diabetes prediction and benchmarked with cross-validation.

## Key Features

- **Pure Python implementation** (no scikit-learn for training)  
- Adaptive thresholding for continuous variables  
- Entropy and information gain calculation  
- Optional **pre-pruning** and **post-pruning**  
- 5-fold cross-validation support  
- Performance evaluation metrics

## Results
Metrics of the baseline model (without improvements such as pruning techniques):
| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| 0     | 0.99850   | 0.99800 | 0.99825 |
| 1     | 0.99800   | 0.99850 | 0.99825 |

Metrics of the model after **pre-pruning**
| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| 0     | 1.00000   | 0.87077 | 0.93092 |
| 1     | 0.85438   | 1.00000 | 0.92147 |

Metrics of the model after **post-pruning**
| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| 0     | 0.93 | 0.87 | 0.90 |
| 1     | 0.86 | 0.92 | 0.89 |

## Installation
```bash
git clone https://github.com/meddyahya/Decision-Tree-Implementation---Classification.git
cd Decision-Tree-Implementation---Classification
pip install -r requirements.txt
```
