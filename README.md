# PRODIGY_DS_01
Task 01: Created a bar chart and histogram to visualize the distribution of a population dataset. Used Python, Pandas, and Matplotlib to analyze age and gender distributions, demonstrating basic data visualization and exploratory data analysis (EDA) techniques as part of the Prodigy InfoTech Data Science Internship.

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
df = pd.read_csv('/content/population_dataset.csv')

print("Dataset loaded successfully. Here are the first 5 rows:")
print(df.head())
print("\nAvailable columns:")
print(df.columns)

# --- Uncomment and modify one of the examples below to visualize a variable ---

# Example 1: Histogram for a continuous variable (e.g., 'Age')
if 'Age' in df.columns:
    plt.figure(figsize=(10, 6))
    sns.histplot(df['Age'], bins=20, kde=True)
    plt.title('Distribution of Age')
    plt.xlabel('Age')
    plt.ylabel('Frequency')
    plt.show()
else:
    print("Column 'Age' not found. Please choose an existing continuous variable.")

<img width="841" height="547" alt="download" src="https://github.com/user-attachments/assets/21b69b5c-f4dd-4fc3-91eb-29c397ab6f93" />

# Example 2: Bar chart for a categorical variable (e.g., 'Gender')
if 'Gender' in df.columns:
    plt.figure(figsize=(8, 5))
    sns.countplot(data=df, x='Gender')
    plt.title('Distribution of Gender')
    plt.xlabel('Gender')
    plt.ylabel('Count')
    plt.show()
else:
    print("Column 'Gender' not found. Please choose an existing categorical variable.")

<img width="686" height="470" alt="download" src="https://github.com/user-attachments/assets/79457368-817b-4de5-946f-a91842da6fee" />
