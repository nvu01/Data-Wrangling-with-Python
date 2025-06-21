# Data Wrangling with Python

This project explores two datasets gathered from the U.S. Census Bureau, focusing on the relationship between education and median earnings across U.S. counties. 
Through this analysis, we aim to address key research questions related to the impact of education on income levels and to identify trends in U.S. income distribution.

## Project Files

1. **`Data_Wrangling_Project.ipynb`**: Jupyter Notebook containing the full analysis, including data wrangling, analysis and visualizations. **Note**: This notebook requires the **`ACSST1Y2023.S2001-Data.csv`** dataset to run. The other files are not required to execute the notebook.
2. **`ACSST1Y2023.S2001-Data.csv`** (Required to run the Jupyter Notebook): Dataset 1 in CSV format. This dataset contains data on full-time earnings for individuals aged 16+ across U.S. counties.
3. **`raw_education.json`**: Dataset 2 in JSON format. This dataset provides information on the number of individuals aged 18 and older with a bachelor's degree, as well as the total population aged 18+ across U.S. counties.
4. **`cleaned_merged_data.csv`**: The final cleaned and merged dataset after performing the data wrangling steps.
5. **`Data_Wrangling_Project.html`**: Exported HTML version of the Jupyter Notebook for easy viewing.

## Structure of Jupyter Notebook

### 1. Problem Statement

Introduces the goal: to investigate how education levels relate to income across U.S. counties using Census data.

**Research Questions:**
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

Each dataset undergoes:
- Tidiness fixes: e.g., renaming coded columns, dropping irrelevant variables.
- Quality improvements: e.g., handling missing values and inconsistent formats.
- Data types are corrected for accurate analysis.

### 4. Combining Datasets
The cleaned datasets are merged on matching geographic identifiers to enable integrated analysis.

### 5. Data Store Updates
The merged dataset is saved as `cleaned_merged_data.csv` and used for further exploration.

### 6. Answer the Research Questions

Visualizations and statistical summaries are used to interpret findings.

### 7. References

- U.S. Census Bureau. [Earnings Data (2023)](https://data.census.gov/table?q=earnings&g=010XX00US$0500000)
- U.S. Census Bureau. [Education Data (2023)](https://data.census.gov/table?q=education&g=010XX00US$0500000)
- U.S. Census Bureau. [Available APIs](https://www.census.gov/data/developers/data-sets.html)
- U.S. Census Bureau. [2023 ACS Subject Tables Variables](https://api.census.gov/data/2023/acs/acs1/subject/variables.html)
- U.S. Census Bureau. [Census Data API User Guide](https://www2.census.gov/data/api-documentation/api-user-guide.pdf)
- U.S. Census Bureau. [Example API Queries](https://www.census.gov/data/developers/guidance/api-user-guide.Example_API_Queries.html#list-tab-559651575)

## Libraries Used

This project was implemented in a **Jupyter Notebook** environment. The following libraries were used:

- `pandas`: Data manipulation and cleaning.
- `matplotlib`: Visualizations.
- `requests`: API calls to the Census Bureau.
- `json`: Parsing JSON dataset.