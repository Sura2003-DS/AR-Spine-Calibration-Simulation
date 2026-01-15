# 🦴 AR Spine Calibration Simulation

## 📌 Overview

This project presents a **simulation-based framework** to evaluate calibration accuracy in **Augmented Reality (AR)–assisted spine surgery**. Precise AR calibration is critical in spinal procedures, as even small misalignments between virtual anatomy and the patient can lead to serious surgical risks.

The proposed framework provides a **safe, controlled, and repeatable environment** to analyze calibration performance **without real patient involvement**.

Using CT data from the **VerSe 2020 Spine Dataset**, the system reconstructs 3D vertebra models, extracts anatomical landmarks, simulates AR tracking errors, and evaluates calibration accuracy using rigid registration techniques.

---

## ❓ Problem Statement

In AR-guided spine surgery, accurate alignment between virtual anatomical models and the patient’s real anatomy is essential. However, existing AR systems often suffer from calibration errors due to:

* Tracking noise
* Limited or poorly distributed landmarks
* Hardware and sensing constraints

There is a lack of **systematic, software-based approaches** to quantitatively analyze how these factors affect AR calibration accuracy under controlled conditions.

---

## 💡 Proposed Solution

This project proposes a **data-driven, simulation-based calibration framework** that:

* Uses **CT-derived 3D vertebra models** for realistic anatomical representation
* Simulates **AR calibration under controlled noise conditions**
* Evaluates calibration accuracy using **quantitative error metrics**
* Analyzes the impact of **landmark count and tracking noise** on calibration performance

---

## 📊 Dataset

**Dataset Name:** VerSe 2020 Spine CT Dataset

**Description:**
Publicly available CT scans of the human spine with vertebra-level segmentation labels.

**Usage in this project:**

* 3D vertebra reconstruction
* Landmark extraction
* Calibration simulation

⚠️ **Note:**
The dataset is **not included** in this repository due to size constraints.
Please download it from the official **VerSe 2020 dataset** source.

---

## ⚙️ Methodology

1. CT data preprocessing and resampling
2. Vertebra segmentation using ground-truth labels
3. 3D surface reconstruction using the **Marching Cubes algorithm**
4. Surface-based anatomical landmark extraction
5. AR calibration simulation using known rigid transformations
6. Gaussian noise injection to model AR tracking errors
7. Rigid registration using **SVD / Kabsch algorithm**
8. Error evaluation using **Target Registration Error (TRE)**
9. Monte-Carlo simulations for robustness analysis

---

## 🧠 Algorithms Used

* **Marching Cubes** – 3D surface reconstruction
* **Rigid Registration (SVD / Kabsch)** – Optimal rotation and translation estimation
* **Target Registration Error (TRE)** – Calibration accuracy metric
* **Monte-Carlo Simulation** – Robustness evaluation under noise

---

## 📈 Experimental Results

Key observations from simulation experiments:

* Calibration accuracy **improves with higher landmark count**
* Increased tracking noise leads to **higher translation and rotation errors**
* Best performance achieved with:

  * **30 landmarks**
  * **Noise level = 0.5 mm**

**Achieved Accuracy:**

* Translation error: **~2–3 mm**
* Rotation error: **~1–2 degrees**

These results fall within **clinically acceptable limits** for AR-guided spine surgery.

---

## 🛠 Tools & Technologies

* Python
* NumPy
* SimpleITK
* scikit-image (Marching Cubes)
* Matplotlib
* PyTorch *(optional, for segmentation extension)*
* MeshLab (3D visualization)
* Gradio (interactive visualization interface)

---

## 🩺 Applications

* AR-guided spine surgery
* Surgical navigation systems
* Medical image analysis and simulation
* Pre-clinical evaluation of AR calibration strategies

---

## 🚀 Future Enhancements

* Integration with real AR hardware (e.g., **Microsoft HoloLens**)
* Automatic anatomical landmark detection using **machine learning**
* Full-spine and multi-level calibration analysis
* Clinical validation using **physical spine phantoms**

---

## 📁 Repository Structure (Optional but Recommended)

```
AR-Spine-Calibration-Simulation/
│
├── Webpage/            # Web UI screenshots and HTML
├── meshes/             # Sample vertebra meshes
├── results/            # Error plots and outputs
├── AR-Spine-Calibration.py
└── README.md
```


