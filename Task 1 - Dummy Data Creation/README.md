
#  Real-Time Inventory Dummy Data Generation – Task 1

This task involves generating a realistic dummy dataset using the structure of the **Online Retail II** dataset. The primary goal is to simulate inventory and transaction data to be used for further analysis, machine learning, or dashboard development.

---

##  Project Structure

- `dummy_data.ipynb` – Google Colab that creates a dummy dataset based on selected columns from the original dataset.
- `online_retail_II.csv` – Original data source used as a reference for structure and values.

---

##  Task Overview

**Objective**:  
Create a **10,000-row dummy dataset** by extracting product information and adding synthetic data for analysis and system testing.

###  Steps Performed:

1. **Read and Explore Original Dataset** (`online_retail_II.csv`)
2. **Selected Columns**:
   - `StockCode`
   - `Description`
   - `UnitPrice`
3. **Added Dummy Columns**:
   - `Quantity` – Random values between 1 and 50
   - `Vendor` – Randomly assigned from a vendor list
   - `Invoice` – Synthetic invoice numbers
   - `InvoiceDate` – Random dates
   - `Customer ID` – Dummy customer identifiers
   - `Country` – Random country names
4. **Generated Unique Rows**:
   - Ensured 4,932 unique combinations of `StockCode` and `Description`
5. **Column Reordering Logic**:
   - Reordered columns to fit retail data conventions

---

##  Sample Output Columns

| Invoice | StockCode | Description | Quantity | UnitPrice | InvoiceDate | Customer ID | Country | Vendor |
|---------|-----------|-------------|----------|-----------|--------------|--------------|---------|--------|

---

##  Tech Stack

- **Python**: `pandas`, `numpy`, `random`
- **Google Colab** for development
- **CSV** for original data structure

---

##  Next Steps

- Use this dummy data for building a product inventory dashboard.
- Apply data cleaning, transformation, and modeling techniques.
- Integrate this into AWS Glue/S3/Kafka pipeline for real-time processing (future stages).

