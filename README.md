# Nexford-Assignment-Module-4

# Netflix Data Analysis Jupyter Notebook

## Overview
This Jupyter Notebook provides an in-depth analysis of Netflix's dataset, including data cleaning, exploration, and visualization. The dataset contains information about movies and TV shows available on Netflix, such as titles, genres, release years, ratings, and more.

## Prerequisites
Before running the notebook, ensure you have the following Python libraries installed:
- `pandas`
- `matplotlib`
- `seaborn`
- `wordcloud`

You can install these libraries using pip:

### 1. **Library Installation and Import**
    - The notebook begins with the installation of required libraries such as `pandas`, `matplotlib`, `seaborn`, and `wordcloud`. These libraries are essential for data manipulation, visualization, and generating word clouds.
    - The libraries are then imported, and a check is performed to ensure successful installation.

### 2. **Dataset Loading and Initial Exploration**
    - The Netflix dataset is loaded into a pandas DataFrame named `Netflix_shows_movies` using the `pd.read_csv()` function.
    - The first few rows of the dataset are displayed to verify successful loading.
    - The `info()` method is used to understand the structure of the dataset, including column names, data types, and non-null counts.

### 3. **Data Cleaning**
    - Missing values in the dataset are identified using the `isnull().sum()` method.
    - The `date_added` column is converted to a datetime format, and new columns (`day_added` and `month_added`) are extracted for further analysis.
    - Missing values are dropped using the `dropna()` method to ensure clean data for analysis.

### 4. **Data Exploration**
    - The dataset is explored to understand its structure and content:
      - The total number of rows and columns is determined using the `shape` attribute.
      - Duplicate entries are identified and counted using the `duplicated().sum()` method.
      - The oldest movies on Netflix are identified by sorting the dataset by the `release_year` column.
      - Categorical columns are described to understand their unique values and distributions.

### 5. **Content Analysis**
    - The distribution of content types (Movies vs. TV Shows) is analyzed using the `value_counts()` method.
    - The most common ratings and top 10 countries with the most content are identified.
    - The distribution of release years is explored to understand trends over time.
    - The `duration` column is converted to numeric minutes for analysis, and the average duration is calculated.

### 6. **Genre Analysis**
    - The most common genres are identified by splitting the `listed_in` column and counting occurrences using the `Counter` class.
    - A DataFrame is created to store genre counts for visualization.

### 7. **Visualizations**
    - Various visualizations are created to represent the findings:
      - **Most Watched Genres**: Bar plots are created using both `matplotlib` and `seaborn` to visualize the top genres.
      - **Ratings Distribution**: A bar plot is created to show the distribution of content ratings.
      - **Content Type Distribution**: A pie chart is used to display the proportion of Movies vs. TV Shows.
    - These visualizations provide insights into the dataset and highlight key trends.

### 8. **Top Actors and Countries**
    - The top 10 actors with the most appearances are identified and stored in a DataFrame named `cast_df`.
    - The top 10 countries with the most content are analyzed and visualized.

### 9. **Word Cloud**
    - A word cloud is generated to visualize the most frequent words in the dataset, providing a quick overview of popular terms.

### 10. **Summary**
    - The notebook provides a comprehensive analysis of the Netflix dataset, including data cleaning, exploration, and visualization. It highlights key trends, such as the most common genres, ratings, and countries, and provides actionable insights for further analysis.
