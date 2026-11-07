# 🧬 OncoDerma – AI-Powered Skin Lesion Classification

An AI-powered skin lesion classification system designed to support early skin lesion assessment, raise awareness about skin cancer, and assist healthcare professionals with AI-based predictions.

<p align="center">
  <a href="https://elsayedsw33-oncoderma-scanner-app-kmjrao.streamlit.app/">
    <strong>🌐 Try the Live Demo</strong>
  </a>
</p>

---

## 📌 Overview

**OncoDerma** is a deep learning-based application developed as our graduation project at **Samsung Innovation Campus (SIC)**.

The project uses **24,930 dermoscopic images** collected from the ISIC 2019 and HAM10000 datasets to classify skin lesions and provide preliminary AI-based assessments.

Our goal is to help patients become more aware of potentially suspicious skin lesions and support doctors by providing quick predictions and estimated probabilities for different skin lesion categories.

The system is designed as a decision-support tool and does not replace professional medical diagnosis.

## 🎯 Project Objectives

- Support early assessment of potentially suspicious skin lesions.
- Raise awareness about skin cancer and the importance of early medical evaluation.
- Provide AI-based predictions to assist healthcare professionals.
- Help prioritize cases for further medical examination.
- Make AI-powered skin lesion classification accessible through an interactive web application.

## 🔬 Models & Architecture

We experimented with multiple deep learning approaches before selecting EfficientNetB6 for our final solution.

### Final Models

| Model | Task | Classes |
|---|---|---|
| EfficientNetB6 – Binary | Benign vs. Malignant classification | 2 |
| EfficientNetB6 – Multiclass | Skin lesion classification | 8 |

Both models were fine-tuned to perform their respective classification tasks.

### Experimental Architectures

- Custom CNN
- DenseNet201
- Google Derm Foundation
- EfficientNetB6

## 📊 Dataset

We combined dermoscopic images from two publicly available datasets:

- **ISIC 2019:** International Skin Imaging Collaboration dataset.
- **HAM10000:** Human Against Machine with 10,000 training images dataset.

**Dataset Statistics:**

| Attribute | Value |
|---|---|
| Total Images | 24,930 |
| Image Type | Dermoscopic Images |
| Data Sources | ISIC 2019 & HAM10000 |
| Classification Tasks | Binary & Multiclass |
| Multiclass Categories | 8 |

### Data Preprocessing

- Image cleaning and preprocessing.
- Duplicate image detection using SHA-256 hashing.
- Handling conflicting labels across datasets.
- Addressing class imbalance using class weighting and data augmentation.

## 🏆 Model Performance

Our best reported multiclass classification results:

| Metric | Score |
|---|---:|
| Accuracy | 85.32% |
| Precision | 85.61% |
| Recall | 85.32% |
| F1-Score | 85.39% |

These results represent a promising starting point. However, achieving clinically meaningful performance requires larger and more diverse datasets, additional computational resources, further model optimization, and rigorous clinical validation.

## 💻 Application Features

OncoDerma provides an interactive Streamlit application with:

- **Image Upload:** Upload dermoscopic images for analysis.
- **Binary Classification:** Predict benign or malignant categories.
- **Multiclass Classification:** Identify the predicted skin lesion category among eight classes.
- **Prediction Probabilities:** Display model-generated confidence scores.
- **LLM-Powered Assistant:** Explain classification results in simple language and provide general skin-health education.
- **Interactive Interface:** Access both classification models through one application.

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming | Python |
| Deep Learning | TensorFlow, Keras |
| Architectures | EfficientNetB6, DenseNet201, Custom CNN |
| Computer Vision | Image Processing, Data Augmentation |
| Foundation Models | Google Derm Foundation |
| LLM Integration | Large Language Models |
| Deployment | Streamlit |
| Data Processing | NumPy, Pandas |
| Data Integrity | SHA-256 Hashing |

## 🚧 Key Challenges

Throughout development, we encountered several technical challenges:

1. **Severe Class Imbalance:** Some skin lesion categories contained around 200 images, while others had up to 8,000. We addressed this using class weighting and data augmentation.

2. **Dataset Integration:** Combining ISIC 2019 and HAM10000 required careful label mapping, duplicate detection, and conflicting-label handling.

3. **Model Optimization:** We experimented with multiple architectures and fine-tuned EfficientNetB6 to improve classification performance.

4. **Computational Limitations:** Training large deep learning models required careful resource management and optimization.

5. **Application Integration:** Integrating two independent classification models and an LLM-powered assistant into one interactive application.

## 🌐 Live Demo

Try the deployed application:

**[Launch OncoDerma on Streamlit](https://elsayedsw33-oncoderma-scanner-app-kmjrao.streamlit.app/)**

## 🔮 Future Improvements

- Expand the training dataset with more diverse dermoscopic images.
- Improve performance on minority skin lesion categories.
- Explore additional architectures and optimization techniques.
- Improve probability calibration and model explainability.
- Conduct rigorous external and clinical validation.
- Enhance deployment performance and scalability.

## 👥 Team Members

This project was developed collaboratively as part of Samsung Innovation Campus.

- **Shaza Mohammed Gamal**
- **Romisaa Mohamed**
- **Elsayed Alaa**
- **Magdolen Hany**

## ⚠️ Medical Disclaimer

OncoDerma is an educational and research-oriented AI project. Its predictions and confidence scores are not medical diagnoses and should not be used as a substitute for professional medical advice, examination, or treatment.

Always consult a qualified healthcare professional for proper evaluation of suspicious skin lesions.

---

<p align="center">
  Developed with ❤️ as part of <strong>Samsung Innovation Campus (SIC)</strong>
</p>

