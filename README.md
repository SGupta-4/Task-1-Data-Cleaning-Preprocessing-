# Titanic Dataset Preprocessing

This project demonstrates a complete preprocessing pipeline on the Titanic dataset before applying any machine learning models.

---

## Steps Performed

### 1. Data Exploration
- Loaded the dataset using `pandas`.
- Checked dataset shape, data types, and missing values using:
  - `data.info()`
  - `data.isnull().sum()`
  - `data.describe()`

### 2. Target & Feature Separation
- Target variable: **Survived**  
- Features: All other columns.

### 3. Handling Missing Values
- **Numerical features** (`Age`, `Fare`): filled using **median imputation**.  
- **Categorical features** (`Cabin`, `Embarked`): filled using **most frequent value (mode)**.

### 4. Encoding Categorical Variables
- Dropped high-cardinality columns (`Name`, `Ticket`, `Cabin`) since they don’t add useful information without heavy feature engineering.
- Converted **Sex** to numeric using **Label Encoding**.  
- Converted **Embarked** to numeric using **One-Hot Encoding**.

### 5. Feature Scaling
- Applied **Standardization (Z-score scaling)** on numerical features so that they have mean 0 and standard deviation 1.

### 6. Outlier Detection and Removal
- Visualized outliers using **boxplots**.  
- Removed outliers from numerical columns using the **IQR (Interquartile Range) method**.

---

## Why These Steps Matter
- **Handling missing values** ensures no information gaps break model training.  
- **Encoding categorical variables** allows machine learning algorithms to process non-numeric data.  
- **Scaling** avoids bias towards features with large magnitudes.  
- **Outlier removal** prevents extreme values from skewing the model.  
- Together, these steps improve the quality of data and lead to more reliable ML models..
