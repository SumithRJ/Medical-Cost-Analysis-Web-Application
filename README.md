# Medical Cost Analysis & Web Application

This repository contains a complete pipeline for analyzing medical cost data and deploying a simple web interface to interact with the results. It includes:

1. **Exploratory Data Analysis & Modeling** via a Jupyter notebook (`MedicalCost.ipynb`) using the provided dataset (`Medical cost.csv`).
2. **Django Web Application** (`mysite/`) to serve a user interface for viewing predictions or analysis summaries.

---

## 🚀 Project Overview

- **Data Analysis**  
  Use the Jupyter notebook to load, clean, and explore the `Medical cost.csv` dataset. Extract insights, build predictive models (e.g., regression), and evaluate performance.

- **Web Deployment**  
  A Django-based web app hosts the analysis results.  
  - **Flow.txt** documents the application workflow.  
  - **Procfile** and **runtime.txt** enable deployment on platforms like Heroku.

---

## 🧩 Repository Structure

```
medical_code/
└── Code/
    ├── Medical cost.csv            # Raw dataset of medical insurance costs
    ├── MedicalCost.ipynb           # Jupyter notebook: analysis & modeling
    └── mysite/                     # Django web application
        ├── db.sqlite3              # SQLite database (auto-generated)
        ├── Flow.txt                # Documentation of app workflow
        ├── manage.py               # Django management script
        ├── Procfile                # Heroku process definition
        ├── requirements.txt        # Python dependencies
        ├── runtime.txt             # Python runtime for Heroku
        ├── mysite/                 # Django project settings
        │   ├── settings.py
        │   ├── urls.py
        │   └── wsgi.py
        └── polls/                  # Django app for cost predictions
            ├── migrations/         # Auto-generated by Django
            ├── models.py           # Data models (if any)
            ├── views.py            # Request handlers and prediction logic
            ├── urls.py             # URL routing for the app
            └── templates/
                └── index.html      # Main UI template
```

---

## 🔧 Technologies & Dependencies

- **Python 3.7+**  
- **Data Science**: pandas, NumPy, scikit-learn, matplotlib, seaborn  
- **Notebook**: Jupyter  
- **Web Framework**: Django  
- **Deployment**: Procfile, Heroku (via `heroku create`, `git push heroku main`)

Install dependencies:

```bash
pip install -r Code/mysite/requirements.txt
```

---

## 🛠️ Getting Started

### 1. Data Analysis Notebook

1. Navigate to the `Code/` directory:
   ```bash
   cd medical_code/Code
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook MedicalCost.ipynb
   ```
3. Follow the notebook cells to:
   - Load and preprocess `Medical cost.csv`
   - Perform exploratory data analysis
   - Train and evaluate predictive models
   - Save or export model artifacts for the web app

### 2. Django Web Application

1. Navigate to the `mysite/` directory:
   ```bash
   cd medical_code/Code/mysite
   ```
2. Create & activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```
3. Install web app dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Apply migrations and run the server:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```
5. Open <http://127.0.0.1:8000/> in your browser to interact with the app.

---

## 📚 Workflow Documentation

- **Flow.txt** describes:
  - HTTP request and response cycle
  - Prediction endpoint logic
  - Template rendering steps

- **Procfile** and **runtime.txt** are configured for Heroku deployments:
  - `web: gunicorn mysite.wsgi`
  - Specifies Python version in use

---

## 🎯 Results & Next Steps

- **Notebook**: Generate plots, performance metrics, and save the final model.
- **Web App**: Integrate the trained model for live predictions.
- **Deployment**: Deploy to Heroku or any WSGI-compatible platform.

---

## 📬 Contact & Contributions

Contributions, issues, and feature requests are welcome!  
For questions or feedback, contact **sumithrjala@gmail.com**.
