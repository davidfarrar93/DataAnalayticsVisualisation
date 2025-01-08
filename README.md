# Trends in Obesity and the Effectiveness of GLP-1 Agonists
# Data Analytics & Visualisation Final Project

## 1. Objective and Research Questions
To design and develop an interactive data visualisation and analysis dashboard to explore global and regional trends in obesity, assess the effectiveness of GLP-1 agonists, and provide predictive insights into future trends.

**Research Questions**:
- What are the global and regional trends in obesity prevalence over the last two decades?
- How effective are GLP-1 agonists in promoting weight loss and improving metabolic health compared to other interventions?
-	Can machine learning algorithms predict future obesity trends and patient outcomes with GLP-1 agonist therapy?
- How can the dashboard support healthcare professionals in decision-making and policy formulation?

## 2. Datasets
- Obesity data retrieved from WHO at https://www.who.int/data/gho/data/indicators/indicator-details/GHO/prevalence-of-obesity-among-adults-bmi--30-(age-standardized-estimate)-(-)
- WHO data exported into csv file: WHO_Obesity_Rates_Per_Country.csv
- GLP-1 inhibitor reported weight loss data retrieved from: [https://www.nature.com/articles/s41366-024-01473-y/tables/2]

### Dataset Details:
- Obesity data retireved from the WHO for all countries for the years 1990 - 2022 inclusive.
- GlP-1 inhibitor data taken from Nature displaying weight loss data for the GLP-1 pipeline.

## 3. Data Preprocessing
- Obesity data was read into a dataframe from the csv file, blank columns and columns with data not required for this review were removed. 
- GLP-1 data was web scraped using BeautifulSoup, then a dataframe was created. Multiple preprocessing steps were required to clean the data into a useable format for visualisation. The data was transposed, switching columns to rows. Columns were renamed for normal naming convention and columns containing unnecessary data were removewd. The min and max weight loss were included in the same cells, so a function clean_weight_loss was created to split the data into separate columns in the dataframe. 

## 4. Analysis & Dashboard
Visualisations were greated to view the obesity data such as:
- Cloropleth map: This was created to give a coloured representation of the variance of obesity across all countries in the world (both sexes).
- Horizontal bar chart: This was created to visualise the top 30 obesity rates by country (both sexes).
- Seaborn line plot: This was used to view obesity rates per continent (Parent Location) across the timeframe of 1990 to 2022.
- Sunburst Charts: These were created as an interactive way to visualise the obesity rates for each year, one showing obesity rates per country grouped by continent (Parent Location) and the other showing obesity rates grouped by gender (Male & Female).
- Seaborn bar chart: This was created to visualise the change in obesity levels per continent (Parent Location) from 1990 to 2022, to learn which continent showed the highest increase.
- Seaborn line plot with **linear regression model**: This chart was created using the data from 1990 to 2022, and estimates the obesity projections each year from 2023 to 2040. 

## 5. Conclusion

## 6. References
