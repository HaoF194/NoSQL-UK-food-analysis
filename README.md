# UK Food Establishments Analysis

## Overview
This project analyzes food establishment data in the UK using MongoDB and Python. It includes data preprocessing, database operations, and exploratory data analysis.

## Setup
- Database: MongoDB
- Collection: `establishments`
- Python libraries: pymongo, pandas, json, pprint

## Key Features

1. **Database Setup and Data Import**
   - Imported JSON data into MongoDB
   - Created `uk_food` database and `establishments` collection

2. **Data Preprocessing**
   - Added a new restaurant "Penang Flavours"
   - Updated BusinessTypeID for the new restaurant
   - Removed establishments in Dover
   - Converted data types (latitude, longitude to float; RatingValue to integer)

3. **Exploratory Analysis**
   - Identified establishments with hygiene score of 20
   - Found establishments in London with RatingValue >= 4
   - Located top 5 establishments with RatingValue 5, sorted by hygiene score
   - Analyzed establishments with hygiene score of 0 by Local Authority

## Key Findings

1. 82 establishments have a hygiene score of 20
2. 66 establishments in London have a RatingValue >= 4
3. The top 5 establishments with a RatingValue of 5 near "Penang Flavours" were identified
4. Thanet has the highest number of establishments (2260) with a hygiene score of 0

## Usage
1. Ensure MongoDB is installed and running
2. Import the JSON data into MongoDB
3. Run the Jupyter Notebooks in the following order:
   - `NoSQL_setup_starter.ipynb`
   - `NoSQL_analysis_starter.ipynb`

## Future Work
- Implement more complex queries for deeper insights
- Create visualizations of the data findings
- Develop a user interface for easy data exploration
