# Text Generation using Vanilla RNN, LSTM, and GRU

## Project Overview

This project focuses on implementing and comparing three recurrent neural network architectures for text generation:

* Vanilla RNN
* LSTM (Long Short-Term Memory)
* GRU (Gated Recurrent Unit)

The objective is to learn how sequence models capture grammar, contextual dependencies, and sentence structure to generate meaningful text sequences.

---

## Problem Statement

Design and implement deep learning models capable of learning the underlying structure, grammar, and contextual dependencies of a given text corpus to generate coherent and meaningful text sequences.

The performance of Vanilla RNN, LSTM, and GRU models is compared based on:

* Training Loss
* Generated Text Quality
* Context Retention
* Long-Term Dependency Learning
* Memory Handling Capability

---

## Dataset / Corpus

A custom text corpus related to Artificial Intelligence and Deep Learning was used for training.

Sample topics included:

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Natural Language Processing
* Sequence Modeling
* Text Generation

The corpus was intentionally kept small to demonstrate how recurrent architectures learn sequential patterns from limited textual data.

---

## Project Workflow

### 1. Text Preprocessing

* Tokenization using Keras Tokenizer
* Vocabulary creation
* N-gram sequence generation
* Sequence padding
* Input-output preparation for next-word prediction

### 2. Model Development

Three sequence models were implemented:

#### Vanilla RNN

* Embedding Layer
* SimpleRNN Layer
* Dense Output Layer

#### LSTM

* Embedding Layer
* LSTM Layer
* Dense Output Layer

#### GRU

* Embedding Layer
* GRU Layer
* Dense Output Layer

---

## Experimental Modifications

The following improvements were implemented beyond the base notebook:

* Custom AI-related text corpus
* Embedding dimension increased from 32 → 64
* Hidden units increased from 64 → 128
* Training epochs increased from 100 → 200
* Generated sequence length increased from 5 → 10 words

These modifications were introduced to evaluate how model capacity influences text generation performance.

---

## Training Loss Comparison

Training loss was monitored throughout the learning process to compare how efficiently each architecture learned patterns from the corpus.

The comparison highlighted differences in convergence behavior among RNN, LSTM, and GRU architectures.

---

## Generated Text Analysis

Generated outputs were evaluated using qualitative analysis rather than relying solely on numerical metrics.

Evaluation criteria included:

* Sentence coherence
* Context retention
* Repetition patterns
* Semantic relevance

Key observations:

* Vanilla RNN learned short-term patterns effectively but occasionally lost contextual consistency.
* LSTM demonstrated memory retention capabilities but showed repetitive word generation due to the limited corpus size.
* GRU maintained contextual flow while using a simpler architecture and fewer gating mechanisms.

---

## Experimental Result Validation

Although some models achieved lower training loss, generated text quality did not always improve proportionally.

This demonstrates that training loss alone is insufficient for evaluating language generation models.

Qualitative inspection of generated sequences revealed that coherence, repetition, and contextual relevance must also be considered when assessing model performance.

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib

---

## Limitations

* The corpus size is relatively small.
* Limited vocabulary restricts language diversity.
* Training loss alone cannot fully capture text quality.
* Generated text evaluation remains partially subjective.
* Larger datasets would likely improve model generalization and coherence.

---

## Conclusion

This project successfully implemented and compared Vanilla RNN, LSTM, and GRU architectures for text generation.

The experiment demonstrated how different recurrent architectures learn sequential patterns and contextual dependencies from text data.

The results highlight the importance of combining quantitative metrics with qualitative analysis when evaluating text generation systems.

Future work may include larger text corpora, longer sequence lengths, and advanced evaluation metrics to further improve generated text quality.

---

## Author

**Pavika Yadav**

B.Tech CSE (Data Science)

Amity University

Machine Learning & Deep Learning Internship – Celebal Technologies
