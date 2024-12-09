# -ETL-Data-Pipeline-for-Global-Superstore-Analytics

# **Superstore ETL Pipeline**

## **Project Overview**
This project demonstrates a complete **ETL (Extract, Transform, Load)** pipeline using real-world datasets. The project is designed to:
- Extract raw sales and geolocation data.
- Transform the data into meaningful insights by cleaning, joining, and aggregating it.
- Load the processed data into a SQLite database for reporting and analytics.

## **Datasets**
The pipeline utilizes the following datasets:
1. **Superstore Sales Data**: Contains sales, customer, product, and shipping information.
2. **Geolocation Data**: Provides mapping between postal codes, cities, and regions.

Both datasets are included in the `data/raw` folder.

## **Pipeline Workflow**

### **1. Extraction**
- Load raw data from CSV files.
- Validate schema, handle missing data, and ensure consistency.

### **2. Transformation**
- Clean: Handle null values, standardize columns.
- Merge: Join datasets on common keys like `Postal_Code`.
- Feature Engineering: Create new columns like `Order Year` and `Profit Margin`.
- Aggregate: Summarize metrics such as sales by region and year.

### **3. Loading**
- Load transformed data into a SQLite database.
- Prepare data for visualization and further analysis.

## **Project Structure**
```plaintext
superstore_etl/
├── data/
│   ├── raw/                # Raw datasets
│   ├── processed/          # Processed datasets
│   ├── database/           # SQLite database
├── notebooks/              # Jupyter notebooks for ETL
├── README.md               # Project overview
```

## **Technologies Used**
- **Python**: Core programming language.
- **Jupyter Notebooks**: For step-by-step ETL documentation and execution.
- **Pandas**: Data manipulation and transformation.
- **SQLite**: Lightweight database for data storage.

## **How to Run**
1. Clone the repository:
   ```bash
   git clone <repository-link>
   cd superstore_etl
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open Jupyter Notebooks:
   ```bash
   jupyter notebook
   ```

4. Run the notebooks in the following order:
   - `1_Extract.ipynb`
   - `2_Transform.ipynb`
   - `3_Load.ipynb`

5. Check the SQLite database in the `data/database` folder for the processed data.

## **Deliverables**
- Cleaned and aggregated datasets in the `processed/` folder.
- SQLite database with organized tables for further analysis.

## **Future Improvements**
- Automate the pipeline using Apache Airflow or Prefect.
- Integrate the pipeline with cloud storage like AWS S3 or Google BigQuery.
- Build a dashboard using Power BI or Tableau to visualize the data.
