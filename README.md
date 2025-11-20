Abstract

This project presents the design and implementation of a Machine Learning–based Intrusion Detection System (IDS) enhanced through a novel activation function termed Malleable Activation Function (MAF). The IDS aims to accurately distinguish between benign and malicious network traffic by leveraging improved nonlinear transformation capabilities introduced by MAF. The work explores the theoretical properties of MAF, compares its performance with conventional activation functions, and evaluates its effectiveness on cybersecurity benchmark datasets.

🎯 Objective

The primary objective of this project is to investigate whether a custom activation function can enhance learning efficiency and detection accuracy in IDS models. Specifically, the project aims to:

Formulate and implement the MAF activation function.

Integrate MAF into a neural network classifier.

Analyze its impact on feature learning and gradient behavior.

Evaluate the IDS performance on standard intrusion detection datasets.

Compare MAF against widely used activation functions such as ReLU, Sigmoid, and Tanh.

🧠 Theoretical Foundation
1. Intrusion Detection Systems (IDS)

An IDS monitors network activity to detect unauthorized access, anomalies, and attacks. Machine Learning–based IDS solutions utilize statistical learning to classify traffic patterns as normal or malicious.

2. Motivation for a Custom Activation Function

Traditional activations (ReLU, Sigmoid, Tanh) suffer from:

Vanishing/exploding gradients

Dead neurons (ReLU)

Limited adaptability to non-linearities in noisy network traffic

Cybersecurity datasets often contain:

Highly imbalanced attack classes

High-dimensional features

Noisy or redundant information

Hence, a more flexible activation mechanism can improve the model's representational power.

3. Malleable Activation Function (MAF)

MAF is introduced as an adaptive nonlinear transformation function designed to:

Provide controlled curvature for better gradient flow

Reduce neuron stagnation

Improve learning stability in deep layers

Enhance representation of subtle attack signatures

The function's theoretical design focuses on balancing smoothness and responsiveness to input variations.

🏗️ Methodology
1. Dataset Preparation

Benchmark datasets considered: CICIDS, KDD, or UNSW-NB15

Steps performed:

Data cleaning

Handling missing values

Feature normalization

Label encoding

Train-test split

2. Model Architecture

A fully connected neural network architecture was developed with:

MAF-based hidden layers

Linear output layer for multi-class classification

Cross-entropy loss

Optimizers such as Adam or SGD

3. Integration of MAF

The MAF function was implemented and injected into the model architecture to replace standard activations. This allowed direct performance comparison between:

Baseline Model (ReLU/Sigmoid)

MAF-enhanced Model

4. Evaluation Metrics

The model was assessed using:

Accuracy

Precision, Recall, F1-score

Confusion Matrix

ROC-AUC

Class-wise detection performance

📊 Results & Analysis

Experiments demonstrated that the MAF-based IDS architecture:

Outperformed baseline activations in detection accuracy

Provided improved recall for minority attack classes

Showed smoother and more stable gradients during training

Enhanced the discrimination of complex, overlapping attack patterns

These results support the hypothesis that customized activation functions can significantly augment IDS effectiveness.
