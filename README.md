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
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/58935ebd-5d02-418c-bc88-8e3e5242bd58" />



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


<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/699c6c08-d2cc-4c0a-9b15-2b230a63115f" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/99238f5a-66c6-482e-9f3e-88c95b860176" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/76b2c863-8fe3-409e-aa6d-affa286eeb0d" />



🌤️ Project 3: Weather Data Analysis
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load Weather Data
df = pd.read_csv('weather_data.csv')
df['Date'] = pd.to_datetime(df['Date'])

# 1. Temperature Trends
df['Month'] = df['Date'].dt.month_name()

# 2. Rainfall Intensity
rainy_days = df[df['Rainfall'] > 10].count()

# 3. Humidity vs Temperature Relationship

<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/0a15217e-5c5b-4811-910c-a551b56d6b51" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/031c749e-2169-4fb8-8f29-ee417a99e19b" />
<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/6bb5bd7a-de18-4704-bcd3-836d7d4bc9a3" />





🏥 Project 4: Healthcare (COVID-19) Analysis
import pandas as pd
import matplotlib.pyplot as plt

# Load COVID Data
df = pd.read_csv('healthcare_covid.csv')
df['Date'] = pd.to_datetime(df['Date'])

# 1. Growth Tracking
cumulative_cases = df['New_Cases'].cumsum()
cumulative_recoveries = df['Recoveries'].cumsum()

# 2. Mortality Rate Analysis
mortality_rate = (df['Deaths'].sum() / df['New_Cases'].sum()) * 100

# 3. Bed Capacity Analysis
avg_bed_occupancy = df['Hospital_Beds_Occupied'].mean()

<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/c74dcedd-ee44-4ac2-a061-9a75852feb15" />
<img width="1200" height="600" alt="image" src="https://github.com/user-attachments/assets/45336f13-3370-4aea-a15c-8468499c5eaf" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/511d2b82-98e7-4be2-a837-2f8308e8cef5" />


🏠 Project 5: Real Estate (House Price) Analysis

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load House Price Data
df = pd.read_csv('house_prices (1).csv')

# 1. Price per SqFt Analysis
df['Price_per_SqFt'] = df['Price'] / df['Area']

# 2. Location-Based Analysis
loc_avg = df.groupby('Location')['Price'].mean()

# 3. Property Type Impact
type_dist = df['Property_Type'].value_counts()


<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/3ca15004-9961-486f-98bb-70ed875c4c63" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/52323b3a-da6e-4fd5-892c-e62688eeb2a9" />
<img width="1000" height="600" alt="image" src="https://github.com/user-attachments/assets/923ff4c8-ad00-40af-bf21-d1401ba73bc1" />










