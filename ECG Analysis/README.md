# AI in Biomedicine – Practical Lesson 1

This repository contains materials related to **Practical Session 1** of the *AI in Biomedicine* course at Politecnico di Milano.  
The session introduces fundamental concepts of ECG signal processing and provides hands-on exercises for atrial fibrillation (AF) detection using machine learning methods.

---

## 📖 Overview

- **Professor:** Valentina Corino  
- **Teaching Assistant:** Francesca Lo Iacono (francesca.loiacono@polimi.it)  

### Topics Covered
1. **ECG Basics**  
   - Acquisition methods (limb leads, chest leads, unipolar vs. bipolar).  
   - Standard 12-lead hospital ECG.  
   - Importance of P-waves and their role in AF diagnosis.  

2. **ECG Alterations: Atrial Fibrillation (AF)**  
   - Most common sustained arrhythmia (~2% of global population).  
   - Risks: stroke, myocardial degeneration, increased mortality.  
   - ECG markers: chaotic atrial depolarization, disappearance of P-waves (f-waves), irregular R-R intervals.  

3. **Practical Session Objectives**  
   - Work with short 12-lead ECG signals.  
   - Learn preprocessing, feature extraction, and feature transformation for AF detection.  

---

## 📂 Dataset

- **Size:** 760 ECG signals (Atrial Fibrillation vs. Normal Sinus Rhythm).  
- **Files per subject:**  
  - `.hea` → metadata (subject information).  
  - `.mat` → 12-lead ECG signals (Matlab format).  

---

## 🧩 Exercises

### **Exercise I – Data Loading and Analysis**
- Load `.hea` and `.mat` files.  
- Plot label distribution (AF vs. NSR).  
- Plot signal length distribution.  
- Visualize sample ECG signals from each class.  

### **Exercise II – Feature Extraction**
- Extract rhythm-based and morphological features.  
- Examples: P-wave presence, R-R interval regularity.  

### **Exercise III – Feature Transformation**
- Adapt data types for machine learning models.  
- Handle missing data and outliers.  
- Apply feature scaling and normalization.  
- Perform dimensionality reduction.  

---

## ⚙️ Pipeline

```text
1. Data Loading
2. Preprocessing
3. Feature Extraction
4. Feature Type Adaptation
5. Feature Scaling & Normalization
6. Dimensionality Reduction
7. Model Training (Machine Learning Classifier)
