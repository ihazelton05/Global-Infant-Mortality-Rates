# Global Infant Mortality Rates - Public Data Repository
This repository was created for Professor Gotzler's English 105 course during the Spring 2024 semester at the University of North Carolina at Chapel Hill.

## Contents
This repository contains a Python notebook called `final_subset_directions.ipynb` that was created using [Google Colab](https://colab.google/).
* The notebook itself provides instructions on how to condense the raw data into a smaller, more organized data subset.
* Using this `.ipynb` file, users can follow the provided instructions and learn how to create their own subset of the original, raw data.

The [data folder](/data) of this repository consists of three `.csv` files: `Infant Mortality Rates 1 - Infant Mortality Rates 1.csv`, `Infant Mortality Rates 2.csv`, and `final_subset.csv`.
* Both `Infant Mortality Rates 1 - Infant Mortality Rates 1.csv` and `Infant Mortality Rates 2.csv` include raw data that was acquired through [The World Bank](https://data.worldbank.org/indicator/SP.DYN.IMRT.IN).
* The `final_subset.csv` was created according to the instructions detailed in the `final_subset_directions.ipynb`. This `.csv` contains a subset of the previous `.csv` files' data, including the infant mortality rates associated with countries in varying regions of the world for comparison between the years 1960 and 2021.

The [data.viz](/data.viz) folder of this repository consists of two files: `data_viz.csv` and `final_subset_visual.png`.
* The `data_viz.csv` was created from the `final_subset.csv` data as explained in the __data visualization__ section below.
* `final_subset_visual.png` is the resulting data visualization.


## Purpose 
* The purpose of this data repository is to allow users to compare past global infant mortality rates to present global infant mortality rates.
* This data might be useful for sociologists or public health research scientists who wish to analyze global patterns in terms of infant mortality rates. In particular, these professionals can determine how global events have affected and continue to affect these patterns.

## Data Visualization
* To create the same visualization as below, you must further simplify the `final_subset.csv` created through the instructions detailed in the `final_subset_directions.ipynb`. This will reorganize the `final_subset.csv` data in a way that makes it easier for [Datawrapper](https://www.datawrapper.de/charts) to create an effective visualization.
> 1. Use the following command in your Python notebook to group the included countries by region as well as to calculate the mean infant mortality for each region between 1960 and 2021: `data_viz= final_subset.groupby("Region").mean("1960", "2021")`
> 2. Once you have finished this step, save your visualization data to your Google Drive using the following command: `data_viz.to_csv('gdrive/My Drive/Colab Notebooks/data_viz.csv')`
> 3. Download the new `data_viz.csv` to your computer so that you can use it later to create your data visualization.
* Now that you have successfully modified your data subset, navigate to the [Datawrapper website](https://www.datawrapper.de/charts) and create the following visualization by uploading the `data_viz.csv` to the site.
> 1. Select the "Grouped Bars" option in the "Chart Type" tab.
> 2. Navigate to the "Refine" tab and select the checkmark for the "Color Key" option under "Appearance".
> 3. You can personalize your visualization as you wish by changing the color of the bars or the name of the chart.
> 4. Once you have finished, download the data visualization.
* Now you have created a data visualization that demonstrates the differences in the mean infant mortality rate of each high-income region of the world between 1960 and 2021.
  > Keep in mind that this visualization represents __mean__ infant mortality rates. Because infant mortality rates typically represent the number of infant deaths per 1,000 live births, you would expect whole numbers. However, since this visual represents __mean__ infant mortality rates, a decimal is also appropriate.
 ![data-viz](/data.viz/final_subset_visual.png)
