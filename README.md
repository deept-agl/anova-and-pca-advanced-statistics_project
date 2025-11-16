# 📘 Advanced Statistics Project — ANOVA & PCA

This project covers two major statistical analyses:
1. **One-Way & Two-Way ANOVA** to study how Salary varies with Education, Occupation, and their interaction  
2. **Principal Component Analysis (PCA)** on university/college dataset with 777 observations and 18 variables  

The project demonstrates hypothesis testing, interaction interpretation, dimensionality reduction, and exploratory statistics.

---

# 🧩 Problem 1 — ANOVA (Salary vs Education & Occupation)

Dataset: **40 individuals**  
Variables:  
- **Education** (HS, Bachelor, Doctorate)  
- **Occupation** (Admin/Clerical, Sales, Professional, Executive)  
- **Salary**

### 🔍 Steps Performed

#### **1. Exploratory Data Analysis**
- Summary statistics and data structure  
- Distribution plots & boxplots  
- Observed:  
  - High school graduates have lowest salaries  
  - Doctorate holders earn the highest  
  - Salary is slightly left-skewed  
  - No missing values  

---

### **2. One-Way ANOVA**

#### **Education → Salary**
- **p-value < 0.00001**  
- Reject H₀ → Salary **differs significantly** across education levels  

#### **Occupation → Salary**
- **p-value = 0.458**  
- Fail to reject H₀ → Salary **does not differ** significantly across occupations  

---

### **3. Post-Hoc Test (Tukey HSD)**  
- All education levels differ significantly  
- Doctorate > Bachelor > High School

---

### **4. Interaction (Education × Occupation)**
- Two-way ANOVA shows:  
  - **Education significant**  
  - **Occupation not significant**  
  - **Interaction is significant (p < 0.0001)**  

📌 *Conclusion:* Salary depends on both education level **and the interaction with occupation**, even though occupation alone is not significant.

---

# 🧠 Business Insights (ANOVA)
- Higher educational qualification strongly drives higher salary  
- Individuals with doctorate degrees earn the most across occupations  
- High school graduates earn the least  
- Combined effect of education + occupation impacts salary decisions  
- Useful for HR salary benchmarking and workforce planning

---

# 🧩 Problem 2 — PCA (Education Post 12th Standard Dataset)

Dataset: **777 colleges**, **18 variables** covering applications, admissions, expenses, faculty details, and graduation rates.

### 🔍 Steps Performed

#### **1. EDA**
- No missing values  
- All numerical variables  
- Significant outliers in many attributes  
- Apps, Accept, Enroll highly correlated  
- Books & Personal expenses show large spread differences  

---

### **2. Scaling**
- Applied **z-score standardization**  
- Necessary due to wide range differences (thousands vs two-digit fields)

---

### **3. Covariance vs Correlation**
- Correlation provides standardized relationships  
- Both matrices show similar structure but different magnitudes  
- Strong positive correlations among Apps, Accept, Enroll, UG student count

---

### **4. PCA**
- Computed covariance matrix  
- Performed eigen decomposition  
- Extracted eigenvalues & eigenvectors  
- **Scree Plot → break at PC2, but only ~58% variance**  
- Chosen **9 principal components** explaining **> 90% variance**

---

### **5. Insights from Principal Components**
- **PC1**: Captures largest variance—applications, acceptances, enrollment, undergrad numbers  
- **PC2**: Involves faculty ratios, expenses, personal cost  
- PCs help reduce dataset from 17 numerical attributes → 9 informative components  
- PCA useful for clustering or further dimensionality-based modelling

---

# 🛠️ Tools & Libraries
- Python  
- Pandas, NumPy  
- Statsmodels  
- Scikit-Learn  
- Matplotlib, Seaborn  


⭐ *If you found this project useful, please star the repository!*
