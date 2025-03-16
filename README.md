# Bioactivity Prediction Web Application

### Introduction:
The focus of this project is to build a web application to predict the bioactivity towards inhibiting the Acetylcholinesterase enzyme.
Acetylcholinesterase is a known drug target related to the Alzheimer's disease

### Literature: https://pubmed.ncbi.nlm.nih.gov/27602288/


### Credits: [*Python for Bioinformatics*](https://www.youtube.com/watch?v=jBlTQjcKuaY&t=52s)


## Part 1: Data Loading, Preprocessing and Exploratory Data Analysis

In this section, we load data from the [*ChEMBL Database*](https://www.ebi.ac.uk/chembl/). The dataset is preprocessed through several steps to prepare it for analysis:

- **Target Selection**: A specific target is chosen for analysis.
- **Missing Data Handling**: Missing values are addressed appropriately.
- **Bioactivity Categorization**: Compounds are classified into three categories based on their biological activity level:
  - **Active**: Compounds with a bioactivity of < 1000 nM.
  - **Inactive**: Compounds with a bioactivity of > 10,000 nM.
  - **Intermediate**: Compounds with bioactivity values between 1000 nM and 10,000 nM.
  
### Exploratory Data Analysis using Lipinski- Descriptors
Exploratory Data Analysis (EDA) is performed to gain insights into the data. To assess the drug-like properties of the selected compounds, **Lipinski's descriptors** are calculated. Lipinski’s Rule of Five is a key criterion in drug discovery, predicting whether a compound is likely to have favorable **Absorption, Distribution, Metabolism, and Excretion (ADME)** properties, which are essential for its effectiveness as an oral drug.

### Chemical Space Analysis Using Lipinski- Descriptors

Next, the compounds categorized as **Intermediate** are removed to simplify the comparison between **Active** and **Inactive** compounds.

A **Mann-Whitney U Test** is then used to statistically assess whether there is a significant difference between the **Active** and **Inactive** groups. This non-parametric test helps determine if the two groups come from different distributions, providing valuable insights into the bioactivity of the compounds.

XXXXXXX PaDEL-Descriptor Xxxxxxxxxxxxx

## Part 2: Model Training, Model Comparison, App Development

### Building a QSAR Model
