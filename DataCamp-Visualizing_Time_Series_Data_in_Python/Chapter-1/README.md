# Introduction to Time Series Plots

## Description:
In this jupyter notebook, we will learn how to leverage basic plottings tools in Python, and how to annotate and personalize your time series plots.

---
## Contents:
1. Importing the required libraries
2. Importing the dataset
    - Knowing the dataset
    - Loading the dataset
3. Exploratory Data Analysis (EDA)
4. Data Pre-processing
5. Data Visualizations
    - Basic Time Series Plot
    - Adding labels to the plot
    - Changing the style of the plot
    - Formatting the plot style
    - Subsetting the time series
    - Adding Vertical & Horizontal Markers
    - Adding Shaded Regions
    - Markers & Shaded Regions
6. Conclusion

---
## Data Info:
This time series dataset contains the number of "great" inventions and scientific discoveries from year 1860 to 1959. [(data)](https://github.com/Ravjot03/Visualizing-Time-Series-Data-in-Python/blob/main/Chapter-1/ch1_discoveries.csv)

---
## Key Pointers:

- ### Adding Vertical & Horizontal Markers
    Additional annotations can help further emphasize specific observations or events.
    
    By adding markers at specific timestamps of our time series plot, we can highlight significant events.
    - **Vertical Markers :** `.axvline()` - This function adds the vertical lines across the axes of the plot.
    - **Horizontal Markers :** `.axhline()` - It is used to add a horizontal line across the axis.
- ### Adding Shaded Regions
    When plotting time series data in Python, it is also possible to highlight complete regions of the time series plot.
    - **Vertically Shading Regions :** `.axvspan()` - This function sets the vertical rectangle across the axes of the plot.
    - **Horizontally Shading Regions :** `.axhspan()` - This function sets the horizontal rectangle across the axes of the plot.

---
