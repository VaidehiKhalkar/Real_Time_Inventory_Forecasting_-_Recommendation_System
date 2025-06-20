#  Dummy Dataset Creation – Online Retail II

This project demonstrates the creation of a structured and realistic **dummy dataset** based on the famous **Online Retail II** dataset. It focuses on product data extraction, enhancement with simulated fields, and data preparation for analytics and modeling.

---

##  Project Objectives

- Extract essential product-related columns from the original dataset
- Clean and deduplicate raw data
- Generate **dummy values** for realistic simulation
- Structure the dataset with **industry-relevant features**
- Understand and document the meaning and behavior of each column
- Enable downstream use cases such as visualization, dashboards, or ML workflows

---

##  Working Process

### 1. **Dataset Loading**
- Load the original **Online Retail II** dataset.
- Focus only on relevant columns: `StockCode`, `Description`, and `Price`.

### 2. **Data Cleaning**
- Remove any rows with missing values.
- Remove duplicate entries based on product code and description.

### 3. **Feature Engineering**
- Create a new column `p_name` by extracting a simplified product name from the description.
- Add a dummy `Quantity` column with randomly generated values to simulate real-world orders.
- Add a dummy `Vendor` column with randomly assigned vendor names to simulate a multi-supplier environment.

### 4. **Column Structuring**
- Reorder the columns for better readability and consistency:  
  `StockCode`, `p_name`, `Description`, `Price`, `Quantity`, `Vendor`

### 5. **Deduplication**
- Generate a version of the dataset that includes **only unique products**, based on `StockCode` and `Description`.

### 6. **Sampling (Optional)**
- Create a 3% sample of the full dataset for quick testing or prototyping.

### 7. **Documentation**
- Explain each column in detail, including real-world meaning and business logic behind capital letters, negative values, and formatting quirks.
- Provide markdown-based documentation (`README.md`) for GitHub or professional sharing.

---

##  Column Descriptions

| Column      | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `StockCode` | Unique identifier for each product. Capital letters indicate variants or service items. |
| `p_name`    | Cleaned and simplified version of the product name, extracted from the full description. |
| `Description` | Original product description, usually in uppercase.                        |
| `Price`     | Unit price of the product in GBP.                                           |
| `Quantity`  | Randomly generated dummy quantity to simulate purchase volume.              |
| `Vendor`    | Dummy vendor name to represent the supplier or manufacturer.                |

---

##  Use Cases

- Product analytics and visualization
- Simulated retail dashboards (Power BI, Tableau, Streamlit)
- Mock customer segmentation and sales forecasting
- Feature engineering practice for ML pipelines
- Data cleaning, transformation, and enrichment exercises

---



