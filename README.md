# PyBer_Analysis
Matplotlib, Panda, Numpy and Scipy


## Overview of the analysis: Explain the purpose of the new analysis.
The purpose of this project was to learn how to generate graphs using matplotlib via Jupyter Notebook, as part of my Week 6 module for DU Coding Bootcamp.  The following graphs were generated by the matlab method (matplotlib.pyplot) - plt.plot(); Object Oriented Interface method - ax.plot; and the matplotlib method - df.plot
* line 
* bar
* scatter
* bubble 
* pie
* box-and-whisker plots using Matplotlib

I also learned how to write code that enabled me to:
* Add and modify features of Matplotlib charts.
* Add error bars to line and bar charts.
* Determine mean, median, and mode using Pandas, NumPy, and SciPy statistics.

To do this, I analyzed two different csv datafiles from a mock ride sharing company called PyBer, one datafile contained 2,376 rows and 4 columns of data; and the second containied 121 rows and 3 columns of data.  The data was comprised of: 
* city, 
* city type(urban, suburban, and rural), 
* ride ID, 
* fare, 
* driver counts per city
* date

After opening the data, I looked for null values and determined if it needed to be cleaned in any way.  I then used pd.merge() to merged the dataframes by city.  From this new dataframe, I used the groupby(), count(), and sum() functions to generate the total rides, total drivers, total fare, and then calcuated the average fare per ride, and average fare per driver, all dependent on city type.  I also used the map() function to format the column values to be displayed as dollar amounts with 2 decimal places and comma markers. See the table below.

**insert table1 here**

I then used the groupby(), count(), and sum() functions to generate a new dataframe containing date of ride, city type, and fare, with formated fare values as above.  I then did the following:
* reset the the index - reset_index() 
* created a pivot table - df.pivot(); where index="date", columns= "type", values="fare"
* sorted the data to only display rides from April 1, 2019 to April 28, 2019 - loc() 
* changed the dataframe to a TimeIndex type and replaced NaN values with 0
* resampled the dataframe and summed the fare values per week - df.resample("W") and sum()
* create a new dataframe (see table below)

**insert table2 here**

I used the object-oriented interface method to plot the resampled DataFrame using the df.plot() function, added lables and a title, then used the style.use('fivethirtyeight') to format the graph and generated a legend (See figure below)

**insert table2 here**

## Results: Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.

## Summary: Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.
