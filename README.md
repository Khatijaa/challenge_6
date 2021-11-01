# challenge_6
## Project Overview

Analysis of the housing rental market data for San Francisco.

---

## Technologies

The application is in python and is uing the following libraries:

* [pandas](https://pandas-profiling.github.io/pandas-profiling/docs/master/index.html) - For data analysis.

* [Path](https://github.com/jaraco/path) - For relative and absolute path to the file.

* [hvplot.pandas](https://github.com/holoviz/hvplot) - For advanced graphs.



The operating system used in creating the application is Windows 10 64 bit. The application that used to code in notebook is Jupyter and then tested in Gitbash and Terminal. 

The application depends on excel file 'sfo_neighborhoods_census_data.csv' and 'neighborhoods_coordinates.csv'

The output files were:

```python
sfo_data_df = pd.read_csv(Path('./sfo_neighborhoods_census_data.csv'))
```

```python
neighborhood_locations_df = pd.read_csv(Path('./neighborhoods_coordinates.csv'),index_col='Neighborhood')
```
---

## Installation Guide

1. Open Gitbach or terminal and go ito the folder where you want to place the files.
2. Click on the blue "code" button which will allow you to clone.![<Code button in Github>]()
3. Then click on SSH or HTTPS as a clone method depending on if you have the SSH key setup. You will copy the link. You will then type "git clone" in Gitback or Terminal. Then paste the ssh or https information and press enter.
4. Next type "git pull" command in Temrianl or GitBash to pull the repository from the remote Github repository to a local directory on your computer.
5. You have access to the application. Also there will be all the python files that the application is depended on. 

---

## Usage

Below is a list of steps/analysis seen in the notebook:
    Calculate and Plot the Housing Units per Year:
    1. Step 1: Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.
    2. Step 2: Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.
    3. Step 3: Style and format the line plot to ensure a professionally styled visualization.
    Calculate and Plot the Average Sale Prices per Square Foot
    1. Step 1: Group the data by year, and then average the results.
    2. Step 2: Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.
    3. Step 3: Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.
    4. Step 4: Style and format the line plot to ensure a professionally styled visualization.
    Compare the Average Sale Prices by Neighborhood
    1. Step 1: Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.
    2. Step 2: Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year
    3. Step 3: Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.
    4. Step 4: Style and format the line plot to ensure a professionally styled visualization.
    Build an Interactive Neighborhood Map
    1. Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.
    2. Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.
    3. Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighborhoods_df. The second cell cleans the data and sets the “Neighborhood” column. Be sure to run these cells to create the all_neighborhoods_df DataFrame, which you’ll need to create the geospatial visualization.
    4. Using hvPlot with GeoViews enabled, create a points plot for the all_neighborhoods_df DataFrame.
---

## Contributors

This application was provided by the instrutor of Columbia University and addtional code was added by Khatija Azeem to complete the project.

---

## License

For this application, I used Github to uplaod the file into a repository. Since this is a public file, there will be no restriction on usage of this code. 