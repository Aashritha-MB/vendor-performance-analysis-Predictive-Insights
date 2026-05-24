# Vendor Performance & Predictive Analytics System

## 📌 Project Overview
This project is a comprehensive data analytics and predictive insight system developed using Python, Pandas, SQLAlchemy, Power BI/Tableau dashboards, and Jupyter Notebook. The project focuses on collecting, processing, analyzing, visualizing, and predicting vendor and brand performance data to generate meaningful business insights.

The system automates data ingestion into a database, performs exploratory data analysis, generates interactive dashboards, and provides predictive insights for future vendor performance. The project demonstrates practical implementation of data analysis workflows, database management, dashboard creation, and business intelligence techniques used in real-world organizations.

---

## 🎯 Objectives
- Perform efficient data ingestion into a database.
- Analyze vendor and brand performance metrics.
- Generate summarized vendor reports.
- Create interactive dashboards for business visualization.
- Explore and visualize datasets for business insights.
- Generate predictive insights for future vendor trends.
- Support data-driven business decision-making.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Core programming language |
| Pandas | Data cleaning and analysis |
| SQLAlchemy | Database connectivity and ORM |
| SQLite | Database storage |
| Jupyter Notebook | Exploratory data analysis |
| Power BI / Tableau | Dashboard creation and visualization |
| CSV Files | Dataset storage and processing |

---

## 📂 Project Structure

```bash
Project/
│
├── ingestion_db.py
├── get_vendor_summary.py
├── Exploratory data analysis.ipynb
├── Dashboard.pbix / dashboard files
├── brand_performance.csv
├── future_vendor_predictions.csv
├── requirements.txt
└── README.md
```

---

## 📄 File Description

### 1. `ingestion_db.py`
This script is responsible for reading datasets and inserting the processed data into the database. It handles database connections, table creation, and data loading operations.

### 2. `get_vendor_summary.py`
This script generates vendor-wise summaries and analytical reports based on the stored data. It helps in understanding vendor performance and trends.

### 3. `Exploratory data analysis.ipynb`
A Jupyter Notebook used for performing exploratory data analysis (EDA), data visualization, and identifying patterns in the dataset.

### 4. `Dashboard.pbix / Dashboard Files`
Contains interactive dashboards used for visualizing vendor performance, sales trends, brand analysis, and predictive insights using business intelligence tools such as Power BI or Tableau.

### 5. `brand_performance.csv`
Contains brand-related performance data used for analysis and reporting.

### 6. `future_vendor_predictions.csv`
Contains prediction-related data for future vendor performance analysis and forecasting.

---

## ⚙️ Installation & Setup

### Step 1: Clone the Repository

```bash
git clone <repository_url>
cd Project
```

### Step 2: Create Virtual Environment (Optional but Recommended)

#### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux / Mac
```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 📦 Install Required Packages

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

### Run Data Ingestion Script
```bash
python ingestion_db.py
```

### Generate Vendor Summary
```bash
python get_vendor_summary.py
```

### Open Jupyter Notebook
```bash
jupyter notebook
```

Then open:

```bash
Exploratory data analysis.ipynb
```

### Open Dashboard
Open the dashboard file (`.pbix` or Tableau dashboard) using the respective BI tool to explore interactive visualizations and predictive insights.

---

## 📊 Features
- Database integration using SQLAlchemy
- Automated CSV data ingestion
- Vendor performance analysis
- Exploratory Data Analysis (EDA)
- Interactive dashboards and visualizations
- Predictive insights and trend forecasting
- Business intelligence reporting
- Structured and scalable project design

---

## 📈 Dashboard Insights
The dashboard provides:
- Vendor performance tracking
- Brand-wise sales analysis
- Revenue and growth trends
- Comparative performance metrics
- Future vendor prediction insights
- Interactive charts and filters for better decision-making

---

## 📈 Expected Outcomes
- Better understanding of vendor and brand performance.
- Automated report generation and visualization.
- Identification of business trends and patterns.
- Predictive insights for future planning.
- Improved decision-making using analytical dashboards.

---

## 🔮 Future Enhancements
- Integration with machine learning models.
- Real-time dashboard updates.
- Cloud database integration.
- Web-based analytics dashboard using Flask or Django.
- Advanced predictive analytics and forecasting models.
- Automated alert and reporting systems.

---

## Dataset Note
Large dataset files are not included in this repository due to GitHub storage limitations.  
The datasets used in this project can be downloaded from Kaggle and placed inside the `data/` folder before running the project.

Kaggle Dataset: Vendor Performance Data
