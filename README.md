# 🌌 Gravity Falls Puzzle Solver

[![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)](https://www.python.org/) 
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-blue?style=for-the-badge&logo=opencv)](https://opencv.org/) 
[![NumPy](https://img.shields.io/badge/NumPy-1.26-orange?style=for-the-badge&logo=numpy)](https://numpy.org/) 

**Automated Jigsaw Puzzle Analysis & Assembly Using Classical Computer Vision Techniques**  

---

## 🚀 Project Overview
The **Gravity Falls Puzzle Solver** is a classical computer vision system that automatically processes and assembles jigsaw puzzles from images. It supports **2x2, 4x4, and 8x8 puzzles**, using **robust preprocessing, contour extraction, and edge-matching techniques without ML/DL**.  

The project is divided into **two milestones**:
- **Milestone 1** – Preprocessing, segmentation, and feature extraction.
- **Milestone 2** – Edge representation, matching, puzzle assembly, and visualization.

---

## 👨‍💻 Team Members

| Name                       | ID       |
|----------------------------|----------|
| Omar Ahmed Abouraia        | 23P0100  |
| Hossam Ossama Hussieny     | 23P0010  |
| Mariam Ibrahim Assr        | 23P0123  |
| Mariam Tarek Farouk        | 23P0214  |
| Lujayn Mohamed             | 23P0187  |

**Supervised by:** Prof. Mahmoud Khalil  
**Course:** Image Processing / CSE483 – Ain Shams University  

---

## 🛠 Key Features

### 🎯 Milestone 1 – Image Preprocessing & Feature Extraction
- **Gaussian & Median Blur** – Removes high-frequency and salt-and-pepper noise.  
- **Grayscale Conversion** – Simplifies image processing.  
- **CLAHE & Sharpening** – Enhances edges and local contrast.  
- **Gamma Correction** – Normalizes lighting across tiles.  
- **Segmentation** – Supports automatic 2x2, 4x4, and 8x8 puzzle extraction.  
- **Feature Extraction** – Contour area, perimeter, centroid, bounding box, Hu Moments, and polygon vertices stored in JSON.  

**Output:** Preprocessed puzzle tiles, edge maps, contour overlays, structured feature dataset.

---

### 🎯 Milestone 2 – Edge Matching & Puzzle Assembly
- **LAB Color Space** – Better perceptual color comparison.  
- **Edge Cropping & Variance Weighting** – Focuses on meaningful edge pixels.  
- **Matching Algorithms**:
  - 2x2 Puzzles: Two-pass solver with flat-edge penalties.  
  - 4x4 Puzzles: Beam Search to efficiently handle combinatorial placements.
- **Stitching & Assembly** – Reconstructs puzzles using NumPy stacking.  
- **Evaluation** – Structural Similarity Index (SSIM) with pixel shift adjustments.

**Limitations:** Struggles with 8x8 puzzles due to combinatorial explosion; future improvements may include hierarchical matching and advanced heuristics.

---

## ✨ Highlights & Visual Results
- **Milestone 1:** Original → Preprocessed → Contour overlays  
- **Milestone 2:** Edge comparison → Candidate matches → Reconstructed puzzles  
- Supports rotated pieces and noisy backgrounds for robust demonstration.

---

## 📜 Installation & Usage

```bash
# 1. Clone the repository
git clone https://github.com/OmarAbouraia/Gravity-Falls-Puzzle-Solver.git
cd Gravity-Falls-Puzzle-Solver

# 2. Install dependencies
pip install opencv-python numpy matplotlib scikit-image

# 3. Run Milestone 1 pipeline (preprocessing & feature extraction)
python Gravity Falls Project_Team 4_MS1/Gravity Falls_MS1.py

# 4. Run Milestone 2 pipeline (edge matching & puzzle assembly)
python Gravity Falls_Team 4_MS2/Gravity Falls_Milestone2.ipynb

# 5. Check outputs
Preprocessed tiles, edge maps, and contours: Gravity Falls Project_Team 4_MS1/outputs_m1/
Assembled puzzles and visualizations: Gravity Falls_Team 4_MS2/Gravity Falls_MS2_Input/puzzle_2x2 or puzzle_4x4 or puzzle_8x8




