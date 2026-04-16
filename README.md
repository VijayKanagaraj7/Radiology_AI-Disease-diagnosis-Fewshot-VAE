# Radiology_AI-Disease-diagnosis---Fewshot-learning-with-VAE
Hybrid Generative AI + Few-Shot Learning model for radiology disease classification using VAE-based augmentation and ResNet-backed prototypical networks under low-data conditions.

🔍 Overview

Medical imaging models typically require large annotated datasets, which are costly and limited. This project addresses this challenge by combining:

Few-Shot Learning → learns from very few labeled samples
Variational Autoencoders (VAE) → generate synthetic medical images

This hybrid approach improves classification performance in data-scarce healthcare environments.

⚙️ Key Features
Hybrid VAE + Few-Shot Learning pipeline
Prototypical Networks with ResNet-18 backbone
Synthetic image generation using β-VAE
Grad-CAM explainability for model interpretation
Multi-dataset support (MedMNIST, Chest X-ray, COVID datasets)
End-to-end training and evaluation pipeline
🧠 System Architecture
Radiology Image
      ↓
Preprocessing (Resize, Normalize)
      ↓
VAE (Synthetic Image Generation)
      ↓
Hybrid Dataset (Real + Synthetic)
      ↓
Few-Shot Classifier (Prototypical Network)
      ↓
Disease Prediction + Grad-CAM
📊 Results
✅ ~9% improvement over baseline few-shot models
📈 Strong performance in 1-shot and 5-shot scenarios
🧪 High-quality synthetic samples (SSIM, FID, PSNR validated)
🏥 Applications
AI-assisted radiology diagnosis
Rare disease detection
Medical dataset augmentation
Explainable AI in healthcare
🛠️ Tech Stack
Python, PyTorch
CNN (ResNet-18)
Few-Shot Learning (Prototypical Networks)
Variational Autoencoders (VAE)
Grad-CAM
📁 Project Structure
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
│── app/
│   ├── api.py
│   ├── inference.py
│── notebooks/
│── requirements.txt
│── README.md
⚡ Installation
git clone https://github.com/your-username/radiology-fewshot-vae-diagnosis.git
cd radiology-fewshot-vae-diagnosis
pip install -r requirements.txt
🚀 Usage
Train VAE
python train_vae.py
Train Few-Shot Model
python train_fewshot.py
Evaluate Model
python evaluate_model.py
👨‍💻 Authors
Priyadarshini S
Rishikumaran T
Vijay K
🔮 Future Work
Diffusion models for higher-quality synthetic images
Multi-modal datasets (CT, MRI)
Deployment as clinical decision support system
⭐ Acknowledgment

This project explores the intersection of Generative AI and Few-Shot Learning to solve real-world challenges in healthcare AI with limited data.
