#  Exploratory Data Analysis on Lung Cancer  Using Python

## Project Overview
The Lung Cancer Data Analysis project aims to explore patterns and factors related to lung cancer using exploratory data analysis (EDA). The project involves data visualization, summary statistics, and insights into features such as smoking, gender, and age, which may be associated with the occurrence of lung cancer.

## Technologies Used
- **Programming Language**: Python
- **Libraries**: 
  - `pandas` (for data manipulation)
  - `numpy` (for numerical operations)
  - `matplotlib` (for plotting graphs)
  - `seaborn` (for advanced data visualization)

## Data Source
- **Lung Cancer Data Set** (CSV format)

## Data Preprocessing
- **Imported data**: The lung cancer dataset was loaded into a pandas DataFrame.
- **Checked for missing values**: `df.isnull().sum()` to identify missing data.
- **Summary statistics**: `df.describe()` provided a quick overview of the dataset.

## Exploratory Data Analysis (EDA)
- **Basic Info**: `df.info()` to understand data types and non-null entries.
- **Age Distribution**:
  - `plt.histplot(df['AGE'], bins=10, kde=True)` to visualize the distribution of ages.
  - **Min Age**: `print(df['AGE'].min())`
  - **Max Age**: `print(df['AGE'].max())`
- **Gender Distribution**:
  - Bar plot of gender counts using `df['GENDER'].value_counts()` and visualized with `plt.bar()`.
- **Lung Cancer Distribution**:
  - Bar plot showing lung cancer counts using `df['LUNG_CANCER'].value_counts()`.
  - Created contingency tables for gender and lung cancer relationships.
- **Cancer by Gender**: 
  - Analyzed the gender distribution for individuals with lung cancer.
- **Smoking vs. Lung Cancer**: 
  - Count plot using `sns.countplot()` to visualize the relationship between smoking and lung cancer.
  - Contingency tables for percentages of smokers and non-smokers with lung cancer.
  
- **Pie Chart of Gender Distribution Among Lung Cancer Patients**:
  - Filtered the data for patients with lung cancer and counted occurrences of each gender.
  - Created a pie chart using:
    ```python
    # Filter the data for patients with lung cancer
    c = df[df['LUNG_CANCER'] == 'YES']

    # Count the occurrences of each gender
    gender_counts = c['GENDER'].value_counts()

    # Create a pie chart
    plt.pie(gender_counts, labels=gender_counts.index, autopct='%1.1f%%', startangle=90)
    plt.title('Gender Distribution Among Lung Cancer Patients')
    plt.show()
    ```

## Key Performance Indicators (KPIs)
- **Smoking and Lung Cancer**: Percentage of smokers and non-smokers with lung cancer.
- **Cancer Distribution by Gender**: Percentage of lung cancer cases in males vs. females.
- **Age Analysis**: Box plot for age distribution and calculation of average age for lung cancer patients.

## Insights
- **Age Distribution**: The average age of lung cancer patients was calculated and visualized using a box plot.
- **Smoking**: A significant relationship between smoking and lung cancer was observed using contingency tables.
- **Gender Analysis**: Males showed a higher percentage of lung cancer cases compared to females.

## Visualizations
1. **Age Distribution**: Histogram with a KDE to show the age distribution of the dataset.
2. **Gender Distribution**: Bar plot showing counts of males and females.
3. **Lung Cancer Distribution**: Bar plot visualizing the counts of cancer and non-cancer cases.
4. **Smoking vs Lung Cancer**: Count plot to show the relationship between smoking and lung cancer.
5. **Box Plot**: Box plot of age to identify the spread and outliers in age distribution.

## How to Use
1. Download the lung cancer dataset from the repository.
2. Run the Python script to load, preprocess, and analyze the data.
3. Explore the various visualizations and insights generated from the data.
