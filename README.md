# TMDb Movie Analysis
### Exploratory Data Analysis Using Python

## Project Overview

This project explores The Movie Database (TMDb) dataset as part of Udacity's *Investigate a Dataset* project. Using Python, Pandas, NumPy, and Matplotlib, I performed exploratory data analysis to better understand relationships between movie budgets, revenue, popularity, runtime, release periods, and genres.

The objective was to practice the complete data analysis process, including data wrangling, exploratory analysis, data visualization, and communicating findings.

## Research Questions

The analysis focuses on two primary questions:

1. How are adjusted budget, adjusted revenue, and popularity related among movies with reported financial data?
2. How do movie popularity and runtime vary across release decades and genres?

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Visual Studio Code

## Dataset

The dataset contains **10,866 movie records across 21 columns**, including information about budgets, revenues, popularity, vote averages, runtime, genres, and release years.

Dataset: TMDb Movies (provided through Udacity).

## Data Cleaning

Before performing the analysis, I inspected the dataset for missing values, duplicates, and invalid numerical information.

The cleaning process included:

- Removing duplicate records.
- Excluding movies with missing genre information.
- Removing records with zero-minute runtimes.
- Creating a separate financial dataset containing movies with positive adjusted budget and revenue values.
- Creating additional variables, including adjusted profit and release decade, to support the analysis.

Rather than discarding every movie with missing financial information, I retained those records for non-financial analysis.

**Final datasets:**

| Dataset | Records |
|---|---:|
| Original dataset | 10,866 |
| Cleaned dataset | 10,812 |
| Financial analysis subset | 3,854 |

## Key Findings

### Financial Relationships

The analysis identified moderate positive relationships between financial performance and several movie characteristics.

| Relationship | Pearson Correlation |
|---|---:|
| Adjusted Budget vs. Adjusted Revenue | 0.570 |
| Popularity vs. Adjusted Revenue | 0.547 |

Higher-budget and more popular movies generally demonstrated higher adjusted revenues, although considerable variation existed.

These relationships are observational and do not establish causation.

### Popularity, Genres, and Release Periods

- More recent decades generally displayed higher average TMDb popularity scores.
- Runtime varied across release decades.
- Adventure, Science Fiction, and Action demonstrated relatively high average popularity among the ten most common genres.
- Median adjusted profit differed across genres with sufficient financial information.

The analysis incorporated histograms, scatterplots, line charts, bar charts, and descriptive statistical summaries to explore these relationships.

## Limitations

Several limitations should be considered when interpreting the findings:

- A significant portion of the dataset contained zero or unavailable financial values.
- TMDb popularity is platform-specific and may not represent overall audience interest.
- Individual movies can belong to multiple genres, creating overlapping genre categories.
- Additional factors, such as marketing expenditures and distribution strategies, were not included in the analysis.
- Correlation does not establish causation.

Further research could explore these relationships using additional financial information and more advanced statistical models.

## Project Files

| File | Description |
|---|---|
| `TMDb_Investigate_a_Dataset_Maximus_Walker.ipynb` | Complete Jupyter Notebook containing the analysis and visualizations |
| `TMDb_Investigate_a_Dataset_Maximus_Walker.html` | Exported HTML report |
| `tmdb-movies(1).csv` | Original TMDb dataset |

## Running the Project

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code or Jupyter Notebook.
3. Install the required Python libraries: `pip install pandas numpy matplotlib jupyter`
4. Ensure the CSV file is located in the same directory as the notebook.
5. Open the `.ipynb` file, select a Python kernel, and run all cells sequentially.

## Author

**Maximus Walker**

B.S. Data Analytics | Western Governors University (WGU)

*This project was completed for educational and portfolio purposes as part of Udacity's Investigate a Dataset coursework.*