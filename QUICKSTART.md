# Quick Start Guide

## Step 1: Set Up Python Environment

1. **Install Python** (if not already installed):
   - Download from [python.org](https://www.python.org/downloads/)
   - Make sure Python 3.11+ is installed

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   
   # Activate it:
   # Windows:
   venv\Scripts\activate
   # macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Step 2: Test the Projects (Optional)

### Test Sales Performance Dashboard:
```bash
cd projects/sales-performance-optimization-dashboard
python src/data_preprocessing.py
python src/sales_analysis.py
jupyter notebook notebooks/analysis_overview.ipynb
```

### Test Financial Forecasting Model:
```bash
cd projects/financial-forecasting-model
python src/data_preprocessing.py
python src/forecasting_model.py
jupyter notebook notebooks/forecasting_overview.ipynb
```

## Step 3: Push to GitHub

1. **Initialize Git** (if not already done):
   ```bash
   git init
   ```

2. **Add all files**:
   ```bash
   git add .
   ```

3. **Make your first commit**:
   ```bash
   git commit -m "Initial commit: Complete portfolio repository"
   ```

4. **Create a new repository on GitHub**:
   - Go to [github.com](https://github.com)
   - Click "New repository"
   - Name it `portfolio` (or your preferred name)
   - **Don't** initialize with README (you already have one)
   - Click "Create repository"

5. **Connect and push**:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git branch -M main
   git push -u origin main
   ```

## Step 4: Share Your Portfolio

- **Add to your resume**: Include your GitHub profile URL
- **LinkedIn**: Add portfolio link to your profile
- **Job applications**: Share the GitHub link in applications

## What Each File Does

- **README.md**: Main landing page - this is what recruiters see first!
- **profile/**: Your background and skills
- **projects/**: Your featured projects with code, data, and documentation
- **reports/**: Case studies showing business impact
- **requirements.txt**: Python dependencies needed to run projects

## Tips

- ✅ Keep the repository updated as you complete new projects
- ✅ Add screenshots of dashboards to replace the markdown placeholders in `assets/images/`
- ✅ Update README with new achievements or projects
- ✅ Use descriptive commit messages when making changes

