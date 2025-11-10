

-----

# Zomato Restaurant Exploratory Data Analysis (EDA)

  

## 📖 Project Overview

This project performs an in-depth exploratory data analysis (EDA) on the Zomato restaurant dataset. The goal is to analyze data from 9,551 restaurants to uncover insights and trends related to:

  * Restaurant ratings and their drivers
  * Price ranges and average costs
  * Popular cuisines and locations
  * The availability of services like online delivery and table booking

## Dataset

The dataset (`zomato.csv`) is a CSV file containing 21 columns (features) that describe various attributes of each restaurant.

**Key features analyzed:**

  * `Restaurant Name`: Name of the restaurant
  * `City`: City where the restaurant is located
  * `Cuisines`: List of cuisines offered
  * `Average Cost for two`: The average cost for a meal for two people
  * `Price range`: A numerical tier (1-4) representing price level
  * `Aggregate rating`: The restaurant's average rating (out of 5.0)
  * `Votes`: The number of ratings the restaurant has received
  * `Has Online delivery`: (Yes/No)
  * `Has Table booking`: (Yes/No)

## 🛠️ Technologies Used

  * **Python 3**
  * **Jupyter Notebook**
  * **Pandas** (for data manipulation and cleaning)
  * **NumPy** (for numerical operations)
  * **Matplotlib** (for plotting)
  * **Seaborn** (for advanced and statistical visualizations)

## 📊 Analysis Workflow

The analysis is structured in a clear, step-by-step process:

1.  **Data Loading:** The `zomato.csv` file is loaded into a Pandas DataFrame.

2.  **Data Cleaning:**

      * **Missing Values:** Identified 9 missing values in the `Cuisines` column. Given the small number, these rows were dropped to maintain data integrity.
      * **Data Types:** Inspected and confirmed data types for all columns.

3.  **Exploratory Data Analysis (EDA):**

      * **Numerical Variables:**

          * Analyzed the distribution of `Aggregate rating`, `Votes`, and `Average Cost for two`.
          * Found that `Aggregate rating` has a large number of '0' values, indicating unrated restaurants.
          * `Votes` and `Average Cost for two` are heavily right-skewed, which is typical for these kinds of features.

      * **Categorical Variables:**

          * Analyzed the frequency of `City`, `Cuisines`, `Price range`, `Has Online delivery`, and `Has Table booking`.
          * Split the `Cuisines` column to identify the most popular individual cuisines across all restaurants.

4.  **Bivariate Analysis (Finding Relationships):**

      * **Correlation Heatmap:** A heatmap was generated to visualize the correlation between numerical features (`Aggregate rating`, `Votes`, `Price range`, `Average Cost for two`).

      * **Rating vs. Price:** A box plot was used to compare `Aggregate rating` across different `Price range` tiers.

      * **Rating vs. Votes:** A scatter plot showed a clear positive relationship: restaurants with more votes tend to have higher ratings.

      * **Rating vs. Online Delivery:** A box plot was used to see if having online delivery impacts a restaurant's rating.

## 💡 Key Questions & Insights

This analysis answered several key questions about the restaurant landscape:

  * **Which cities have the most restaurants?**

      * The dataset is heavily dominated by restaurants in India, with New Delhi having the highest count.

  * **What are the most common cuisines?**

      * After splitting multi-cuisine entries, **North Indian** and **Chinese** were found to be the two most popular cuisines.

  * **Is there a link between Votes and Rating?**

      * Yes, there is a strong positive correlation. As the number of votes increases, the aggregate rating tends to be higher and more reliable. Unrated (0.0) restaurants all have 0 votes.

  * **Does a higher Price Range guarantee a better rating?**

      * Not necessarily. While Price Range 3 and 4 have a higher median rating, Price Range 1 and 2 also have many highly-rated restaurants. The highest ratings (4.5-4.9) are found across all price ranges.

  * **How does Online Delivery affect ratings?**

      * Restaurants offering online delivery, on average, have slightly higher ratings than those that do not.

## 📈 Visualizations

  * **Count Plots (Bar Charts):** Used to show the frequency of top cities, top cuisines, and price ranges.
  * **Histograms & KDE Plots:** Used to understand the distribution of numerical features like `Aggregate rating`.
  * **Pie Charts:** Used to show the simple Yes/No ratio for `Has Online delivery` and `Has Table booking`.
  * **Box Plots:** Used to compare `Aggregate rating` against categorical features (`Price range`, `Has Online delivery`).
  * **Scatter Plot:** Used to visualize the relationship between `Votes` and `Aggregate rating`.
  * **Heatmap:** Used to display the Pearson correlation matrix for all numerical features.

## 🚀 How to Run this Project

To run this analysis on your own machine:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/zomato-eda.git
    cd zomato-eda
    ```
2.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn jupyterlab
    ```
3.  **Launch Jupyter Lab:**
    ```bash
    jupyter lab
    ```
4.  Open the `.ipynb` notebook file and run the cells sequentially.# EDA-ASSIGNMENT-
