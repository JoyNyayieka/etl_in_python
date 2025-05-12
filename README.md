# Health Data ETL and EDA Project

This project demonstrates how to integrate PostgreSQL with Python using SQLAlchemy and Pandas for performing data analysis and transformation. The project focused on processing a dataset containing individuals' height, weight, and year of birth to derive new insights such as BMI, BMI category, and age.

## Tools Used

- **PostgreSQL** for data storage
- **SQLAlchemy** for database connectivity
- **Pandas** for data manipulation and analysis
- **Python** for scripting the entire workflow

## Workflow Summary

1. **Data Source**: A CSV file containing `Height`, `Weight`, and `Born_Year` was loaded into a Pandas DataFrame.

2. **ETL Process**:
   - **Extract**: The CSV data was read into memory.
   - **Transform**:
     - BMI was calculated using the formula: *weight (kg) / (height (m))²*
     - BMI Category was assigned based on standard ranges (Underweight, Normal, Overweight, Obese).
     - Age was calculated as the difference between the current year and `Born_Year`.
   - **Load**: The cleaned and enriched dataset was written to a PostgreSQL database table.

3. **Exploratory Data Analysis**:
   - Basic statistics and summaries were generated to understand the distribution of BMI and age.
   - Grouping and aggregation provided insights into trends across BMI categories.

## Database Integration

The transformed data was written back to PostgreSQL using SQLAlchemy. This ensures it can be queried and reused for further analysis or integration into applications.

## How to Run

1. Install required packages:

    ```bash
    pip install pandas sqlalchemy psycopg2
    ```

2. Update your database connection string and run the ETL script.

## Outcome

This pipeline shows how basic demographic data can be transformed into useful health metrics, stored reliably, and analyzed efficiently with Python and SQL.
