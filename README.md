# Mapping the Future of Data Science Careers
A Big Data Approach to Job Trend Analysis and Recommendation Systems
AIT-614 Final Project – Team 7

Project Summary
This project explores the rapidly evolving landscape of data science careers using real-world job posting data. Leveraging Databricks, MongoDB, PySpark, and Tableau, our goal is to identify current hiring trends, analyze salary distributions, and offer salary prediction models to support better career decisions for job seekers and deeper insights for employers and educators.

Objectives
Understand the distribution of job titles, employment types, and categories.

Analyze salary patterns by job title, employment type, and experience level.

Build a predictive model for salary forecasting using machine learning (Gradient Boosting).

Provide insights through visual dashboards for informed career decisions.

Dataset Overview
Source: ai-jobs.net

Refresh Rate: Updated monthly (2024)

Key Columns:

work_year: Year of job data collection

job_title: Specific role title

job_category: General classification of the role

salary_in_usa: Gross annual salary (USD)

experience_level: Entry, Mid, Senior, Executive

employment_type: Full-time, Part-time, Contract

work_setting: Remote, Hybrid, In-person

company_location: Company’s base location

company_size: Small, Medium, Big

Data Cleaning & Processing
Performed extensive preprocessing using Python and PySpark:

Removed null and duplicate records

Cleaned inconsistent labels (e.g., job levels, employment types)

Merged useful fields for clarity and modeling

Filtered irrelevant or incomplete rows

Used log transformation on salary to normalize skewness

Tools & Technologies Used
Tool	Purpose
Databricks	Main platform for PySpark-based data analysis
MongoDB	Hosted job posting data
PySpark	Processing large-scale data
Pandas, NumPy, Matplotlib	Local data manipulation and visualization
Scikit-learn	ML model training and evaluation
Tableau	Dashboards for visualization and reporting
Jupyter Notebooks	Exploratory data analysis

Exploratory Data Analysis (EDA)
Conducted deep EDA using plots such as:

Top 10 Job Titles – Salary distribution using box plots

Top Job Categories – Count of job postings

Employment Types – Salary spread by contract type

Company Locations – Mapping job opportunities by geography

Company Sizes – Job counts vs salary range across company scale

Notebook files:

EDA.ipynb – Contains cleaned dataset analysis and visuals

AIT614_FinalProject_Team7.ipynb – Includes modeling and dashboard steps

Predictive Modeling
Built a Gradient Boosting Regressor to predict salaries using features like:

Experience level

Employment type

Job category

Company size

Work setting

Model Evaluation:

RMSE: ~$53,491 (without transformation)

RMSE: ~$53,997 (after log transformation)

Insights:

Model struggles to predict extreme high salaries (bias at top end)

Log transformation improved consistency but further refinement is needed

📊 Tableau Dashboard
An interactive Tableau Public dashboard was created to visualize:

Job category frequency

Salary by title and employment type

Salary comparisons based on company size and location



Project Structure

.
├── data/
│   └── jobs_in_data_2024.csv
├── notebooks/
│   ├── EDA.ipynb
│   └── AIT614_FinalProject_Team7.ipynb
├── visualizations/
│   └── Tableau Dashboard (link or screenshots)
├── README.md
├── AIT-614-Sec001-Team7-Final.pdf
└── requirements.txt
Authors
Team 7 | AIT 614 – Big Data Essentials
Advisor: Dr. Eddy Zhang

Pritham Mahajan

Rakesh Somukalahalli Venkatappa

Nithish Bilasunur Manjunatha Reddy

Sai Sriram Dubusai

Usage Instructions
Prerequisites:
Databricks account

MongoDB Atlas setup with job data

PySpark and MongoDB Spark Connector installed

Steps:
Launch Databricks cluster with appropriate Spark version.

Install MongoDB Spark Connector:


org.mongodb.spark:mongo-spark-connector_2.12:3.0.1
Import the .ipynb notebooks from this repo into Databricks Workspace.

Attach notebooks to your cluster and run code cells.

Load data from MongoDB or CSV.

Run EDA and modeling scripts step-by-step.

View final Tableau dashboard via provided link.

Future Improvements
Integrate real-time job scraping from multiple sources

Add NLP-based skill extraction using BERT

Improve salary prediction with ensemble deep learning

Deploy the model via Flask or Streamlit for public use

Include cost-of-living adjustments for salary fairness

