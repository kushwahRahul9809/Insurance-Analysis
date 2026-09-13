🏥 Insurance Analysis

An exploratory data analysis and preprocessing project using the Insurance dataset with Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, and Scikit-learn.

📌 Project Overview

This project explores customer insurance data and prepares the dataset for further analytical or machine-learning work.

The notebook covers:

Exploratory Data Analysis (EDA)

Dataset inspection and descriptive statistics

Missing-value checking

Duplicate removal

Categorical encoding

Region one-hot encoding

BMI category feature engineering

Numerical feature standardization

Pearson correlation analysis

Chi-square testing for categorical features

Final feature selection

📂 Dataset

The dataset contains 1,338 rows and 7 columns.

Column

Description

age

Customer age

sex

Customer sex

bmi

Body Mass Index

children

Number of children

smoker

Smoking status

region

Customer region

charges

Insurance charges

The notebook reports no missing values and identifies 1 duplicate row, which is removed during preprocessing.

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

SciPy

Scikit-learn

Jupyter Notebook

🔎 Exploratory Data Analysis

The notebook performs:

Dataset shape inspection

First-record inspection

Data-type inspection

Descriptive statistics

Missing-value analysis

Column inspection

Numerical feature distributions

Sex distribution

Smoker distribution

Numerical boxplots

Correlation heatmap

Dataset Summary

Metric

Value

Rows

1,338

Columns

7

Missing values

0

Duplicate rows found

1

Average age

39.21

Average BMI

30.66

Average children

1.09

Average charges

13,270.42

Category Counts

Category

Count

Non-smoker

1,064

Smoker

274

Southeast

364

Southwest

325

Northwest

325

Northeast

324

📊 Visualizations

Numerical Distributions

<img width="2140" height="1417" alt="numerical_distributions" src="https://github.com/user-attachments/assets/29cb62c2-699c-4fd0-8754-f629d41d0262" />


Sex Distribution

<img width="1241" height="877" alt="sex_distribution" src="https://github.com/user-attachments/assets/1c7bd169-7cb9-4fc1-b532-6be39afb55b7" />


Smoker Distribution

<img width="1241" height="877" alt="smoker_distribution" src="https://github.com/user-attachments/assets/4702ca1a-a338-4945-9e57-158f05ed3ea5" />


Correlation Heatmap

<img width="1367" height="1059" alt="correlation_heatmap" src="https://github.com/user-attachments/assets/5fe93d4f-a7a4-4fde-9242-42c583631899" />


Boxplots

<img width="2141" height="1417" alt="boxplots" src="https://github.com/user-attachments/assets/3e71da30-522e-48fe-9e42-eada59721aba" />


GitHub image links: The README uses relative image paths such as images/correlation_heatmap.png. After uploading the images folder to the same GitHub repository, GitHub will automatically render these images in the README.

🧹 Data Cleaning & Preprocessing

A copy of the original dataframe is created as df_cleaned.

The notebook then:

Removes duplicate rows.

Converts sex into a binary variable:

male = 0

female = 1

Converts smoker into a binary variable:

no = 0

yes = 1

Renames:

sex → is_female

smoker → is_smoker

Applies one-hot encoding to region.

Converts the processed dataframe to integer form where used.

🧠 Feature Engineering

BMI is divided into four categories:

BMI Range

Category

< 18.5

Underweight

18.5 – 24.9

Normal

25.0 – 29.9

Overweight

≥ 30

Obese

The BMI categories are one-hot encoded.

The numerical columns age, bmi, and children are standardized using StandardScaler.

📈 Feature Analysis

The notebook calculates Pearson correlation between selected features and charges.

Among the selected features, is_smoker has the strongest positive Pearson correlation with insurance charges, followed by age.

A Chi-square test is also performed on selected categorical features after dividing charges into four quantile-based groups.

🎯 Final Feature Set

The notebook creates a final dataframe containing:

age
is_female
bmi
children
is_smoker
charges
region_southeast
bmi_category_Obese

📁 Project Structure

Insurance-Analysis/
│
├── Insurance analysis.ipynb
├── insurance.csv
├── README.md
│
└── images/
    ├── numerical_distributions.png
    ├── sex_distribution.png
    ├── smoker_distribution.png
    ├── correlation_heatmap.png
    └── boxplots.png

▶️ How to Run

1. Clone the repository

git clone <your-repository-url>
cd Insurance-Analysis

2. Install dependencies

pip install numpy pandas matplotlib seaborn scipy scikit-learn jupyter

3. Open Jupyter Notebook

jupyter notebook

4. Run

Open:

Insurance analysis.ipynb

Make sure insurance.csv is in the same directory as the notebook.

📌 Key Takeaways

The dataset has 1,338 records and 7 original columns.

No missing values are reported.

One duplicate row is removed.

Smoking status shows the strongest Pearson correlation with charges among the selected features in the notebook.

BMI categories provide an additional engineered representation of BMI.

age, bmi, and children are standardized before the final feature-selection stage.

👤 Author

Rahul Kushwaha

📄 Project Files

Insurance analysis.ipynb — analysis and preprocessing notebook

insurance.csv — source dataset

images/ — charts displayed in this README

⭐ If you find this project useful, consider giving the repository a star!
