# Nobel Prize Winners Analysis

## Project Overview

This project analyzes the Nobel Prize winners dataset, covering awards from 1901 to 2024, to identify key patterns and trends. The dataset, sourced from the Nobel Prize API, includes comprehensive details on laureates, categories, and awards. The analysis addresses specific questions about gender, birth country, and historical trends, while incorporating visualizations to enhance data exploration. The project is implemented in a Jupyter Notebook (`notebook.ipynb`) using Python and popular data science libraries.

## Objectives

The analysis answers the following questions:
- **Most Common Gender and Birth Country**: Identify the most frequently awarded gender and birth country.
- **US-Born Winners by Decade**: Determine the decade with the highest proportion of US-born Nobel Prize winners.
- **Female Laureates by Decade and Category**: Find the decade and category with the highest proportion of female winners.
- **First Female Winner**: Identify the first woman to receive a Nobel Prize and her category.
- **Repeat Winners**: List individuals or organizations who have won multiple Nobel Prizes.
- **Additional Exploration**: Analyze the age distribution of winners at the time of their award.

## Repository Structure

- **`notebook.ipynb`**: The main Jupyter Notebook containing the data analysis, visualizations, and results.
- **`data/nobel.csv`**: The dataset file containing Nobel Prize winner data from 1901 to 2023 (updated programmatically with 2024 winners).
- **`README.md`**: This file, providing an overview and instructions for the project.

## Dependencies

To run the notebook, ensure the following Python libraries are installed:
- `pandas`: For data manipulation and analysis.
- `seaborn`: For statistical visualizations.
- `numpy`: For numerical computations.
- `matplotlib`: For plotting graphs.

Install the dependencies using pip:
```bash
pip install pandas seaborn numpy matplotlib
```

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/nobel-prize-analysis.git
   cd nobel-prize-analysis
   ```

2. **Ensure Data Availability**:
   - Place the `nobel.csv` file in the `data/` directory. The notebook expects this file to contain the Nobel Prize dataset up to 2023.
   - The notebook programmatically adds 2024 winners; no manual data update is required.

3. **Set Up Environment**:
   - Ensure Python 3.9 or later is installed.
   - Install dependencies as listed above.

4. **Run the Notebook**:
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook notebook.ipynb
     ```
   - Execute the cells sequentially to perform the analysis and generate visualizations.

## Notebook Details

### Data Preprocessing
- The dataset is loaded from `nobel.csv` and updated with 2024 Nobel Prize winners using a programmatically constructed DataFrame.
- A `decade` column is created by grouping years into 10-year intervals (e.g., 1900, 1910).
- A `female_winner` boolean column is added to indicate female laureates.
- Birth dates are converted to datetime for age calculations, handling missing or invalid data gracefully.

### Analysis
- **Top Gender and Country**: Computed using `value_counts()` and `mode()` to find the most common gender (`Male`) and birth country (`United States of America`).
- **US-Born Winners**: The proportion of US-born winners per decade is calculated, identifying the 2000s as the peak decade.
- **Female Proportion**: A grouped analysis determines the decade and category with the highest female winner proportion, stored as a dictionary (e.g., `{2020: 'Literature'}`).
- **First Female Winner**: The earliest female winner is identified by sorting female laureates by year (Marie Curie, Physics, 1903).
- **Repeat Winners**: Laureates with multiple awards are found using `value_counts()`, resulting in a list of names (e.g., Marie Curie, International Committee of the Red Cross).
- **Age Analysis**: The age at award is calculated and visualized for deeper insights into winner demographics.

### Visualizations
- **Gender Distribution**: Bar plot showing counts of male and female winners.
- **Top Birth Countries**: Bar plot of the top 10 birth countries by winner count.
- **US-Born Proportion Over Time**: Line plot of the proportion of US-born winners by decade.
- **Female Proportion Heatmap**: Heatmap showing female winner proportions by decade and category.
- **Age Distribution**: Histogram with kernel density estimation of winners’ ages at the time of award.

## Results

The key findings are stored in the following variables:
- `top_gender`: `'Male'`
- `top_country`: `'United States of America'`
- `max_decade_usa`: `2000`
- `max_female_dict`: `{2020: 'Literature'}`
- `first_woman_name`: `'Marie Curie'`
- `first_woman_category`: `'Physics'`
- `repeat_list`: List of laureates with multiple awards (e.g., `['Marie Curie', 'International Committee of the Red Cross', ...]`)

## Further Exploration

The notebook includes an additional analysis of winners' ages at the time of their award, visualized as a histogram. Users are encouraged to explore further questions, such as:
- Trends in specific categories over time.
- Geographic distribution of winners by organization country.
- Prize share patterns (e.g., solo vs. shared awards).

## Notes
- The dataset includes some missing values (e.g., birth dates, organization details), which are handled appropriately in the analysis.
- The 2024 data is programmatically added based on official Nobel Prize announcements for 2024, ensuring the analysis is current as of August 30, 2025.
- Visualizations use `seaborn` and `matplotlib` for clarity and aesthetic appeal.



## Contact

For questions or contributions, please open an issue or submit a pull request on the repository.