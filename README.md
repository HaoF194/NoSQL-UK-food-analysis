# UK Food Establishments Analysis

## Project Overview
This project conducts an in-depth analysis of food establishments across the United Kingdom using MongoDB and Python. It encompasses data preprocessing, database operations, and exploratory data analysis to derive insights into food hygiene ratings and geographical distribution of establishments.

## Technical Setup
- **Database**: MongoDB
- **Primary Collection**: `establishments` in `uk_food` database
- **Programming Language**: Python 3.x
- **Key Libraries**: 
  - pymongo: For MongoDB interactions
  - pandas: For data manipulation and analysis
  - json: For JSON file handling
  - pprint: For formatted console output

## Project Structure
The project is divided into two main Jupyter Notebooks:
1. `NoSQL_setup_starter.ipynb`: Handles initial database setup and data preprocessing
2. `NoSQL_analysis_starter.ipynb`: Conducts exploratory data analysis and generates insights

## Key Features and Processes

### 1. Database Setup and Data Import
- Imported extensive JSON dataset into MongoDB
- Created and configured the `uk_food` database
- Established the `establishments` collection to store food establishment data

### 2. Data Preprocessing and Cleaning
- **New Data Entry**: Added "Penang Flavours", a new restaurant in Greenwich
- **Data Updating**: 
  - Identified and updated the correct BusinessTypeID for "Restaurant/Cafe/Canteen"
  - Applied this ID to the newly added restaurant
- **Data Removal**: Eliminated all establishments associated with the Dover Local Authority
- **Data Type Conversion**:
  - Transformed latitude and longitude from string to float for geospatial accuracy
  - Converted RatingValue from string to integer for numerical analysis
  - Handled null and non-standard values in the RatingValue field

### 3. Exploratory Data Analysis
The analysis focused on several key questions:

a) **Hygiene Scores**:
   - Identified 82 establishments with a hygiene score of 20
   - Analyzed the distribution of establishments with a hygiene score of 0 across different Local Authorities

b) **London Establishments**:
   - Located 66 establishments in London with a RatingValue greater than or equal to 4

c) **Top-Rated Establishments**:
   - Discovered the top 5 establishments with a RatingValue of 5, sorted by hygiene score, in proximity to "Penang Flavours"

d) **Local Authority Analysis**:
   - Ranked Local Authorities based on the number of establishments with a hygiene score of 0

## Key Findings and Insights

1. **Hygiene Standards**:
   - A significant number of establishments (82) have the highest hygiene score of 20
   - Thanet leads with 2,260 establishments having a hygiene score of 0, indicating potential areas for improvement

2. **London's Food Scene**:
   - 66 high-rated establishments (RatingValue >= 4) were identified in London, showcasing a notable presence of quality eateries

3. **Geographical Insights**:
   - The analysis revealed patterns in the distribution of hygiene scores across different Local Authorities

4. **Top Performers**:
   - Identified excellence clusters with the top 5 establishments near "Penang Flavours"

## Usage Instructions
1. **Environment Setup**:
   - Ensure MongoDB is installed and operational on your system
   - Install required Python libraries: `pip install pymongo pandas`

2. **Data Import**:
   - Use the provided JSON file to import data into MongoDB
   - Verify the successful creation of the `uk_food` database and `establishments` collection

3. **Notebook Execution**:
   - Run `NoSQL_setup_starter.ipynb` for initial data setup and preprocessing
   - Follow with `NoSQL_analysis_starter.ipynb` for in-depth analysis and insights generation

## Future Enhancements
- Implement advanced geospatial queries for location-based insights
- Develop trend analysis over time for hygiene ratings
- Create interactive data visualizations (e.g., heatmaps of hygiene scores)
- Build a web interface for public access to key findings
- Integrate with additional data sources for more comprehensive analysis

## Conclusion
This project provides valuable insights into the UK's food establishment landscape, offering a data-driven perspective on hygiene standards and geographical distribution of food businesses. The findings can be instrumental for public health initiatives, business strategies, and consumer awareness in the food industry.
