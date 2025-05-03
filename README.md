# 🛒 Market Basket Analysis using Apriori Algorithm

This project implements **Market Basket Analysis** using the **Apriori algorithm** to uncover frequent itemsets and generate association rules from transactional purchase data. It helps retailers and analysts understand customer buying patterns, optimize product placement, and make data-driven decisions for cross-selling and promotions.

---

## 📌 Project Overview

Market Basket Analysis is a data mining technique used by businesses to discover associations between products bought together. This project focuses on using the Apriori algorithm (via the `mlxtend` library) to extract meaningful relationships between items in customer transactions. These insights are valuable for improving sales strategies such as bundling products, recommending items, or optimizing shelf layouts.

This notebook walks through the full pipeline:
- Data extraction  
- Preprocessing and transformation  
- Frequent pattern mining  
- Association rule generation  
- Result visualization and interpretation

---

## 📂 Dataset Description

The dataset contains **transactional data** where each row represents a shopping basket filled with one or more items purchased by a customer.

### 📄 Format:
- Each row is a list of items in a single transaction.
- Stored in a CSV file and loaded using Python's built-in `csv.reader()` to accommodate variable-length rows (ragged arrays).

### 🔍 Example:
```python
['milk', 'bread', 'butter']
['eggs', 'milk']
['bread', 'butter', 'jam']
✅ Key Characteristics:
No fixed number of columns (unlike structured tabular data).

Suitable for one-hot encoding using TransactionEncoder for association rule mining.

🧰 Libraries and Tools Used
pandas – Data manipulation

numpy – Array handling

seaborn, matplotlib – Data visualization

csv – Reading raw transaction lists

mlxtend – Apriori algorithm and rule generation

⚙️ Methodology
Data Loading
Transaction data is read using csv.reader and stored in a list format for flexible processing.

Preprocessing
The raw transaction list is transformed into a one-hot encoded matrix using TransactionEncoder, which allows us to apply algorithms that require binary input.

Frequent Itemset Generation
The Apriori algorithm is applied to discover itemsets that appear together with a minimum support threshold.

Association Rule Mining
Generated frequent itemsets are converted into rules using metrics like:

Support

Confidence

Lift

Visualization
High-confidence and high-lift rules are visualized using bar plots and heatmaps to interpret item associations effectively.

📈 Results & Insights
Extracted strong association rules (e.g., {milk} → {bread}) with high support and lift values.

Identified frequent itemsets that can guide product bundling and promotional campaigns.

Visualizations highlight top rules and item combinations that frequently occur together.

💡 Use Cases
Retail recommendations: Suggest related items at checkout or on product pages.

Promotional planning: Create offers based on frequently bought-together items.

Store layout optimization: Place frequently associated items near each other.

Inventory forecasting: Predict demand for product combinations.
