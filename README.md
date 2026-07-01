# 🛒 Market Basket Analysis Project

## 📌 Project Overview
This project applies **Association Rule Mining** using the **Apriori Algorithm** to identify hidden relationships between products in retail transaction histories. These insights allow e-commerce businesses or grocery chains to optimize store layouts, refine product recommendations, and build highly effective cross-selling bundles.

---

## 🛠️ Tech Stack & Dependencies
* **Language:** Python 3
* **Environment:** Google Colab / Jupyter Notebooks
* **Libraries Used:** 
  * `mlxtend` (Apriori and association rules generation)
  * `pandas` (Data frame transformations)
  * `matplotlib` & `seaborn` (Statistical visualization)

---

## 📊 Dataset Detail
The project utilizes a standard public **Groceries Dataset** containing **9,835 unique purchase transactions** from a brick-and-mortar grocery retail store.

---

## 🚀 Key Steps & Implementation

### 1. Data Structuring & Encoding
* Transactions were read as raw, variable-length arrays.
* Used `TransactionEncoder` from `mlxtend` to pivot the dataset into a sparse, binary grid layout (One-Hot Encoded Matrix), where columns represent distinct grocery items and values are set to `True` or `False`.

### 2. Association Rule Criteria
* **Minimum Support (0.02):** Filters out items that appear in less than 2% of overall sales transactions.
* **Minimum Confidence (0.30):** Selects rules where there is at least a 30% conditional probability that buying the first product (antecedent) will result in buying the second product (consequent).

---

## 📈 Key Findings & Business Insights

* **Strongest Rule Affinities:** Customers purchasing itemsets like `yogurt` or `root vegetables` demonstrate a strong statistical inclination (`Lift > 1.5`) to simultaneously buy `whole milk`. 
* **Actionable Layout Strategies:** By placing high-lift product groups together (or featuring them together on digital storefront carousels), retail operations can directly increase their average transaction value (ATV).

---

## 💻 How to Run Locally

1. Clone the repository:
   ```bash
   git clone [https://github.com/samuelberchmans/Market-Basket-Analysis.git](https://github.com/samuelberchmans/Market-Basket-Analysis.git)
