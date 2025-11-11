# **gcp-etl-pipeline**
End-to-end ETL pipeline on Google Cloud Platform: Raw data generation (Python), transformation with Data Fusion, storage in BigQuery, and interactive analytics in Looker Studio.

---

## **Project Overview**

E-commerce datasets provide valuable insights into sales trends, product performance, and customer behavior. This project simulates such data using the Faker library and processes it through a robust ETL pipeline on GCP.  
Key steps include:
1. **Data Generation:** Synthetic data generation using Python's Faker library.
2. **Data Transformation:** Using Cloud Data Fusion for data enrichment and quality assurance.
3. **Data Loading:** Loading the transformed data into BigQuery.
4. **Visualization:** Creating interactive dashboards in Looker Studio.

---

## **Project Components**

### **1. Data Generation**
The dataset is synthetically generated using the [Faker](https://faker.readthedocs.io/en/master/) library in Python.  
Fields include:
- Product Name
- Category
- Price
- Units Sold
- Purchase Date  

**Script:** `data_generation.py`  
This script generates a CSV file and uploads it to a Google Cloud Storage bucket.

---

### **2. ETL Pipeline**
The ETL pipeline was built using Google Cloud Data Fusion:  
- **Data Extraction:** Raw data from Google Cloud Storage.  
- **Data Transformation:** Combining columns, calculating revenue, and ensuring data consistency.  
- **Data Loading:** Final transformed data stored in BigQuery for analysis.

---

### **3. Visualizations**
Looker Studio was used to create the following dashboards:  
- **Bar Chart:** Revenue by category.  
- **Line Chart:** Monthly revenue trends.  
- **Pie Chart:** Units sold distribution by category.  

---

## **How to Reproduce the Project**

### **Prerequisites**
- Google Cloud Platform account with a project setup.
- Access to Google Cloud Data Fusion, BigQuery, and Looker Studio.
- Python installed locally with necessary libraries (e.g., Faker, Google Cloud SDK).

---

### **Steps to Reproduce**
1. **Generate Data**  
   Run the `data_generation.py` script to create the dataset and upload it to Google Cloud Storage.

2. **Set Up Data Fusion**  
   - Create a Data Fusion pipeline to extract, transform, and load the data into BigQuery.  
   - Apply transformations such as combining product details and calculating revenue.

3. **Query Data in BigQuery**  
   Use SQL queries in BigQuery to analyze the transformed dataset.

4. **Create Visualizations**  
   Connect BigQuery to Looker Studio and create the specified visualizations.

---

## **Files in This Repository**
- `data_generation.py`: Python script to generate and upload the dataset.
- `project_report.pdf`: Final report detailing the methodology, results, and findings.
