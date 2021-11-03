# Work with Multiple Time Series Data

## Description:

In the field of Data Science, it is common to work with multiple time series simultaneously.

In this jupyter notebook, we learnt how to plot multiple time series at once, and how to discover and describe relationships between multiple time series.

---
## Contents:
1. Importing the required libraries
2. Importing & Loading the dataset
    - Knowing the dataset
    - Importing the dataset
    - Loading the dataset
3. Data Manipulations
4. Plotting the data
    - Basic Line Chart
    - Area Chart
5. Enhancing Plots
    - Clarity is Key
    - Colormap Argument
    - Adding information to plots
    - Facet Plots
6. Correlation b/w variables
    - Compute correlations
    - Correlation Matrix
    - Computing correlation matrix with pandas
    - Heat Maps
    - Cluster Maps
7. Conclusion

---
## Data Info:
The dataset contains the amount of different types of meat produced in the USA between 1944 and 2012. [(data)](https://github.com/Ravjot03/Visualizing-Time-Series-Data-in-Python/blob/main/Chapter-4/ch4_meat.csv)

---
## Theoretical Concepts & Key Pointers:

### 1. Area Chart
**Area charts** are commonly used when dealing with multiple time series, and can be leveraged to represent cumulated totals. With the `pandas` library, we can simply leverage the `.plot.area()` method to produce an area chart.

### 2. Enhancing Plots
Plotting and visualizing data that contains multiple time series can be a challenging task. While the `pandas` library can still be leveraged to perform this task, there are a number of parameters that can be applied in order to optimize the readability of the graphs.

Now, we will discuss how multiple times series can be clearly displayed simultaneously in Python.

- #### 2.1 Clarity is Key
  When plotting multiple time series, matplotlib will iterate through its default color scheme until all columns in the DataFrame have been plotted. Therefore, the repetition   of the default colors may make it difficult to distinguish some of the time series.
  
- #### 2.2 Colormap Argument
  To remedy this, the `.plot()` method has an additional argument called `colormap`.This argument allows us to assign a wide range of color palettes with varying contrasts     and intensities. We can either define our own Matplotlib colormap, or use a string that matches a colormap registered with matplotlib.

  Changing line colors with the color map argument.

### 3. Facet Plots
In order to overcome issues with visualizing datasets containing time series of different scales, we can leverage the `subplots` argument, which will plot each column of a DataFrame on a different subplot. In addition, the layout of our subplots can be specified using the `layout` keyword, which accepts two integers specifying the number of rows and columns to use. It is important to ensure that the total number of subplots is greater than or equal to the number of time series in our DataFrame. We can also specify if each subgraph should share the values of their x-axis and y-axis using the `sharex` and `sharey` arguments. Finally, we need to specify the total size of our graph (which will contain all subgraphs) using the `figsize` argument.

### 4. Correlation b/w variables
One of the most widely used methods to assess the similarities between a group of time series is by using the correlation coefficient. The correlation coefficient is a measure used to determine the strength or lack of relationship between two variables. The standard way to compute correlation coefficients is by using the Pearson's coefficient, which should be used when we think that the relationship between the variables of interest is linear. Otherwise, we can use the Kendall Tau or Spearman rank coefficient methods when the relationship between the variables of interest is thought to be non-linear.

- #### 4.1 Compute Correlations
  In Python, we can quickly compute the correlation coefficient between two variables by using the `pearsonr`, `spearmanr` or `kendalltau` functions in the `scipy.stats`       module. All three of these correlation measures return both the correlation and p-value between the two variables.

- #### 4.2 Correlation Matrix
  If we want to investigate the dependence between multiple variables at the same time, we will need to compute a correlation matrix.

  The result is a table containing the correlation coefficients between each pair of variables. Correlation coefficients can take any values between -1 and 1. A correlation     of 0 indicates no correlation, while 1 and -1 indicate strong positive and negative correlation.

  Importantly, a correlation matrix will be always be "symmetric", i.e., the correlation between x and y will be identical to the correlation between y and x. Finally, the     diagonal values will always be equal to 1, since the correlation between the variable x and a copy of itself is 1.

- #### 4.3 Computing Correlation Matrix with pandas
  The `pandas` library comes in with a `corr()` method that allows to measure the correlation between all pairs of columns in a DataFrame.

  Using the meat dataset, we selected the columns beef , veal and turkey and invoked the `corr()` method by invoking both the `pearson` and `spearman` methods.

- #### 4.4 Heat Maps
  A **heatmap** is a two-dimensional graphical representation of data where the individual values that are contained in a matrix are represented as colors.
  
  **Heatmap** is defined as a graphical representation of data using colors to visualize the value of the matrix. In this, to represent more common values or higher             activities brighter colors basically reddish colors are used and to represent less common or activity values, darker colors are preferred. Heatmap is also defined by the     name of the shading matrix. Heatmaps in Seaborn can be plotted by using the `seaborn.heatmap()` function.
  
- #### 4.5 Cluster Maps
  Heatmap is a useful tool to visualize correlation matrices, but the lack of ordering can make it difficult to read, or even identify which groups of time series are the       most similar.

  For this reason, it is recommended to leverage the `clustermap()` function in the `seaborn` library, which applies hierarchical clustering to our correlation matrix to plot   a sorted heatmap, where similar time series are placed closer to one another.
  
  The `clustermap()` function of seaborn plots a hierarchically-clustered heat map of the given matrix dataset. It returns a clustered grid index.

---
