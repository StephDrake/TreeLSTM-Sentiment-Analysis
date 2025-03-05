# TreeLSTM-Sentiment-Analysis

# Roots of Sentiment: Tree-LSTMs vs Traditional Models in Semantic Representation

This repository contains the code and experiments for **"Roots of Sentiment: Tree-LSTMs vs Traditional Models in Semantic Representation"**. The project investigates how hierarchical models like Tree-LSTMs compare to traditional sequential models in sentiment classification tasks. 

## Overview

Understanding sentence meaning is crucial in **Natural Language Processing (NLP)**, and various models have been developed to encode both syntax and semantics. This study compares three major approaches:

- **Bag-of-Words (BoW) & Deep Continuous BoW (DCBOW)** – Ignore word order but are computationally efficient.
- **Long Short-Term Memory (LSTM)** – Captures sequential dependencies and mitigates the vanishing gradient problem.
- **Tree-LSTM** – Leverages hierarchical structures to encode compositional semantics.

The study evaluates these models on the **Stanford Sentiment Treebank (SST)** dataset and investigates key research questions, including the role of word order, sentence length effects, and the impact of node-level supervision in hierarchical models.

## Results Summary

| Model                          | Accuracy (Mean ± SD) |
|--------------------------------|----------------------|
| BoW                            | 0.25 (±0.01)        |
| CBOW                           | 0.34 (±0.013)       |
| Deep CBOW (pre-trained)        | 0.44 (±0.08)        |
| LSTM (fixed GloVe)             | 0.46 (±0.006)       |
| N-ary Tree-LSTM (fixed GloVe)  | 0.47 (±0.005)       |
| Supervised N-ary Tree-LSTM     | **0.50 (±0.004)**   |

The results indicate that **hierarchical models outperform traditional sequential models**, especially for longer and syntactically complex sentences. Node-level supervision further improves accuracy.
