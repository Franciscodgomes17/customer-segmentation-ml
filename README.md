# Customer Segmentation and Targeted Promotions

This project applies **unsupervised machine learning** to segment customers based on demographics, purchase history, and behavioral patterns.  
We use **clustering techniques** (KMeans, Ward hierarchical) to identify distinct groups of customers, then generate **association rules** to design **personalized marketing strategies**.

Developed as the **Machine Learning II Final Project (NOVA IMS, 2023/2024)**.

---

## Tech Stack

- **Python 3.10+**
- **Jupyter Notebook**
- **scikit-learn** – clustering (KMeans, Ward linkage, DBScan trials)
- **scipy** – hierarchical clustering, dendrograms
- **mlxtend** – association rules
- **NumPy / Pandas** – data wrangling
- **Matplotlib / Seaborn** – visualization
- **UMAP** – dimensionality reduction for cluster visualization

---

## Repository Structure

~~~text
.
├─ Code/
│  ├─ eda - project.ipynb           # Exploratory Data Analysis & preprocessing
│  ├─ segmentation - project.ipynb  # Clustering, UMAP visualization
│  ├─ association_rules_project.ipynb # Market basket analysis for each cluster
│  ├─ utils1.py                     # helper functions (EDA, preprocessing)
│  ├─ utils2.py                     # helper functions (clustering, plots)
│  └─ Data/
│     ├─ customer_info.csv
│     └─ customer_basket.csv
├─ docs/
│  ├─ Project Report.pdf            # full academic report
├─ requirements.txt
├─ README.md
└─ LICENSE
~~~

---

## 🔎 Methodology

1. **Exploratory Data Analysis (EDA)**  
   - Data cleaning (drop irrelevant cols, fix percentages, binary encodings).  
   - Missing values imputation using **KNNImputer**.  
   - Outlier detection (custom thresholds, DBScan).  
   - Feature engineering (education, loyalty, dietary preferences, total spend).  

2. **Customer Segmentation**  
   - Methods tested: KMeans, Hierarchical (Ward), DBScan.  
   - Best solution: **Ward with MinMax scaling** → 9 clusters + “Fishy” as a separate 10th.  
   - Final segments:  
     - Promo Hunters  
     - High Spenders  
     - Vegetarians  
     - Pet Lovers  
     - Tech Enthusiasts  
     - Demanding Foodies  
     - Large Families  
     - College Students  
     - Karens  
     - Fishy  

3. **Association Rules & Targeted Promotions**  
   - Market basket analysis (Apriori, support, confidence, lift).  
   - Designed campaigns tailored to each segment (e.g., *Tech & Toast*, *Cooking Essentials*, *Student Drink Bundles*).  

---

## 📊 Results & Insights

- Identified **10 unique customer segments** with distinct purchasing patterns.  
- **High Spenders** and **Tech Enthusiasts** concentrated in wealthy urban areas.  
- **Promo Hunters** and **Karens** highly responsive to promotions and discounts.  
- **Vegetarians** and **Fishy** show strong dietary-driven purchasing behaviors.  
- Tailored promotions leverage association rules (e.g., bundle deals, loyalty programs).  

---

## 🚀 How to Run

1. Clone the repository:  
   ~~~bash
   git clone https://github.com/<your-username>/customer-segmentation-ml.git
   cd customer-segmentation-ml
   ~~~

2. Install dependencies:  
   ~~~bash
   pip install -r requirements.txt
   ~~~

3. Open Jupyter Notebooks:  
   ~~~bash
   jupyter notebook
   ~~~
   - Run `eda - project.ipynb` first  
   - Then run `segmentation - project.ipynb`  
   - Finally run `association_rules_project.ipynb`

---

## Requirements

See [`requirements.txt`](./requirements.txt).


