# Hybrid Deep Learning Models for Multi-Class ECG Classification

Advanced hybrid deep learning architectures for multi-class ECG classification using time-domain and frequency-domain feature integration.

This project explores progressively enhanced models culminating in a multi-scale InceptionTime + Attention hybrid framework.

---

## 📌 Project Objective

To improve ECG classification accuracy and interpretability by integrating:

- Time-domain morphology
- Frequency-domain (FFT) features
- Multi-scale convolution (InceptionTime)
- Residual connections
- BiLSTM temporal modeling
- Multi-head self-attention

---

## 🏥 Dataset

- **PTB-XL ECG Dataset**
- 21,799 clinical 12-lead ECG records
- 18,869 patients
- 10-second recordings
- Expert cardiologist annotations

---

## ⚙️ Preprocessing Pipeline

- Resampling to 250 Hz
- High-pass, bandpass, and notch filtering
- Z-score normalization
- 5-second windowing (50% overlap)
- Stratified train-validation split
- Class balancing (oversampling / class weights)
- FFT feature extraction (for hybrid models)

---

## 🧠 Model Architectures

### 🔹 Model 1
Baseline FFT-based CNN

### 🔹 Model 2
Hybrid Time + FFT Dual-Branch CNN

### 🔹 Model 3
Residual CNN + FFT + BiLSTM + Multi-Head Attention

### 🔹 Model 4 (Best Model)
Multi-Scale InceptionTime + Residuals  
+ Dual-Branch Time-Frequency Fusion  
+ Multi-Head Self-Attention  
+ Class Weights + Early Stopping  

---

## 📊 Results (Ablation Study)

| Model | Description | Accuracy | F1 Score |
|-------|------------|----------|----------|
| Model 1 | FFT-CNN | 0.73 | 0.71 |
| Model 2 | Time + FFT Hybrid | 0.78 | 0.70 |
| Model 3 | Residual + BiLSTM + Attention | 0.85 | 0.81 |
| Model 4 | InceptionTime + Attention Hybrid | **0.92** | **0.92** |

Model 4 achieved the highest performance by combining multi-scale temporal features with frequency-domain information and attention mechanisms.

---

## 🖥️ Implementation Environment

- Python
- TensorFlow 2.x
- Keras
- NumPy / SciPy
- Pandas
- Scikit-learn
- NVIDIA Tesla T4 GPU (Kaggle environment)

---

## 🚀 How to Run

```bash
git clone https://github.com/<your-username>/Hybrid-ECG-Classification-InceptionTime-Attention.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run notebook:

```bash
jupyter notebook
```

---

## 🔬 Key Contributions

✔ Time–frequency fusion  
✔ Multi-scale InceptionTime blocks  
✔ Residual deep architecture  
✔ Attention-based interpretability  
✔ Full ablation study  

---

## 📜 License

MIT License

---

## ⚠️ Disclaimer

This project is for research and academic purposes only.  
Not intended for clinical deployment.
