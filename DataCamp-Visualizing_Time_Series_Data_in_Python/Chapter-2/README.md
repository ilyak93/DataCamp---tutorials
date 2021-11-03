# Plotting Rolling Models and Aggregate Values Model

## Description:
In this jupyter notebook, we will learn about deeper understanding of our time series data by computing summary statistics and plotting aggregated values from our data.

---
## Contents:
1. Importing the necessary libraries
2. Importing and Loading the dataset
    - Knowing the dataset
    - Importing the dataset
    - Loading the dataset
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
    - Dealing with Missing Values
      - Finding Missing Values
      - Handling Missing Data
5. Plotting Rolling Models
    - Moving Average Model
    - Rolling Mean & Variance
6. Plotting Aggregate Value Models
    - Displaying Aggregated values
7. Some more Data Visualizations
    - Boxplots
    - Histograms
    - Density Plots
8. Conclusion

---
## Data Info:
This time series dataset contains the CO2 measurements at the Mauna Loa Observatory, Hawaii between the years of 1958 and 2001. You can download dataset from here - [(data)](https://github.com/Ravjot03/Visualizing-Time-Series-Data-in-Python/blob/main/Chapter-2/ch2_co2_levels.csv).

---
## Theoretical Concepts & Key Pointers:

### 1. Feature Engineering
Feature engineering is the process of transforming raw data into features that better represent the underlying problem to the predictive models, resulting in improved model accuracy on unseen data.

#### 1.1 Dealing with Missing Values

- **Finding Missing Values**
 
In the field of Data Science, it is common to encounter datasets with missing values. This is especially true in the case of time series data, where missing values can occur if a measurement fails to record the value at a specific timestamp.

Missing values are one of the most common problems we can encounter when we prepare our data for machine learning. The reason for the missing values might be human errors, interruptions in the data flow, privacy concerns, etc. Whatever the reason, missing values affect the performance of machine learning models.

- **Handling Missing Values or Imputation** -

We are filling the missing values in our dataset with `bfill` (backfilling) method.

In this method, missing values are replaced using the next valid observation in the dataset.

### 2. Plotting Rolling Models

The stability of the model over time. A common time-series model assumption is that the coefficients are constant with respect to time.

### 3. Boxplots

Boxplots represent a graphical rendition of the minimum, median, quartiles, and maximum of our data.

We can generate a boxplot by calling the `.boxplot()` method on a DataFrame.

### 4. Histograms

Another method to produce visual summaries is by leveraging histograms, which allows us to inspect the data and uncover its underlying distribution, as well as the presence of outliers and overall spread.

We used the standard `.plot()` method but specified the kind argument to be `'hist'`. In addition, we also added the `bins=100` parameter, which specifies how many intervals (i.e bins) we should cut our data into.

### 5. Density Plots

In practice, histograms can be a substandard method for assessing the distribution of our data because they can be strongly affected by the number of bins that have been specified. Instead, kernel density plots represent a more effective way to view the distribution of our data.

The standard `.plot()` method is specified with the kind argument set to `'density'`. We also specified an additional parameter `linewidth`, which controls the width of the line to be plotted.

---
