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

This project supports **RadioML benchmark datasets**.Dataset and SNR Regimes: The model was trained and evaluated on the RML2022.01A dataset across multiple Signal-to-Noise Ratio (SNR) conditions, ranging from -20 dB to +20 dB. Overall Accuracy: It achieved an overall accuracy of 89.59% for high SNR (≥10 dB), 88.35% for medium SNR (≥0 dB), 79.05% for low SNR (≥-10 dB), and 65.39% for very low SNR (≥-20 dB) 
Robustness: The model demonstrated robust performance on linear modulations (BPSK, QPSK, QAM) and frequency modulations (CPFSK, GFSK). Near-perfect classification was achieved for BPSK, CPFSK, GFSK, and PAM4 

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
### Environment Setup
1. Clone the Repository
git clone https://github.com/mdisalm664-hub/Machine-Learning-Project.git
cd Machine-Learning-Project

2. Create and Activate a Virtual Environment
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows

3. Install Dependencies
pip install --upgrade pip
pip install -r requirements.txt

### Quick Start
1. Prepare the Dataset
Download the RadioML 2022.01A dataset and place it in the data/ directory

2. Run an Experiment
3. Results

After completion, the following outputs will be generated:

Trained model checkpoints

Training and validation accuracy/loss plots

Confusion matrices for modulation classes

Performance metrics across multiple SNR levels

All outputs are saved in the results/ directory.

### Directory Structure
Machine-Learning-Project/
│
├── data- RML22.01A.pkl             # RadioML dataset

│   ├── figures/                    # Accuracy, loss plots
│   ├── confusion_matrices/         # CM plots (per SNR)
│   └── logs/                       # Training logs
│
│   ├── data_loader.py              # Dataset loading & SNR filtering
│   ├── model.py                    # CNN + TCN + GRU architecture
│   ├── train.py                    # Training loop & callbacks
│   ├── evaluation.py               # Metrics & confusion matrices
│   └── utils.py                    # Helper functions
│
├── image_1.png                     # Architecture diagram         
├── README.md                       # Project documentation

