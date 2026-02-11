🌍 World Bank Economic Analytics & ETL Pipeline
End-to-End Data Engineering & Statistical Analysis Project
A production-style data pipeline analyzing GDP and Population trends using World Bank datasets to evaluate economic disparities and development patterns.
📌 Project Overview
This project builds a complete ETL and analytics workflow using World Bank economic datasets.
The objective was to:
Standardize inconsistent global datasets
Clean and transform multi-source economic data
Handle missing values using multiple strategies
Perform statistical outlier detection
Analyze GDP vs Population relationships
Create modeling-ready datasets
This project demonstrates real-world data engineering and analytical problem-solving skills.
🚀 Key Highlights
✔ Multi-source data integration (Projects, GDP, Population, Country Metadata)
✔ ISO-3 country code standardization
✔ Missing value strategy comparison (Mean, Forward Fill, Backward Fill)
✔ Wide-to-Long time-series transformation
✔ Feature engineering with One-Hot Encoding
✔ Outlier detection using Tukey’s IQR method
✔ Economic visualization & insight generation
🛠 Tech Stack
Languages
Python
Data Processing
Pandas
NumPy
PyCountry
regex
Visualization
Matplotlib
Seaborn
Machine Learning Utilities
Scikit-learn
Geospatial (Ready for Expansion)
GeoPandas
Folium
🔄 End-to-End Workflow
1️⃣ Data Extraction
Downloaded dataset from Kaggle
Loaded:
Projects dataset
GDP dataset
Population dataset
Country metadata
Performed schema validation and data inspection
2️⃣ Data Standardization & Cleaning
🔹 Country Code Normalization
Used pycountry to map country names to ISO-3 codes
Created manual mapping dictionary for unmatched records
Resolved inconsistencies across datasets
🔹 Data Type Engineering
Converted year columns (1960–2020) to numeric
Cleaned and converted monetary columns
Converted approval and closing dates to datetime
Extracted year and weekday features
🔹 Removed Non-Country Aggregates
Filtered out:
OECD members
World aggregates
Regional economic groupings
Ensured clean country-level analysis.
3️⃣ Missing Value Strategy Comparison
Instead of blindly filling missing values, multiple approaches were tested:
Mean Imputation
Forward Fill (ffill)
Backward Fill (bfill)
Forward + Backward combination
Ensured:
No null GDP values
No null Population values
This demonstrates data reliability handling before analysis.
4️⃣ Data Reshaping (Wide → Long Format)
Transformed time-series data using:
pd.melt()
From:
Country | 1960 | 1961 | 1962 | ...
To:
Country | Year | GDP
Country | Year | Population
Benefits:
Enables time-series analytics
Supports scalable merging
Improves modeling readiness
5️⃣ Feature Engineering
📊 Sector-Based Project Analysis
Cleaned sector labels
Removed "(Historic)" artifacts
Applied One-Hot Encoding
Created modeling-ready dataset:
Project Cost | Approval Year | Sector Indicators
📊 Economic Analysis
📈 Time-Series Visualization
Plotted GDP & Population trends for selected countries to analyze:
Growth trajectories
Economic volatility
Development progression
📦 Distribution Analysis (2020)
Generated boxplots to:
Understand GDP distribution
Identify economic skew
Detect extreme values
🔎 GDP vs Population Relationship
Built annotated scatter plots
Filtered out mega economies (US, China, India, etc.)
Revealed clearer mid-tier economic relationships
📉 Statistical Outlier Detection
Applied Tukey’s IQR method:
Q1 = 25th percentile
Q3 = 75th percentile
IQR = Q3 - Q1
Identified:
GDP outliers
Population outliers
Countries extreme in both metrics
Demonstrates applied statistical reasoning in economic datasets.
🎯 Business & Analytical Insights
Large economies significantly distort GDP visualization.
High population does not guarantee high GDP performance.
Some small-population countries are strong GDP outliers.
Aggregate economic regions must be removed for accurate modeling.
