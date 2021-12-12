
# Predicting Superstore Sales using Time Series Analysis

## Project Overview:

This repository was created for the INFO 659 course at Drexel University, Introduction to Data Analytics.  The overall scope of this project was to predict sales numbers of Superstore from 2014-2015 using sales data from 2011-2014.  The Superstore dataset was downloaded from [Kaggle](https://www.kaggle.com/jr2ngb/superstore-data).

## File Manifest: 

- `SuperstoreSalesPredictor.Rmd` - Main R code that predicts sales.
- `SuperstoreSalesPredictor.ipynb - Main Python code that predicts sales.
- `Folder /data` - Contains all data files
    - `superstore_dataset2011-2015.csv` - Raw sales data (source in **Project Overview**)
    - `train.csv` - Monthly total sales data from January 2011 - December 2013.  Used for training.
    - `test.csv` - Monthly total sales data from January 2014 - December 2014.  Used for validation.
    - `initial_sales.csv` - Sales data grouped by `Order Date`
    - `daily_sales.csv` - Sales data grouped using `D` frequency.
    - `monthly_sales.csv` - Sales data grouped using `MS` frequency.
    - `yearly_sales.csv` - Sales data grouped using `YS` frequency.
- `Folder /documents` - Cotains all miscellaneous documents
    - `Project_Summary.docx` - Summary report of project made for class.


## Reason for Project:

Businesses may benefit from accurately predictions on sales and/or profit.  If a company knows what sales volume to expect for the following month or business quarter, they can adapt in what amount of overhead stock they purchase.  Our goal with this project attempts to answer two questions:

1. Can we confirm if sales and profit are increasing over time?
2. Can we accurately predict the sales of the year 2014 using the historical sales data from 2011-2013?

## Team Members

Our team consisted of the following individuals: 

- Zach Carlson, zc378@drexel.edu
- Sarah Haley, slh54@drexel.edu
- Nancy Melucci, njm99@drexel.edu

## Python Requirements
- Python ≥ 3.8. 
- Python modules, packages, and methods required: 
    - `matplotlib.pylot`
    - `numpy`
    - `pandas`
    - `seaborn`
    - `sklearn.metrics`
    - `statsmodels` ≥ 0.12.1
    - `warnings`

## R Requirements
- R libraries:
    - `forecast`
    - `ggfortify`
    - `knitr`
    - `kableExtra`
    - `lubridate`
    - `tidyverse`
    - `zoo`
   
## How to Execute Code: 

All of the code in this project needs to be opened with the Jupyter notebook environment. We recommend using [Anaconda](https://www.anaconda.com/products/individual) to help with Jupyter notebook.  Additionally, this code can be run in Google Colab or your preferred Python coding environment, assuming folder organization remains unchanged.

## Known Limitations of Project:

- **The dataset from Kaggle had little documentation.**  We could not confirm the units of the sales data.  We assumed it was in USD, however it could easily be CAD, considering this is data from a Canadian company.  The units themselves might not even be prices, but a quantity of items sold or some output from a formula we do not have access to.

- **We only have three years of training data.** To make the most accurate predictions, having as many years of data as possible would be ideal.  Fortunately, the data is fairly clean and shows clear, yearly seasonality.  However, the yearly trend for 2014 does look different from the years 2011-2013.

- **When predicting a given month of 2014, the model assumes we have all prior months.**  This improves the accuracy, of course, however, a team may want predictions extended out six months.  If this model was adjusted, the accuracy would most certainly drop.  However, we believe the assumption of having all prior months of data is more realistic and provides better predictions.
