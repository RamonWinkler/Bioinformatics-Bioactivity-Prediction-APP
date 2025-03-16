# Bioactivity Prediction Web Application: A QSAR-Based Approach for Acetylcholinesterase Inhibition

### Introduction:
The focus of this project is to build a web application to predict the bioactivity towards inhibiting the Acetylcholinesterase enzyme.
Acetylcholinesterase is a known drug target related to the Alzheimer's disease

### Literature: https://pubmed.ncbi.nlm.nih.gov/27602288/


### Credits: [*Python for Bioinformatics*](https://www.youtube.com/watch?v=jBlTQjcKuaY&t=52s)


## **Project Workflow**

### **1. Data Acquisition and Preprocessing**
- **Data Source:** ChEMBL Database
- **Target Selection:** Filtering compounds tested for AChE inhibition.
- **Handling Missing Data:** Imputation or removal.
- **Bioactivity Categorization:**
  - **Active**: IC₅₀ < 1000 nM (strong inhibition)
  - **Inactive**: IC₅₀ > 10,000 nM (weak inhibition)
  - **Intermediate**: 1000 nM ≤ IC₅₀ ≤ 10,000 nM (excluded for binary classification)

---

### **2. Exploratory Data Analysis (EDA) and Chemical Space Characterization**
- **Lipinski’s Rule of Five (Ro5) Evaluation:**
  - Molecular weight ≤ 500 Da
  - Hydrogen bond donors ≤ 5
  - Hydrogen bond acceptors ≤ 10
  - LogP ≤ 5
- **Statistical Analysis:** Mann-Whitney U Test for active vs. inactive compounds.

---

### **3. Molecular Descriptor Calculation (PaDEL-Descriptors)**
- **2D Descriptors**: Molecular fingerprints, atom counts, charge distributions.
- **3D Descriptors**: Shape, topology, and conformation-dependent properties.

---

### **4. QSAR Model Development and Evaluation**
- **ML Algorithms Used:**
  - Random Forest (RF)
  - Support Vector Machine (SVM)
  - Gradient Boosting (GBM)
  - Deep Neural Networks (DNN)
- **Performance Metrics:**
  - Accuracy
  - Precision & Recall
  - ROC-AUC
  - Feature importance analysis using SHAP

---

### **5. Web Application Development (Streamlit Integration)**
- **Features:**
  - Upload molecular structures.
  - Generate **Lipinski and PaDEL descriptors**.
  - Obtain **bioactivity predictions**.

---

## **Installation & Usage**

### **Requirements**
Ensure you have the following installed:
```bash
pip install pandas numpy scikit-learn padelpy streamlit rdkit
```

### **Run the Application**
```bash
streamlit run app.py
```

---

## **Project Structure**
```
├── data/
│   ├── bioactivity_data.csv
│   ├── descriptors.csv
│
├── models/
│   ├── qsar_model.pkl
│
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── model_training.ipynb
│
├── app.py  # Streamlit App
├── utils.py  # Helper functions
├── requirements.txt
├── README.md
```
