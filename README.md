🧠 NeuroExplain AI – Neurological Disease Prediction & Explainability

NeuroExplain AI is a deep learning–based framework for neurological disease classification from MRI scans with built-in Explainable AI (XAI) capabilities using Grad-CAM. The project combines multiple state-of-the-art CNN architectures, feature fusion, ensemble learning, and visual explanations to provide accurate and interpretable predictions.

🚀 Features
📊 MRI-based neurological disease classification
🏗️ Transfer learning using:
MobileNetV2
ResNet50
EfficientNetB3
🔄 Data augmentation & preprocessing pipeline
🎯 Feature extraction and feature fusion
🤝 Ensemble classification using:
Logistic Regression
Random Forest
Support Vector Machine (SVM)
🔥 Grad-CAM visual explanations
📈 Training curves, ROC curves, and confusion matrix
🖼️ Single MRI image prediction
💾 Automated model and results export
🏗️ System Architecture
MRI Dataset
      │
      ▼
Preprocessing & Augmentation
      │
      ▼
Train / Validation / Test Split
      │
      ▼
 ┌──────────────┬──────────────┬──────────────┐
 │   ResNet50  │ EfficientNet │ MobileNetV2 │
 └──────────────┴──────────────┴──────────────┘
      │
      ▼
Feature Extraction
      │
      ▼
Feature Fusion
      │
      ▼
Ensemble Classification
      │
      ▼
Disease Prediction
      │
      ▼
Grad-CAM Explainability
📂 Dataset Structure
Dataset/
│
├── Disease_1/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
│
├── Disease_2/
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
│
└── Disease_N/

Each folder represents a neurological disease class.

⚙️ Installation

Clone the repository:

git clone https://github.com/yourusername/NeuroExplain-AI.git
cd NeuroExplain-AI

Install dependencies:

pip install torch torchvision torchaudio
pip install grad-cam==1.4.8
pip install scikit-learn matplotlib seaborn pandas numpy
🧪 Training Pipeline

The notebook performs:

1. Dataset Preparation
Extract dataset
Create train/validation/test splits
Apply augmentations
2. Model Training

Train three transfer learning models:

ResNet50
EfficientNetB3
MobileNetV2

Features:

Early stopping
Learning rate scheduling
Transfer learning
Fine-tuning
3. Feature Fusion

Deep features from all three models are extracted and concatenated into a single fused representation.

ResNet Features
       +
EfficientNet Features
       +
MobileNet Features
       =
Fused Feature Vector
4. Ensemble Learning

The fused features are used to train:

Logistic Regression
Random Forest
Support Vector Machine (SVM)

Final predictions are generated using ensemble learning for improved performance.

🔥 Explainable AI (Grad-CAM)

The framework generates Grad-CAM heatmaps to highlight MRI regions responsible for model predictions.

Benefits:

Increased model transparency
Clinical interpretability
Trustworthy AI-assisted diagnosis

Generated outputs:

gradcam_results/
├── original_image.png
├── heatmap.png
└── overlay.png
📈 Evaluation Metrics

The project evaluates performance using:

Accuracy
Precision
Recall
F1-Score
ROC-AUC
Confusion Matrix

Generated visualizations:

training_curves.png
confusion_matrix.png
roc_curves.png
🖼️ Single Image Prediction

Upload an MRI image and obtain:

Predicted disease
Confidence score
Probability distribution
Grad-CAM explanation

Example:

Prediction: Alzheimer's Disease
Confidence: 96.4%
📋 Output Files

After execution, the following files are generated:

ResNet50_best.pth
EfficientNetB3_best.pth
MobileNetV2_best.pth
training_curves.png
confusion_matrix.png
roc_curves.png
neuroexplain_results.json
gradcam_results/
🛠️ Technologies Used
Python
PyTorch
Torchvision
Scikit-Learn
NumPy
Pandas
Matplotlib
Seaborn
Grad-CAM
Google Colab
🎯 Applications
Neurological disease diagnosis
MRI image analysis
Clinical decision support systems
Explainable healthcare AI
Medical imaging research
🔮 Future Enhancements
Vision Transformers (ViT)
Multimodal clinical data integration
Web deployment using FastAPI & React
Real-time MRI diagnosis dashboard
Neuro-symbolic reasoning for clinical explanations
