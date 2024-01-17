
# Advanced Stock Data Processing and Analysis

This Python project focuses on advanced processing and analysis of stock market data. It encompasses a comprehensive workflow, from data downloading and cleaning to detailed indicator calculation and correlation analysis. This project is ideal for financial analysts and data scientists interested in exploring stock market trends and correlations using sophisticated data processing techniques.

## Features

### Price Data Downloader
- Downloads historical stock data for approximately 11,895 tickers.
- Implements a mechanism to record the time taken for each download and adds a delay to ensure a consistent 1.05-second interval between downloads, preventing API rate limiting issues with Yahoo Finance.
- Handles tickers differently based on weekdays and weekends to ensure the data's relevance and accuracy.

### Price Data Cleaner
- Cleans and filters the downloaded stock price data based on predefined criteria, such as price limits, NaN values, and minimum data days.
- Provides diagnostics post-cleaning, including the total number of files processed and removed.

### Indicator Calculator
- Performs complex calculations on the cleaned data to generate various stock market indicators.
- Includes advanced techniques like local extrema detection, best-fit line calculation, and channel metrics analysis.

### Control Logic
- Intermediate data processing including backfilling, forward filling, and outlier handling.
- Dynamic scaling of data using both MinMaxScaler and RobustScaler.
- Processes individual stock data files by computing indicators, scaling, and saving them to a new directory.

### Data Testing/Improvement
- A testing mode to process a limited number of files for quicker iterations and improvements.
- Calculates and analyzes correlations for specific columns of interest in the processed data.
- Generates visualizations of correlation data for intuitive understanding.

## Execution Flow
- The main function orchestrates the data downloading, cleaning, indicator calculation, scaling, and saving processes.
- The top of each file contains comments indicating the estimated time to run, providing a rough idea of the script's duration.

## Requirements
- Libraries: `pandas`, `numpy`, `yfinance`, `scipy`, `plotly`, `tqdm`, `sklearn`
- Data: Stock ticker symbols in a text file, data storage directories

## How to Use
- Set the desired mode (Testing or Full-scale processing).
- Run the main script to initiate the full workflow.
- Check the output directories for processed data and correlation analysis results.

## Authors
- [@JonIsHere242](https://github.com/JonIsHere242)
