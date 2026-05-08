
# 🧠 Microwave Brain Tumor Detection using DAS Algorithm

This project implements an improved **Delay-And-Sum (DAS) beamforming algorithm** for detecting and localizing brain tumors using microwave imaging. The system processes multi-antenna **S-parameter (.s6p)** data obtained from simulations and reconstructs images to identify tumor presence and position.

---

## 📌 Project Overview

* Uses **microwave imaging** for non-invasive tumor detection
* Processes **multi-port S-parameter data (.s6p files)**
* Implements **DAS algorithm in Python**
* Supports **multiple tumor types and positions**
* Compares **healthy vs tumor cases**

---

## 📂 Repository Structure

```
├── DAS_improved_final.ipynb      # Main implementation of DAS algorithm
├── high_grade_glioma(-33,-5,-30).s6p
├── lowgrade.s6p
├── melignoma.s6p
├── tumor_2ndpos_1 (1).s6p
├── without_tumor_1 (5).s6p
└── README.md
```

---

## ⚙️ Methodology

### 1. Data Acquisition

* S-parameters are obtained from CST simulations of antenna arrays around a head phantom
* Includes both **healthy** and **tumor-affected cases**

### 2. Signal Processing

* Frequency-domain data is converted to **time-domain signals** using IFFT
* Preprocessing is applied to improve signal quality

### 3. DAS Algorithm

* Computes propagation delay for each pixel
* Aligns signals from multiple antennas
* Performs **coherent summation** to enhance tumor reflections

### 4. Image Reconstruction

* Generates intensity maps
* High-intensity regions indicate tumor presence

---

## 🧪 Dataset Description

| File Name                           | Description                 |
| ----------------------------------- | --------------------------- |
| `without_tumor_1 (5).s6p`           | Healthy head model          |
| `high_grade_glioma(-33,-5,-30).s6p` | High-grade tumor case       |
| `lowgrade.s6p`                      | Low-grade tumor             |
| `melignoma.s6p`                     | Malignant tumor             |
| `tumor_2ndpos_1 (1).s6p`            | Tumor at different position |

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies

```bash
pip install numpy matplotlib scipy scikit-rf
```

### 3. Run the Notebook

```bash
jupyter notebook DAS_improved_final.ipynb
```

---

## 📊 Results

* Successfully reconstructs microwave images
* Clearly distinguishes **tumor vs no tumor cases**
* Accurately localizes tumors for different:

  * Sizes
  * Types
  * Positions

---

## 📈 Complexity

* **Time Complexity:**
  `O(N × M × T)`
* **Space Complexity:**
  `O(N + M × T)`

Where:

* `N` = number of pixels
* `M` = number of antennas
* `T` = number of time samples

---

## ✨ Key Features

* Works with **realistic CST simulation data**
* Supports **multi-case tumor analysis**
* Improved DAS implementation for better clarity
* Easy to extend for **real-time medical imaging systems**

---

## 🔮 Future Work

* Improve tumor localization accuracy
* Implement advanced beamforming (e.g., DMAS, adaptive methods)
* Extend to **3D imaging**
* Integrate with a **web-based interface** for real-time analysis

---


## 📜 License

This project is for academic and research purposes.


