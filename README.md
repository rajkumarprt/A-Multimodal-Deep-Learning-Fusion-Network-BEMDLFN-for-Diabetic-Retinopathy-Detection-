# A-Multimodal-Deep-Learning-Fusion-Network-BEMDLFN-for-Diabetic-Retinopathy-Detection-
---
This project presents a Bootstrap-Ensemble Multimodal Deep Learning Fusion Network (BEMDLFN) for automated diabetic retinopathy (DR) detection using complementary retinal imaging modalities, namely Fundus photographs and Optical Coherence Tomography Angiography (OCTA) images. The framework integrates a Bootstrap-Ensemble DenseNet121 model for structural lesion analysis from fundus images and a Bootstrap-Ensemble ResNet50 model for microvascular feature extraction from OCTA images. Feature-level fusion is employed to combine structural and vascular retinal biomarkers, while bootstrap aggregation and soft-voting enhance model diversity, robustness, and generalization.
Experiments conducted on the APTOS 2019 Fundus Dataset and OCT2017 OCTA Dataset demonstrate the effectiveness of the proposed multimodal framework. The model achieved 97.93% Accuracy, 98.06% F1-Score, and 99.74% ROC-AUC, outperforming conventional CNN, VGG16, InceptionV3, EfficientNetB3, ResNet18, DenseNet121, and ResNet50 architectures. The proposed system provides a reliable computer-aided screening solution for early diabetic retinopathy detection and clinical decision support by jointly leveraging retinal structural abnormalities and microvascular changes. 
---
# Proposed Framework
The proposed BEMDLFN architecture consists of five major stages:
### 1. Fundus Image Processing
- Contrast Limited Adaptive Histogram Equalization (CLAHE)
- Shade correction
- Image normalization
- Noise reduction
- Image resizing (224×224)

DenseNet121 is employed to learn retinal structural abnormalities including:

- Microaneurysms
- Hemorrhages
- Hard exudates
- Cotton wool spots
- Optic disc abnormalities

----

### 2. OCTA Image Processing

OCTA images undergo:

- Median filtering
- Vessel enhancement
- Contrast normalization
- Intensity normalization
- Image resizing (224×224)

ResNet50 extracts vascular biomarkers including:

- Capillary density
- Vessel morphology
- Perfusion changes
- Foveal avascular zone characteristics
- Microvascular abnormalities

---
# Dataset

The framework utilizes publicly available retinal imaging datasets.

## Fundus Dataset

**APTOS 2019 Blindness Detection**

Contains color fundus photographs annotated for diabetic retinopathy severity.

----

## OCTA Dataset

**OCT2017 Dataset**

Contains Optical Coherence Tomography Angiography retinal scans used for extracting retinal vascular features.

---
## Project Structure

## Project Structure

```text
Bootstrap-Ensemble-Multimodal-DR-Detection/
│
├── README.md
├── requirements.txt
├── Bootstrap_Ensemble_Multimodal_DR_Detection.ipynb
│
├── datasets/
│   ├── APTOS2019/
│   └── OCT2017/
│
├── models/
│   ├── best_ResNet_octa_model.pth
│   ├── best_DenseNet_fundus_model.pth
│   ├── fundus_complete_ensemble.pkl
│   ├── octa_complete_ensemble.pkl
│   └── fusion_complete_ensemble.pkl/
│
├── results/
│   ├── fusion_performance.png
│   ├── extracted_actual_metrics.json
│   ├── fusion_test_results.json
│   └── fusion_bootstrap_results.json
│
├── figures/
│   ├── architecture.png
│   └── workflow.png
│
└── LICENSE
```
---

# Experimental Results

The proposed Bootstrap-Ensemble Multimodal Deep Learning Fusion Network significantly outperforms conventional deep learning architectures.

| Model | Accuracy (%) |
|---------|-------------|
| CNN | Baseline |
| VGG16 | Baseline |
| InceptionV3 | Baseline |
| EfficientNetB3 | Baseline |
| ResNet18 | Baseline |
| DenseNet121 | Baseline |
| ResNet50 | Baseline |
| **Bootstrap-Ensemble Multimodal Fusion Network (Proposed)** | **97.93** |

## Performance Metrics

| Metric | Score |
|---------|-------|
| Accuracy | **97.93%** |
| F1-Score | **98.06%** |
| ROC-AUC | **99.74%** |

---
# Advantages of the Proposed Framework

- Integrates complementary retinal imaging modalities
- Captures both structural and vascular retinal biomarkers
- Reduces overfitting using Bootstrap Aggregation
- Improves robustness through ensemble learning
- Better generalization than single CNN models
- Transfer learning reduces training time
- Suitable for real-world clinical screening systems
- Provides reliable computer-aided diagnosis support

---
# Applications

- Automated Diabetic Retinopathy Screening
- AI-Assisted Ophthalmology
- Clinical Decision Support Systems
- Computer-Aided Disease Diagnosis
- Multimodal Medical Image Analysis
- Intelligent Healthcare Systems
- Early Retinal Disease Detection

---
