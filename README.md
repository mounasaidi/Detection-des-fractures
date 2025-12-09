# Fracture Detection in Arm X-rays using Random Forest

# 📋 Project Overview
This project implements a machine learning-based fracture detection system for arm X-rays using Random Forest classification on radiomic features. The system analyzes texture and intensity characteristics to identify fractures with high accuracy and interpretability.

# 🎯 Key Features
 *Radiomic Feature Extraction: GLCM texture, intensity statistics, edge features

 *Random Forest Classification: 86% test accuracy

 *Interpretable Results: Feature importance analysis for clinical insights

 *Fast Inference: CPU-friendly implementation

 *Comprehensive Evaluation: ROC, confusion matrix, cross-validation

# 📊 Dataset
 *Source: Kaggle Bone Fracture Detection : https://www.kaggle.com/datasets/pkdarabi/bone-fracture-detection-computer-vision-project

 *Selection: 234 arm X-rays (60% fractures, 40% non-fractures)

# 🏗️ Technical Architecture
1. Image Processing Pipeline
text
Raw X-ray → Grayscale → CLAHE → Edge Detection → Feature Extraction

3. Feature Engineering
 *Texture: GLCM contrast, energy, homogeneity, correlation

 *Intensity: Mean, std, skewness, kurtosis

 *Geometric: Edge density, compactness

 *Frequency: Wavelet coefficients

3. Model Specification
python
RandomForestClassifier(
    n_estimators=150,
    max_depth=12,
    min_samples_split=3,
    class_weight='balanced',
    random_state=42
)

# 📈 Performance Metrics
Metric	Value
Accuracy	86%
Precision	85%
Recall	87%
F1-Score	86%
AUC-ROC	90%
5-Fold CV	85% ± 4%

# ⚡ Advantages vs Deep Learning
Aspect	Random Forest	CNN
Accuracy	86%	89%
Speed	⚡ 0.1s/image	🐢 0.5s/image
Interpretability	✅ Feature importance	❌ Black box
Data Required	200+ images	1000+ images
Hardware	CPU	GPU recommended

# 📋 Clinical Applications
 *Triage Support: Prioritize urgent cases

 *Second Opinion: Reduce diagnostic errors

 *Epidemiology: Fracture pattern analysis

 *Education: Training tool for residents

