# module-5-challenge

## Pymaceuticals Inc. Analyses

### Trends

* Removing duplicates ID the total number of mice is 248. We can also see that 49% are female and 51% are male
* We can see that the correlation between mouse weight, and average tumor volume is 0.84.
* When looking for outliers in the top 4 treatments, Infubinol was the only regimen that shows one.
* Beased in the data results it shows that Ramicane and Capomulin are the most effective treatments.

## Background

You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Prepare the Data

* Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

* Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

* Display the updated number of unique mice IDs.

![Cleaning Data part 1](./Images/Cleaning_data_1.png)


![Cleaning Data part 2](./Images/Cleaning_data_2.png)


## Generate Summary Statistics

* Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

* Your summary statistics should include:

* A row for each drug regimen. These regimen names should be contained in the index column.

* A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

### Solution

![Summary Statistics](./Images/Summary_Statistics.png)

## Create Bar Charts and Pie Charts

1. Generate two bar charts. Both charts should be identical and show the total number of time points for all mice tested for each drug regimen throughout the study.

    * Create the first bar chart with the Pandas DataFrame.plot() method.

    * Create the second bar chart with Matplotlib's pyplot methods.

2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

    * Create the first pie chart with the Pandas DataFrame.plot() method.

    * Create the second pie chart with Matplotlib's pyplot methods.

### Solution 1

#### Using Pandas

![Mice tested for each drug regimen using Pandas](./Images/Pan_mice_tested_per_regimen.png)

#### Using Pyplot

![Mice tested for each drug regimen using Pyplot](./Images/Pan_mice_per_treat.png)


### Solution 2

#### Using Pandas

![Distruition of gender using Pandas](./Images/Distribuition_of_gender_pandas.png)

#### Using Pyplot

![Distribuition of gender using Pyplot](./Images/Distribuition_of_gender_pyplot.png)

## Calculate Quartiles, Find Outliers, and Create a Box Plot

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

    * Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    * Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

    * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

    * Determine outliers by using the upper and lower bounds, and then print the results.

2. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

### Solution 1

![Top 4](./Images/Top_4.png)

![Outliers](./Images/Outliers.png)

### Solution 2

![Final Tumor Volume](./Images/Final_tumor_volume_per_treatment.png)

## Create a Line Plot and a Scatter Plot

1. Select a mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

![Single Mouse](./Images/Single_mouse.png)

2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

![Tumor Volume x Mouse Weight](./Images/Tumor_volume_x_Mouse_weight.png)

## Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment.

The correlation between mouse weight and the average tumor volume is 0.84

2. Plot the linear regression model on top of the previous scatter plot.

![Correlation](./Images/Correlation.png)








