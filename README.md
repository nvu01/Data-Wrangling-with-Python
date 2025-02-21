# Data Wrangling with Python

This project explores two datasets gathered from the U.S. Census Bureau, focusing on the relationship between education and median earnings across U.S. counties. Through this analysis, we aim to address key research questions related to the impact of education on income levels and to identify trends in U.S. income distribution.

The project files included in this repository are:

1. **`Data_Wrangling_Project.ipynb`**: Jupyter Notebook containing the full analysis, including data wrangling, analysis and visualizations. **Note**: This notebook requires the **`ACSST1Y2023.S2001-Data.csv`** dataset to run. The other files are not required to execute the notebook.
2. **`ACSST1Y2023.S2001-Data.csv`** (Required to run the Jupyter Notebook): Dataset 1 (Full-Time Earnings) in CSV format.
3. **`raw_education.json`**: Dataset 2 (Educational Attainment) in JSON format.
4. **`cleaned_merged_data.csv`**: The final cleaned and merged dataset after performing the data wrangling steps.
5. **`Data_Wrangling_Project.html`**: Exported HTML version of the Jupyter Notebook for easy viewing.

## Structure of Jupyter Notebook

### 1. Problem Statement

In this project, we will explore the following two datasets from the U.S. Census Bureau:

#### Dataset 1: Full-Time Earnings (2023)
This dataset contains data on full-time earnings for individuals aged 16+ across U.S. counties.

#### Dataset 2: Educational Attainment (2023)
This dataset provides information on the number of individuals aged 18 and older with a bachelor's degree, as well as the total population aged 18+ across U.S. counties.

#### Research Questions:
- What’s the relationship between the percentage of bachelor's degree holders and median earnings across U.S. counties?
- Which income range has the highest percentage in the U.S.?

### 2. Data Gathering

#### 2.1 Dataset 1: Full-Time Earnings Data
- **Type**: CSV file
- **Gathering method**: This data was manually downloaded from the U.S. Census Bureau website: [Earnings Data (2023)](https://data.census.gov/table?q=earnings&g=010XX00US$0500000).

#### 2.2 Dataset 2: Educational Attainment Data
- **Type**: JSON file
- **Gathering method**: This data was gathered using the U.S. Census Bureau API: [Education Data (2023)](https://data.census.gov/table?q=education&g=010XX00US$0500000).

### 3. Data Wrangling

#### 3.1 Dataset 1: Full-Time Earnings Data
##### Tidiness Issues:
- **Unnecessary Variables**: Some columns were not relevant to the analysis.
- **Column Headers Are Codes**: Some column headers contained codes instead of descriptive names.
- **Column Headers Are Values, Not Variables**: Some column headers represented values, not variables.

##### Quality Issues:
- **Inconsistency**: Inconsistent data formatting and entry errors were found.
- **Completeness Issues**: Missing values in some counties needed to be addressed.
- **Validity Issues**: Incorrect data types were identified and corrected.

#### 3.2 Dataset 2: Educational Attainment Data
##### Tidiness Issues:
- **Unnecessary Variables**: Columns containing irrelevant information were removed.
- **Column Headers Are Not Available**: Some columns lacked headers.
- **Column Headers Are Codes**: Column headers were numeric codes instead of descriptive names.
- **Column Headers Are Values, Not Variables**: Some column headers were values, not actual variables.

##### Quality Issues:
- **Inconsistency**: The data had some inconsistencies in format and categorization.
- **Completeness Issues**: Missing values were present across certain counties.
- **Validity Issues**: Incorrect data types were found and converted.

### 4. Combining Datasets
Once both datasets were cleaned, they were combined into a single dataset to enable an analysis of the relationship between education and earnings. This involved matching counties from both datasets and merging them on the appropriate identifiers.

### 5. Data Store Updates
The cleaned and merged data was saved into a new file for analysis. This updated data store is used for answering the research questions.

### 6. Answer the Research Questions

#### 6.1 Define and Answer the Research Questions
- **Research Question 1**: What’s the relationship between the percentage of bachelor's degree holders and median earnings across U.S. counties?
- **Research Question 2**: Which income range has the highest percentage in the U.S.?
    
#### 6.2 Reflection

### 7. References
- U.S. Census Bureau. [Earnings Data (2023)](https://data.census.gov/table?q=earnings&g=010XX00US$0500000)
- U.S. Census Bureau. [Education Data (2023)](https://data.census.gov/table?q=education&g=010XX00US$0500000)
- U.S. Census Bureau. [Available APIs](https://www.census.gov/data/developers/data-sets.html)
- U.S. Census Bureau. [2023 ACS Subject Tables Variables](https://api.census.gov/data/2023/acs/acs1/subject/variables.html)
- U.S. Census Bureau. [Census Data API User Guide](https://www2.census.gov/data/api-documentation/api-user-guide.pdf)
- U.S. Census Bureau. [Example API Queries](https://www.census.gov/data/developers/guidance/api-user-guide.Example_API_Queries.html#list-tab-559651575)

## Libraries Used

This project was implemented in a **Jupyter Notebook** environment. The following libraries were used:

- `Pandas`: For data manipulation and cleaning.
- `Matplotlib`: For creating visualizations and exploring data insights.
- `Requests`: For accessing data from the U.S. Census Bureau API.
- `JSON`: For handling the JSON format of Dataset 2.