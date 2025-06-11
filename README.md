# ETL_Pipeline
# 🛠️ ETL Data Integration Pipeline

This project demonstrates a simple ETL (Extract, Transform, Load) pipeline using Python. It combines structured data from multiple file formats — CSV, JSON, and XML — transforms it, and exports a clean, consolidated dataset as a `.csv` file.

---

## 📂 Project Structure
etl_project/
├── extract.py # Extract logic for CSV, JSON, and XML
├── transform.py # Data transformation logic
├── load.py # Save output to CSV
├── main.py # Main runner script
├── data/ # Folder containing source files (CSV, JSON, XML)
├── output/ # Folder where final_report.csv will be saved
└── README.md # Project documentation



---

## 🔧 Technologies Used

- Python 3.x
- pandas
- xml.etree.ElementTree
- glob
- OS module

---

## 🚀 How It Works

### 1. **Extract**
Reads all files from `data/` directory:
- Skips the final output file if it already exists
- Uses custom functions to extract data from:
  - `.csv` files using `pandas.read_csv()`
  - `.json` files using `pandas.read_json()`
  - `.xml` files using `ElementTree`

### 2. **Transform**
Applies the following transformations:
- Drops missing rows
- Converts height and weight to integers
- Capitalizes name strings

### 3. **Load**
Saves the final transformed dataset to:
