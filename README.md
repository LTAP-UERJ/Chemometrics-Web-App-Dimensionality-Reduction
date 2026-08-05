# Chemometrics Web App — Dimensionality Reduction & Exploratory Analysis (Part 2)

![Status](https://img.shields.io/badge/Status-Active-green)
![Version](https://img.shields.io/badge/Release-V3-orange)
![License](https://img.shields.io/badge/License-Proprietary%20%2F%20INPI%20Registered-red.svg)
![R](https://img.shields.io/badge/R%20Version-4.3.0%2B-blue.svg)

Developed by the **[Process Analytical Technology Laboratory (LTAP-UERJ)](https://www.ltapuerj.com.br/)**, this application is an advanced platform for exploratory data analysis, feature filtering, signal compression, cluster analysis, and linear/non-linear dimensionality reduction of chemometric datasets.

---

## 🔗 Quick Links

* **Online Web App:** [Access on Shinyapps.io](https://ltap.shinyapps.io/dimensionality_reduction/)
* **Desktop Executable Download:** [Download Executable (Google Drive)](https://drive.google.com/drive/folders/1l8dB4BGKVjqPMrvA5ZCLvafRNtTOCFew?usp=drive_link)
* **Scientific Article:** [Chemometrics Web App Part 2: Dimensionality Reduction and Exploratory Analysis (Chemometrics and Intelligent Laboratory Systems)](https://doi.org/10.1016/j.chemolab.2023.104810)
* **Official Website:** [LTAP-UERJ Portal](https://www.ltapuerj.com.br/)
* **Software Registration (INPI):** [LTAP-UERJ CWA — Registros de Software](https://sites.google.com/view/ltap-uerj/cwa)
* **Support & Licensing:** [licarion@gmail.com](mailto:licarion@gmail.com) | [ltapuerj@gmail.com](mailto:ltapuerj@gmail.com)

---

## 👥 Developers & Authors

This module was developed by the chemometrics research team at **LTAP-UERJ**:

| Author | Affiliation | Profile / Contact |
| :--- | :--- | :--- |
| **[Bernardo Cardeal Darzé](http://lattes.cnpq.br/0590620499595344)** | LTAP — UERJ | [Lattes Profile](http://lattes.cnpq.br/0590620499595344) |
| **[José Licarion Pinto Segundo Neto](http://lattes.cnpq.br/5267552018296169)** | LTAP — UERJ | [Lattes Profile](http://lattes.cnpq.br/5267552018296169) |
| **[Aderval Severino Luna](http://lattes.cnpq.br/0294676847895948)** | UERJ | [Lattes Profile](http://lattes.cnpq.br/0294676847895948) |
| **[Igor Campos de Almeida Lima]** | UERJ | [Lattes Profile](http://lattes.cnpq.br/8976902901816349) | 

---

## 🆕 Version History (Change Log)

### **V3 — Current Release**
* **Non-Linear Methods Expansion:** Full integration of **t-SNE**, **Kernel PCA**, **Multidimensional Scaling (MDS)**, and **Isomap** for non-linear manifold learning.
* **Robust Diagnostic Engine:** Integrated Score Distance vs. Orthogonal Distance (Model Distance) outlier diagnostics for robust PCA model validation.
* **3D Interactive Visualizations:** Full 3D interactive rendering of Scores, Loadings, and BiPlots powered by Plotly.
* **Wavelet & Filter Compression:** Added Discrete Wavelet Transform (DWT) compression along with Low-Variance and High-Correlation feature selection filters.
* **Automated Report Builder:** Multi-language HTML/PDF report generator summarizing exploratory models and diagnostic metrics.
* **CWA Workspace Serialization:** Save and restore workspace states in `.RData` format for seamless inter-module data transfer across the CWA platform.

### **V2 — Structural Enhancements**
* Integrated **Robust PCA** ($L_1$-norm / Hubert's ROBPCA) and **Factor Analysis (FA)**.
* Hierarchical Cluster Analysis (HCA) dendrogram enhancements with custom distance metrics and linkage criteria.

### **V1 — Initial Release**
* Standard Principal Component Analysis (PCA) with 2D score and loading plots.

---

## 🚀 Key Features

### ✂️ Data Filtering & Compression
| Tool | Description |
| :--- | :--- |
| **Resolution Reduction** | Spectral resolution downsampling for high-density spectral data. |
| **Low-Variance Filter** | Automatic identification and removal of uninformative, near-zero variance features. |
| **High-Correlation Filter** | Elimination of highly collinear and redundant variables based on custom thresholding. |
| **Wavelet Compression** | Discrete Wavelet Transform (DWT) multi-resolution feature reduction. |

### 🌳 Cluster Analysis (HCA & Clustering)
| Tool | Description |
| :--- | :--- |
| **Hierarchical Cluster Analysis (HCA)** | Agglomerative clustering with customizable linkage (Ward, Complete, Single, Average) and distance metrics (Euclidean, Manhattan, Mahalanobis). |
| **Interactive Dendrograms** | Dynamic dendrogram tree visualization with class color-coding and cluster assignment export. |
| **NbClust** | Automatic determination of the optimal number of clusters using 26 internal validity indices. |

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
| **Isomap** | Isometric Feature Mapping — geodesic distance preservation across non-linear manifolds via `vegan`. |

### 📊 Diagnostics & Visualizations
* **Scree & Variance Plots:** Individual and cumulative variance explained per principal component/factor.
* **Interactive Loadings & Scores:** 2D and 3D score scatter plots, loading profiles, and unified BiPlots.
* **Outlier & Residual Diagnostics:** Score distance ($SD$) vs. Orthogonal distance ($OD$) cutoff thresholds for robust sample diagnostic classification.
* **Heatmaps & Circular Correlation Maps:** `pheatmap` and `circlize` heatmaps and correlation circle diagrams.

---

## 🛠️ Technical Stack & Environment

### **Build & Compilation Environment**
* **Language Runtime:** `R (>= 4.3.0)`

### **Core R Dependencies & Libraries**
| Package | Version / Scope | Purpose |
| :--- | :--- | :--- |
| **`shiny`** | `^1.8.0` | Reactive application framework and web server architecture. |
| **`shinydashboard`** | `^0.7.2` | Dashboard layout structure and sidebar navigation UI. |
| **`plotly`** | `^4.10.0` | Interactive 2D/3D score plots, loading profiles, and BiPlots. |
| **`DT`** | `^0.30` | DataTables interface for dataset preview and tabular outputs. |
| **`mdatools`** | `^0.14.0` | PCA, Robust PCA, Score/Orthogonal Distance outlier diagnostics. |
| **`rrcov`** | `^1.7.4` | Robust PCA via Minimum Covariance Determinant (ROBPCA). |
| **`ica`** | `^1.0-3` | Independent Component Analysis (ICA) blind source separation. |
| **`kernlab`** | `^0.9-32` | Kernel PCA with RBF, Polynomial, and Sigmoid kernel functions. |
| **`Rtsne`** | `^0.17` | t-SNE non-linear dimensionality reduction and manifold embedding. |
| **`vegan`** | `^2.6-4` | MDS and Isomap geodesic distance-based manifold learning. |
| **`NbClust`** | `^3.0.1` | Optimal cluster number determination (26 validity indices). |
| **`dendextend`** | `^1.17.1` | Enhanced HCA dendrogram visualization and color-coding. |
| **`factoextra`** | `^1.0.7` | PCA/clustering visualization (scree, silhouette, cluster plots). |
| **`wavelets`** | `^0.3-0` | Discrete Wavelet Transform (DWT) compression. |
| **`pheatmap`** | `^1.0.12` | High-quality heatmaps with hierarchical clustering annotation. |
| **`circlize`** | `^0.4.15` | Circular correlation diagram visualizations. |
| **`psych`** | `^2.3.6` | Factor Analysis with Varimax and Promax rotations. |
| **`ggcorrplot`** | `^0.1.4` | Correlation matrix visualizations with significance testing. |
| **`rmarkdown`** | `^2.25` | Automated multi-language HTML/PDF report generation. |

---

## 💻 Access & Execution

This application is distributed under proprietary closed-source terms (the underlying `app.R` source code is not publicly distributed). Access is available through two distribution models:

1. **🌐 Online Web Version (Shinyapps.io):**
   * Access directly via web browser without installing R or any dependencies:
   * 🔗 **[https://ltap.shinyapps.io/dimensionality_reduction/](https://ltap.shinyapps.io/dimensionality_reduction/)**

2. **🖥️ Desktop Executable Version:**
   * Standalone Windows executable bundle (`.exe`) with an embedded runtime environment. No prior R installation required on the target computer.
   * Download the executable for Dimensionality Reduction (Part 2) and other LTAP CWA modules here:
   * 🔗 **[LTAP CWA Executables Folder (Google Drive)](https://drive.google.com/drive/folders/1l8dB4BGKVjqPMrvA5ZCLvafRNtTOCFew?usp=drive_link)**

---

## ⚠️ Methodological Guidelines

> [!IMPORTANT]
> **Critical recommendations for dimensionality reduction & exploratory analysis:**
> - Apply **Data Preprocessing** (centering, scaling, scatter corrections) in the CWA: Data Handling module *before* importing data into this module.
> - Evaluate the optimal number of principal components using **Scree Plots** and cumulative explained variance (typically retaining components explaining ≥ 95% of total variance).
> - Use **Score Distance vs. Orthogonal Distance** diagnostics to classify samples as regular, moderate outliers, or extreme outliers before downstream modeling.
> - For high-dimensional, non-linear, or cluster-structured datasets, complement PCA with **t-SNE** or **Isomap** projections to avoid distorted linear projections.

---

## 📜 License & Intellectual Property Protection

> [!CAUTION]
> **All Rights Reserved — Intellectual Property Protection (INPI)**
> 
> This software, its interface designs, compiled binaries, and underlying analytical workflows are protected under Intellectual Property laws (Brazilian Software Law No. 9.609/98 and Industrial Property Law No. 9.279/96) and registered at the **National Institute of Industrial Property (INPI)**.

### **Terms of Use & Protection Clause:**
1. **Mandatory Attribution & Citation:** Any academic work, scientific article, technical report, software integration, or presentation utilizing or referencing this application **must explicitly credit** the authors (**Bernardo Cardeal Darzé, I. C. A. Lima, José Licarion Pinto Segundo Neto, Aderval Severino Luna**) and the **Process Analytical Technology Laboratory ([LTAP-UERJ](https://www.ltapuerj.com.br/))**, and cite the published scientific paper:
   > B.C. Darzé, I.C.A. Lima, A.S. Luna, L. Pinto, *Chemometrics web app's part 2: dimensionality reduction and exploratory analysis*, Chemometrics and Intelligent Laboratory Systems, 237 (2023) 104810. DOI: [10.1016/j.chemolab.2023.104810](https://doi.org/10.1016/j.chemolab.2023.104810)
2. **Prohibition of Unauthorized Reproduction & Redistribution:** Copying, modifying, decompiling, reverse engineering, re-licensing, sub-licensing, mirroring, or redistributing the binary executables or deployment packages without explicit prior written consent from LTAP-UERJ is strictly prohibited.
3. **Non-Commercial Use Only:** The application may only be used for personal, educational, or non-commercial academic research purposes unless a specific commercial license has been granted by LTAP-UERJ.
4. **Disclaimer of Liability:** LTAP-UERJ and the developers accept no responsibility or liability for damages, misinterpretation, or loss resulting from the use of this software or its generated datasets. The software is provided "as is", without warranties of any kind.

For licensing inquiries or commercial use permissions, please contact [licarion@gmail.com](mailto:licarion@gmail.com) or [ltapuerj@gmail.com](mailto:ltapuerj@gmail.com).

---

## 📧 Contact & Institutional Support

**[Process Analytical Technology Laboratory (LTAP/UERJ)](https://www.ltapuerj.com.br/)**

We acknowledge financial and institutional support from **UERJ**, **FAPERJ** (JCNE and CNE research scholarships), **CNPq** (Universal Grant), and **CAPES** (Finance Code 001).

---

<p align="center">
  <a href="https://www.ltapuerj.com.br/">LTAP-UERJ</a> •
  <a href="https://www.uerj.br/">UERJ</a> •
  <a href="https://www.faperj.br/">FAPERJ</a> •
  <a href="https://www.gov.br/cnpq/pt-br">CNPq</a> •
  <a href="https://www.gov.br/capes/pt-br">CAPES</a>
</p>
```
