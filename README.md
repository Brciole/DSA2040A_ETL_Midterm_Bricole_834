#  DSA2040A ETL Midterm – Bricole Asiachi

This project demonstrates a complete **ETL (Extract, Transform, Load)** pipeline using Python and Pandas for the DSA2040A midterm.


##  1. Project Overview

The goal of this ETL lab is to:
- Load raw and incremental data from CSV files
- Clean and transform the data
- Save the final output in efficient formats like Parquet
- Demonstrate each stage of the ETL process clearly through Jupyter notebooks


##  2. ETL Phases & Notebooks

### `etl_extract.ipynb`
- Loads two CSV files: `raw_data.csv` and `incremental_data.csv`
- Displays `.head()` and `.info()` for both
- Identifies missing values and duplicates
- Saves raw copies into `data/` folder

### `etl_transform.ipynb`
Applies 4 key transformations:
1. **Cleaning**: Removes duplicates, fills missing values
2. **Enrichment**: Adds `total_price = quantity * unit_price`
3. **Structural**: Converts `order_date` to datetime
4. **Filtering**: Drops rows with null critical fields

- Outputs saved in `transformed/` as:
  - `transformed_full.csv`
  - `transformed_incremental.csv`

### `etl_load.ipynb`
- Loads transformed CSV files
- Saves them in Parquet format for efficient storage
- Output saved in `parquet/` as:
  - `full_data.parquet`
  - `incremental_data.parquet`



##  3. Tools Used

  Tool          Purpose                        
 
  Python        Programming language            
  Pandas        Data manipulation and cleaning  
  Jupyter       Notebooks for ETL steps         
  Parquet       Efficient file storage format   
  PowerShell    Command-line for Git & file ops 
  Git + GitHub  Version control and publishing  



##  4. How to Run the Project

### Prerequisites
- Python 3.8+
- `pandas` and `pyarrow` installed:
  ```bash
  pip install pandas pyarrow
