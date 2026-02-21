📁 Portfolio Structure
├── README.md                  # Portfolio overview and project index
├── requirements.txt           # Python dependencies (pandas, seaborn, etc.)
├── data/                      # All raw datasets (CSV files)
│   ├── supermarket_sales.csv
│   ├── house_prices.csv
│   ├── student_performance.csv
│   ├── weather_data.csv
│   └── healthcare_covid.csv
├── notebooks/                 # Analysis notebooks for each domain
│   ├── project_retail.ipynb
│   ├── project_education.ipynb
│   ├── project_weather.ipynb
│   ├── project_healthcare.ipynb
│   └── project_finance.ipynb
├── reports/                   # Executive summaries and findings
│   ├── project_retail_report.txt
│   ├── project_education_report.txt
│   └── ...
├── src/                       # Reusable Python scripts
│   └── analysis_utils.py      # Core data loading and cleaning functions
├── visualizations/            # 15+ Charts across all 5 projects
│   ├── project1_daily_sales.png
│   ├── project2_score_box.png
│   ├── project3_temp_trends.png
│   └── ...
├── docs/                      # Detailed documentation and guides
└── presentation/              # Presentation slides (Placeholders)

# Supermarket-Sales-Analysis
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load Data
df = pd.read_csv('supermarket_sales (1).csv')
df['Date'] = pd.to_datetime(df['Date'])

# 1. Daily Sales Trend
daily_sales = df.groupby('Date')['Total'].sum().reset_index()

# 2. Product Line Performance
product_sales = df.groupby('Product_Line')['Total'].sum().sort_values(ascending=False).reset_index()

# 3. Payment Method Analysis
payment_counts = df['Payment'].value_counts()

# Insights Generation
total_rev = df['Total'].sum()
best_cat = product_sales.iloc[0]['Product_Line']
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/3f8127f1-81e8-4965-b31b-e28fd2f1dc26" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/043196fd-6f37-4b6e-b551-ef06129d1c99" />


🎓 Project 2: Student Performance Analysis
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load Simulated Data
df = pd.read_csv('student_performance.csv')

# 1. Subject Average Scores
math_avg = df['Math'].mean()
science_avg = df['Science'].mean()

# 2. Correlation: Attendance vs Performance
correlation = df['Attendance'].corr(df['Math'])

# 3. Grade Distribution
pass_rate = (df['Math'] >= 50).mean() * 100


🎓 Project 2: Student Performance Analysis

