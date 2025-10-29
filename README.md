# Bandaru-Lab-Inspired-AI
# A 1D-CNN for Biosignal Classification: An Analysis Inspired by the Bandaru Lab

**Author:** YoonYoung Lee

---

## Abstract & Dedication

This project is an independent research endeavor inspired by the pioneering work of Professor Prabhakar Bandaru's lab at UCSD on graphene field-effect transistors (G-FETs). The lab's publications on detecting femtomolar-level analytes demonstrate a fundamental challenge in modern materials science: identifying unique, low-amplitude "fingerprints" within complex, noisy 1D electrical signal data.

This project validates an AI-driven approach to this problem. I have designed, built, and trained a 1D Convolutional Neural Network (1D-CNN) to prove its effectiveness in classifying noisy, 1D biosignals, using a public dataset as a robust and analogous model.

This work is respectfully dedicated to Professor Bandaru and his team, whose research served as the primary inspiration for this exploration.

## Methodology

### The Analogous Problem
To test the hypothesis that a 1D-CNN can parse biosignal "fingerprints" without access to proprietary G-FET data, this project uses the publicly available **MIT-BIH Arrhythmia Database**.

This dataset is an ideal analogy:
* **Data Type:** 1D time-series signal data (ECG).
* **The Challenge:** The data is noisy, and the goal is to classify signals into 5 distinct categories (Normal, PVC, etc.) based on subtle pattern changes—a direct parallel to identifying different molecules from G-FET signals.

### The Model Architecture
A 1D-Convolutional Neural Network was constructed using TensorFlow and Keras. This architecture is superior to standard feed-forward networks for this task because its convolutional layers are specifically designed to learn "local" patterns (like the "blip" of a molecule or a QRS complex of a heartbeat) within a long sequence of data.

## Results & Analysis

The model was successfully trained on 87,554 heartbeat samples and validated on a separate test set of 21,892 samples.

* **Final Test Accuracy:** [99.14%]

This high-level accuracy confirms that the 1D-CNN architecture is exceptionally effective at identifying and classifying unique patterns in noisy, 1D biosignal data.



## Conclusion & Future Work

This project successfully demonstrates that a 1D-CNN is a powerful and viable tool for the automated classification of 1D biosignals.

The clear next step for this research would be to apply this validated architecture to the novel G-FET data from the Bandaru Lab. It is hypothesized that this model, when re-trained on G-FET data, could serve as a powerful accelerator for research—automating the identification of target molecules and increasing the throughput of sensor analysis.

---

### Runnable Code & Data
A complete, documented, and runnable version of this project is available as a public Kaggle Notebook:

[link to kaggle nb]
