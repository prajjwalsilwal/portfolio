# Environment Setup Notes

This document describes the recommended environment setup for running the portfolio projects.

## Python Version

**Recommended**: Python 3.11 or higher

Python 3.9+ is also supported, but Python 3.11 is recommended for best performance and compatibility.

### Checking Your Python Version

```bash
python --version
# or
python3 --version
```

## Required Libraries

The projects in this portfolio use the following Python libraries:

### Core Data Analysis
- **pandas** (>= 1.5.0): Data manipulation and analysis
- **numpy** (>= 1.23.0): Numerical computing

### Visualization
- **matplotlib** (>= 3.6.0): Basic plotting and visualization
- **seaborn** (>= 0.12.0): Statistical data visualization

### Machine Learning / Forecasting
- **scikit-learn** (>= 1.2.0): Machine learning models (for regression-based forecasting)

### Jupyter Notebooks
- **jupyter** (>= 1.0.0): Interactive notebook environment
- **ipykernel** (>= 6.20.0): Jupyter kernel

## Installation Instructions

### Option 1: Using pip (Recommended)

Create a virtual environment first:

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install packages
pip install pandas numpy matplotlib seaborn scikit-learn jupyter ipykernel
```

### Option 2: Using requirements.txt

A `requirements.txt` file can be created with the following contents:

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
jupyter>=1.0.0
ipykernel>=6.20.0
```

Then install using:

```bash
pip install -r requirements.txt
```

## Database Tools

### SQL Server / Azure SQL Database

For projects that reference SQL Server or Azure SQL Database:
- SQL Server Management Studio (SSMS) or Azure Data Studio for query development
- Appropriate database drivers for Python (if connecting programmatically):
  - `pyodbc` for SQL Server
  - `sqlalchemy` for database abstraction

### MySQL

If working with MySQL:
- MySQL Workbench or command-line tools
- Python library: `mysql-connector-python` or `pymysql`

## BI Tools

### Power BI

- **Power BI Desktop**: For dashboard development (Windows only)
- **Power BI Service**: For publishing and sharing dashboards (web-based)
- **Power Query**: Integrated within Power BI Desktop for data transformation

### Tableau

- **Tableau Desktop**: For dashboard development (Windows/Mac)
- **Tableau Public**: Free version for public sharing

## Development Environment

### Recommended IDE/Editor

- **Jupyter Notebook / JupyterLab**: For interactive data analysis
- **VS Code**: With Python extension and Jupyter extension
- **PyCharm**: Professional Python IDE (optional)

### VS Code Extensions (Optional)

- Python
- Jupyter
- Pylance (Python language server)
- Python Docstring Generator

## Project-Specific Setup

### Sales Performance Optimization Dashboard

1. Navigate to project directory:
   ```bash
   cd projects/sales-performance-optimization-dashboard
   ```

2. Install dependencies (if not already installed globally)

3. Run data preprocessing:
   ```bash
   python src/data_preprocessing.py
   ```

4. Run sales analysis:
   ```bash
   python src/sales_analysis.py
   ```

5. Open Jupyter notebook:
   ```bash
   jupyter notebook notebooks/analysis_overview.ipynb
   ```

### Financial Forecasting Model

1. Navigate to project directory:
   ```bash
   cd projects/financial-forecasting-model
   ```

2. Install dependencies (if not already installed globally)

3. Run data preprocessing:
   ```bash
   python src/data_preprocessing.py
   ```

4. Train forecasting model:
   ```bash
   python src/forecasting_model.py
   ```

5. Open Jupyter notebook:
   ```bash
   jupyter notebook notebooks/forecasting_overview.ipynb
   ```

## Troubleshooting

### Common Issues

1. **ModuleNotFoundError**: Ensure virtual environment is activated and packages are installed
2. **Jupyter kernel not found**: Install ipykernel: `pip install ipykernel`
3. **CSV encoding issues**: Ensure CSV files are UTF-8 encoded (default for sample data)

### Getting Help

- Check Python and package versions match requirements
- Ensure you're in the correct project directory when running scripts
- Verify file paths in scripts match your directory structure

## Notes on Sample Data

All datasets in this portfolio are **synthetic/sample data** created for demonstration purposes. They are not real business data and should not be used for actual business decisions.

For production use:
- Replace sample data with actual business data sources
- Implement proper data security and access controls
- Follow your organization's data governance policies

