#  Radiology_AI-Disease-diagnosis---Fewshot-learning-with-VAE

Hybrid **Generative AI + Few-Shot Learning** model for radiology disease classification using **VAE-based augmentation** and **ResNet-backed prototypical networks** under low-data conditions.

---

## 🔍 Overview

This project focuses on improving medical image classification performance when very limited labeled training data is available — a common challenge in healthcare AI systems.

Deep learning models in medical imaging usually require large annotated datasets, which are expensive and difficult to obtain. This project addresses that limitation by integrating:

- **Few-Shot Learning (FSL)** – enables learning from very few labeled samples  
- **Variational Autoencoders (VAE)** – generate synthetic medical images  

The hybrid approach improves performance in **data-scarce environments**.

---

## ⚙️ Key Features

- Hybrid **VAE + Few-Shot Learning pipeline**  
- **Prototypical Networks** with ResNet-18 backbone  
- Synthetic image generation using **β-VAE**  
- Radiology image preprocessing and normalization  
- **Grad-CAM explainability** for disease localization  
- Performance analytics and evaluation metrics  
- Support for multiple radiology datasets  

---

## 🧠 System Architecture

```
Radiology Image
      ↓
Image Preprocessing (resize, normalize, denoise)
      ↓
Variational Autoencoder (generate synthetic samples)
      ↓
Hybrid Dataset (real + synthetic samples)
      ↓
Few-Shot Learning Classifier (Prototypical Network)
      ↓
Disease Prediction
```

📌 Grad-CAM is used for visualization and interpretability.

---

## 📊 Datasets Used

- **MedMNIST** – lightweight benchmark dataset  
- **NIH Chest X-ray14** – 14 thoracic disease labels  
- **COVID-19 Radiography Dataset** – COVID, pneumonia, normal  

✔️ All images resized to **224×224**

---

## 🧩 Model Architecture

### Variational Autoencoder (VAE)

- Encoder → Convolution layers  
- Latent Space → Dimension = 128  
- Decoder → Transposed convolution  

**Loss Function:**  
`Reconstruction Loss + KL Divergence`

---

### Few-Shot Learning Classifier

- Model → Prototypical Networks  
- Backbone → ResNet-18  
- Training → Episodic learning  

Examples:
- 5-way 1-shot  
- 5-way 5-shot  

Distance Metric: **Euclidean**

---

## 🔄 Hybrid Training Strategy

- Real Data: **70%**  
- Synthetic Data: **30%**

**Steps:**
1. Train VAE  
2. Generate synthetic images  
3. Merge datasets  
4. Train Few-Shot model  

---

## 📈 Experimental Results

| Model                  | Accuracy | F1 Score | AUC |
|-----------------------|----------|----------|-----|
| Baseline Few-Shot     | 62%      | 0.58     | 0.61 |
| Hybrid VAE + Few-Shot | 71%      | 0.66     | 0.72 |

✅ **+9% improvement**

---

## 🎯 Few-Shot Performance

| Scenario | Baseline | Hybrid |
|----------|----------|--------|
| 1-Shot   | 58%      | 67%    |
| 5-Shot   | 66%      | 75%    |

---

## 🧪 Synthetic Image Quality

| Metric | Score |
|--------|------|
| SSIM   | 0.76 |
| FID    | 23.4 |
| PSNR   | 28.2 |

✔️ 90%+ samples passed quality checks  

---

## 🔍 Explainable AI

- Uses **Grad-CAM** for interpretability  
- Highlights important regions in radiology images  

**Outputs:**
- Disease prediction  
- Confidence score  
- Attention heatmap  

---

## 📁 Project Structure

```
radiology-fewshot-vae-diagnosis/
│── data/
│── models/
│   ├── vae.py
│   ├── prototypical_network.py
│── training/
│   ├── train_vae.py
│   ├── train_fewshot.py
│── evaluation/
│   ├── evaluate_model.py
│── utils/
│   ├── preprocessing.py
│   ├── metrics.py
│── notebooks/
│── app/
│   ├── api.py
│   ├── inference.py
│── requirements.txt
│── README.md
```

---

## ⚡ Installation

```bash
git clone https://github.com/vijaykanagaraj7/Radiology_AI-Disease-diagnosis---Fewshot-learning-with-VAE.git
cd Radiology_AI-Disease-diagnosis---Fewshot-learning-with-VAE
pip install -r requirements.txt
```

---

## 🚀 Training

```bash
python train_vae.py
python train_fewshot.py
```

---

## 📊 Evaluation

```bash
python evaluate_model.py
```

---

## 🏥 Applications

- AI-assisted radiology diagnosis  
- Rare disease detection  
- Medical image dataset augmentation  
- Research in Few-Shot Learning & Generative AI  
- Explainable AI in healthcare  

---

## 🔮 Future Work

- Diffusion models for better image generation  
- Multi-modal datasets (CT, MRI, X-ray)  
- Large-scale clinical training  
- Deployment as decision support system  

---

## 👨‍💻 Authors

- Priyadarshini S  
- Rishikumaran T  
- Vijay K  

---
