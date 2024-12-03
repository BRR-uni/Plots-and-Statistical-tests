# Plots and Statistical tests in Python

## Python code to plot time series data and to run statistical tests from data imported from Excel

This scripts where used to create the plots used in my Master's degree thesis. I wont share the file with the raw data for this reason. However, the functions used to create this kind of plots might be useful for more people so I share the code here.
The code requires to have an Excel file with a table containing the properly named pages so that the code can find the file, and where to extract the data from

### Time-series_AND_Correlations_Seaborn-plots

The first script was created to make time series plots and correlation joinplots from an excel file. After loading the data, a jointplot for each experimental group is created using Seaborns libray. Next lineplots are created for the variables that were longitudinally measured. This cell is repeated to plot the experimental data together, next the data separated by age, and lastly the experimental data plus some additional individuals that were excluded from the results of my project.

### Swarmplot-barplot-overlay_AND_Statistics-test

This script is intended to open an Excel file, read the content, generate plots, and perform statistical test from its data. First a function to avoid overlapping of data points is defined. Next it is defined a function to create a swarmplot on top of a barplot. Additionally, each datapoint is represented a digit to uniquely identify each individual in the experimental group. Later are defined the statistical test to check for normality, equality of variances, and differences between groups. Lastly all variables measured are iterated to generate the corresponding graphs and statistical test.



## Known issues (Work in progress)

This code is far from perfect, so I'll next mention some of the improvements I would like to implement in it:

  - Toggle between young and old plots should be automated, and not a repetition of that block of code
  - The range for each variable should be automated
  - The statistical tests could be chosen given some criteria depending on the data
  - I would love to generalize the code for more than just this very specific Excel file with very specific names for each field
  - Finally I want to plot a line with asterisks or p values indicating when there is a significant difference between the bars plotted. 
