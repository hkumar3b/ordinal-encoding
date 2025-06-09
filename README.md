# Customer Data Ordinal Encoding Project

This project focuses on transforming categorical data in a customer dataset using **Ordinal Encoding** and **Label Encoding**. The goal was to convert text-based categories into numerical formats, which is essential for training machine learning models, while preserving the natural order of certain categories.

## Project Overview

The dataset (`customer.csv`) contains key customer information, including:

- **Review** (e.g., 'Poor', 'Average', 'Good')
- **Education** (e.g., 'School', 'UG', 'PG')
- **Purchased** (whether a product was bought - 'Yes' or 'No')

I specifically targeted these features for encoding in order to make them suitable for use in machine learning models.

## Key Steps Taken

### 1. Data Loading

I loaded the `customer.csv` file into a pandas DataFrame to begin the preprocessing.

### 2. Feature Selection

I selected only the relevant columns — **review**, **education**, and **purchased** — for encoding.

### 3. Train-Test Split

The dataset was split into training and testing sets using `train_test_split` to evaluate the effectiveness of the encoding strategies.

### 4. Ordinal Encoding

I applied `OrdinalEncoder` to the **review** and **education** features because they have a clear, natural order:
- **Review:** 'Poor' → 0, 'Average' → 1, 'Good' → 2
- **Education:** 'School' → 0, 'UG' → 1, 'PG' → 2

I explicitly defined these category orders in the encoder to ensure accurate and meaningful transformation.

### 5. Label Encoding

For the **purchased** column (a binary target variable: 'Yes'/'No'), I used `LabelEncoder`, which mapped:
- 'No' → 0  
- 'Yes' → 1

## Libraries Used

- **pandas** — For efficient data handling and manipulation  
- **numpy** — For numerical operations and array transformations  
- **scikit-learn**:  
  - `OrdinalEncoder` — For ordered categorical data  
  - `LabelEncoder` — For binary target encoding  
  - `train_test_split` — For splitting data into training and testing sets


