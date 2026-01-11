# Machine-Learning-Project

## Project Overview and Motivation

This project investigates **Automatic Modulation Classification (AMC)** using modern deep learning techniques introduced in the course, particularly **Convolutional Neural Networks (CNNs)** and **sequence modeling architectures inspired by Transformer-style temporal learning**.

AMC is the task of identifying the modulation type of a received wireless signal **without prior knowledge of the transmitter**. This problem is important because accurate modulation recognition is essential for **cognitive radio**, **dynamic spectrum management**, and **intelligent wireless communication systems**.

Traditional feature-based AMC methods rely on handcrafted signal properties and often perform poorly in **low Signal-to-Noise Ratio (SNR)** environments. By leveraging deep learning, this project aims to **automatically learn robust spatial and temporal features directly from raw signal data**, thereby improving classification performance under varying SNR conditions.

---

## Architecture

![Proposed hybrid spatial-temporal architecture for AMC](https://github.com/mdisalm664-hub/Machine-Learning-Project/blob/970ba635769305b18eaaee13ff2b6de080590c5f/image_1.png)

**Figure:** Proposed hybrid spatial-temporal architecture for Automatic Modulation Classification (AMC)

---

## Dataset

This project supports **RadioML benchmark datasets**.

| Dataset | Classes | Samples per Pair | Total Samples | SNR Range |
|-------|---------|------------------|---------------|-----------|
| RML22 | 10 | 2,000 | ~420,000 | -20 to +20 dB (2 dB steps) |

---

## Requirements

### Core Dependencies
- Python **3.9+**
- TensorFlow **2.19+**
- NumPy **1.26+**
- Matplotlib **3.8+**
- Scikit-learn **1.4+**
- Pandas **2.2+**

### Additional Libraries
- `h5py` (for dataset loading)
- `pickle` (for RML2016.10a)
- `seaborn` (for visualization)

---

## Notes
- The model is designed to handle **raw IQ signal data**
- Performance is evaluated across **multiple SNR levels**
- The architecture combines **spatial feature extraction** and **temporal sequence modeling**


