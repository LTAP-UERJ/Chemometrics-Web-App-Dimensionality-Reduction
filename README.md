# Chemometrics Web App — Dimensionality Reduction & Exploratory Analysis (Part 2)

![Status](https://img.shields.io/badge/Status-Active-green)
![Version](https://img.shields.io/badge/Release-V3-orange)
![License](https://img.shields.io/badge/License-Proprietary%20%2F%20INPI%20Registered-red.svg)
![R](https://img.shields.io/badge/Language-R-blue.svg)

Developed by the **Process Analytical Technology Laboratory (LTAP-UERJ)**, this application is an advanced platform for exploratory data analysis, feature filtering, signal compression, cluster analysis, and linear/non-linear dimensionality reduction of chemometric datasets.

---

## 🔗 Quick Links

* **Online Version:** [Access the Web App](https://ltap.shinyapps.io/exploratory_analysis/)
* **Scientific Article:** [ScienceDirect — Chemometrics Web App Part 2: Dimensionality Reduction and Exploratory Analysis](https://doi.org/10.1016/j.chemolab.2023.104810)
* **Software Registration (INPI):** [LTAP-UERJ CWA — Registros de Software](https://sites.google.com/view/ltap-uerj/cwa)
* **Support/Feedback:** [ltapuerj@gmail.com](mailto:ltapuerj@gmail.com)

---

## 🆕 Version History (Change Log)

### **V3 — Current Release**
* **Non-Linear Methods Expansion:** Full integration of **t-SNE**, **Kernel PCA**, **Multidimensional Scaling (MDS)**, and **Isomap** for non-linear manifold learning.
* **Robust Diagnostic Engine:** Integrated Score Distance vs. Orthogonal Distance (Model Distance) outlier diagnostics for robust PCA model validation.
* **3D Interactive Visualizations:** Full 3D interactive rendering of Scores, Loadings, and BiPlots powered by Plotly.
* **Wavelet & Filter Compression:** Added Discrete Wavelet Transform (DWT) compression along with Low-Variance and High-Correlation feature selection filters.
* **Automated Report Builder:** Multi-language HTML/PDF report generator summarizing exploratory models and diagnostic metrics.

### **V2 — Structural Enhancements**
* Integrated **Robust PCA** ($L_1$-norm / Hubert's ROBPCA) and Factor Analysis (FA).
* Hierarchical Cluster Analysis (HCA) dendrogram enhancements with custom distance metrics and linkage criteria.

### **V1 — Initial Release**
* Standard Principal Component Analysis (PCA) with 2D score and loading plots.

---

## 🚀 Key Features

### ✂️ Data Filtering & Compression
* **Resolution Reduction:** Spectral resolution downsampling for high-density spectral data.
* **Low-Variance Filter:** Automatic identification and removal of uninformative, near-zero variance features.
* **High-Correlation Filter:** Elimination of highly collinear and redundant variables based on custom thresholding.
* **Wavelet Compression:** Discrete Wavelet Transform (DWT) multi-resolution feature reduction.

### 🌳 Cluster Analysis (HCA & Clustering)
* **Hierarchical Cluster Analysis (HCA):** Agglomerative clustering with customizable linkage (Ward, Complete, Single, Average) and distance metrics (Euclidean, Manhattan, Mahalanobis).
* **Interactive Dendrograms:** Dynamic dendrogram tree visualization with class color-coding and cluster assignment export.

### 📐 Parametric (Linear) Dimensionality Reduction
| Method | Description |
| :--- | :--- |
| **PCA** | Principal Component Analysis — variance-maximizing linear projection. |
| **Robust PCA** | Outlier-resistant PCA based on Minimum Covariance Determinant (MCD) / ROBPCA. |
| **Factor Analysis (FA)** | Underlying latent factor identification with orthogonal/oblique rotations (Varimax, Promax). |
| **ICA** | Independent Component Analysis — blind source separation into statistically independent components. |

### 🌀 Non-Parametric (Non-Linear) Manifold Learning
| Method | Description |
| :--- | :--- |
| **Kernel PCA** | Non-linear PCA using RBF, Polynomial, and Sigmoid kernels. |
| **t-SNE** | $t$-Distributed Stochastic Neighbor Embedding for local structure preservation and cluster separation. |
| **MDS** | Multidimensional Scaling — classical metric and non-metric pairwise distance preservation. |
| **Isomap** | Isometric Feature Mapping — geodesic distance preservation across non-linear manifolds. |

### 📊 Diagnostics & Visualizations
* **Scree & Variance Plots:** Individual and cumulative variance explained per principal component/factor.
* **Interactive Loadings & Scores:** 2D and 3D score scatter plots, loading profiles, and unified BiPlots.
* **Outlier & Residual Diagnostics:** Score distance ($SD$) vs. Orthogonal distance ($OD$) cutoff thresholds for robust sample diagnostic classification.

---

## 💾 Installation & Usage

### **How to Run (R/RStudio)**
After downloading or cloning the unencrypted source files, open the application in RStudio and click the **"Run App"** button at the top right of the editor.

### **Distribution Models**
* **Shinyapps Version 01:** Open source and free online access.
* **Desktop Version 01:** Available as an offline standalone executable.

---

## 📜 License & Intellectual Property Protection

> [!CAUTION]
> **All Rights Reserved — Intellectual Property Protection (INPI)**
> 
> This software, its source code, interface designs, visual assets, and underlying analytical workflows are protected under Intellectual Property laws (Brazilian Software Law No. 9.609/98 and Industrial Property Law No. 9.279/96) and registered at the **National Institute of Industrial Property (INPI)**.

### **Terms of Use & Protection Clause:**
1. **Mandatory Attribution & Citation:** Any academic work, scientific article, technical report, software integration, or presentation utilizing or referencing this application **must explicitly credit** the authors (**Paulo Henrique Couto Simões, Julio Cesar Siqueira, Licarion Pinto, Aderval Luna**) and the **Process Analytical Technology Laboratory (LTAP-UERJ)**, and cite the published scientific paper:
   > B.C. Darz, I.C.A. Lima, A.S. Luna, L. Pinto, *Chemometrics web app's part 2: dimensionality reduction and exploratory analysis*, Chemometrics and Intelligent Laboratory Systems, 237 (2023) 104810. DOI: [10.1016/j.chemolab.2023.104810](https://doi.org/10.1016/j.chemolab.2023.104810)
2. **Prohibition of Unauthorized Reproduction & Redistribution:** Copying, modifying, decompiling, reverse engineering, re-licensing, sub-licensing, mirroring, or redistributing the source code or binary executables without explicit prior written consent from LTAP-UERJ is strictly prohibited.
3. **Non-Commercial Use Only:** The application may only be used for personal, educational, or non-commercial academic research purposes unless a specific commercial license has been granted by LTAP-UERJ.
4. **Disclaimer of Liability:** LTAP-UERJ and the developers accept no responsibility or liability for damages, misinterpretation, or loss resulting from the use of this software or its generated datasets. The software is provided "as is", without warranties of any kind.

For licensing inquiries or commercial use permissions, please contact [ltapuerj@gmail.com](mailto:ltapuerj@gmail.com).

---

## 📧 Contact & Team

**Process Analytical Technology Laboratory (LTAP/UERJ)**

| Name | Email |
| :--- | :--- |
| **Paulo Henrique Couto Simões** | [ph.simoes@gmail.com](mailto:ph.simoes@gmail.com) |
| **Julio Cesar Siqueira** | [juliosiqueira86@hotmail.com](mailto:juliosiqueira86@hotmail.com) |
| **Licarion Pinto** | [licarion@gmail.com](mailto:licarion@gmail.com) |
| **Aderval Luna** | [adsluna@gmail.com](mailto:adsluna@gmail.com) |

---

<p align="center">
  <a href="https://www.ltapuerj.com.br/">LTAP-UERJ</a> •
  <a href="https://www.uerj.br/">UERJ</a> •
  <a href="https://www.faperj.br/">FAPERJ</a> •
  <a href="https://www.gov.br/cnpq/pt-br">CNPq</a> •
  <a href="https://www.gov.br/capes/pt-br">CAPES</a>
</p>
