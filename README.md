# AR Spine Calibration Simulation

## Overview
This project presents a simulation-based framework to evaluate calibration accuracy in Augmented Reality (AR)–assisted spine surgery. Accurate AR calibration is critical in spine procedures, where even small misalignments can lead to surgical risks. The proposed framework provides a safe and controlled environment to analyze calibration performance without real patient involvement.

Using CT data from the VerSe 2020 dataset, the system reconstructs 3D vertebra models, extracts anatomical landmarks, simulates AR tracking errors, and evaluates calibration accuracy using rigid registration techniques.

---

## Problem Statement
In AR-guided spine surgery, precise alignment between virtual anatomical models and the patient’s real anatomy is essential. Existing AR systems often suffer from calibration errors due to tracking noise, limited landmarks, and hardware constraints. There is a lack of systematic, software-based approaches to quantitatively analyze how these factors affect calibration accuracy.

---

## Proposed Solution
This project proposes a data-driven and simulation-based framework that:
- Uses CT-derived 3D vertebra models for realistic anatomical representation
- Simulates AR calibration under controlled noise conditions
- Evaluates calibration accuracy using quantitative error metrics
- Provides insights into the impact of landmark count and tracking noise

---

## Dataset
- **Dataset Name:** VerSe 2020 Spine CT Dataset  
- **Description:** Publicly available CT scans of the human spine with vertebra-level segmentation labels  
- **Usage:** 3D reconstruction, landmark extraction, and calibration simulation  
- **Note:** The dataset is not included in this repository due to size constraints. Please download it from the official VerSe dataset source.

---

## Methodology
1. CT data preprocessing and resampling  
2. Vertebra segmentation using ground-truth labels  
3. 3D surface reconstruction using the Marching Cubes algorithm  
4. Surface-based landmark extraction  
5. AR calibration simulation using known rigid transformations  
6. Gaussian noise injection to model tracking errors  
7. Rigid registration using SVD / Kabsch algorithm  
8. Error evaluation using Target Registration Error (TRE)  
9. Monte-Carlo simulations for robustness analysis  

---

## Algorithms Used
- Marching Cubes (3D surface reconstruction)  
- Rigid Registration (SVD / Kabsch algorithm)  
- Target Registration Error (TRE)  
- Monte-Carlo Simulation  

---

## Experimental Results
- Calibration accuracy improves with higher landmark count  
- Increased tracking noise leads to higher translation and rotation errors  
- Best performance achieved with:
  - **30 landmarks**
  - **Noise level of 0.5 mm**
- Achieved accuracy:
  - Translation error: ~2–3 mm  
  - Rotation error: ~1–2 degrees  

These results fall within clinically acceptable limits for AR-guided spine surgery.

---

## Tools & Technologies
- Python  
- NumPy  
- SimpleITK  
- scikit-image (Marching Cubes)  
- Matplotlib  
- PyTorch (optional, for segmentation extension)  
- MeshLab (3D visualization)  
- Gradio (interactive visualization)  

---

## Applications
- AR-guided spine surgery  
- Surgical navigation systems  
- Medical image analysis and simulation  
- Pre-clinical evaluation of AR calibration strategies  

---

## Future Enhancements
- Integration with real AR hardware (e.g., HoloLens)  
- Automatic anatomical landmark detection using machine learning  
- Full-spine and multi-level calibration analysis  
- Clinical validation using physical spine phantoms  

---

## Author
**Surabhi H R**  
M.Sc. Data Science  
REVA University

