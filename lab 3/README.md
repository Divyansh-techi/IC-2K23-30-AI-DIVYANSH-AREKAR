Data Science Practical Programs

This folder contains Python practical programs for the first three topics:

Dataset Loading

Exploratory Data Analysis (EDA)

Data Cleaning

Requirements

pip install pandas

1. Dataset Loading

import pandas as pd

df = pd.read_csv("data.csv")

print(df.head())
print("\nDataset Information:")
print(df.info())

2. Exploratory Data Analysis (EDA)

import pandas as pd

df = pd.read_csv("data.csv")

print("First 5 rows:")
print(df.head())

print("\nLast 5 rows:")
print(df.tail())

print("\nShape:")
print(df.shape)

print("\nColumns:")
print(df.columns)

print("\nData Types:")
print(df.dtypes)

print("\nStatistical Summary:")
print(df.describe())

print("\nUnique Values:")
print(df.nunique())

print("\nMissing Values:")
print(df.isnull().sum())

3. Data Cleaning

import pandas as pd

df = pd.read_csv("data.csv")

# Remove duplicate rows
df = df.drop_duplicates()

# Remove rows where all values are missing
df = df.dropna(how="all")

# Clean column names
df.columns = df.columns.str.strip()

# Remove extra spaces from text columns
for column in df.select_dtypes(include="object"):
    df[column] = df[column].str.strip()

print("Cleaned Dataset:")
print(df.head())

print("\nShape after cleaning:")
print(df.shape)

Dataset

Keep your dataset in the same folder as the Python program:

project/
├── data.csv
├── dataset_loading.py
├── eda.py
├── data_cleaning.py
└── README.md

Replace data.csv with your actual CSV filename if required.