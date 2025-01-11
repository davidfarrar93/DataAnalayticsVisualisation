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
- Obesity data retrieved from WHO (WHO, 2024)
- WHO data exported into csv file: WHO_Obesity_Rates_Per_Country.csv
- GLP-1 inhibitor reported weight loss data retrieved from Nature (Parker et al., 2024)

### Dataset Details:
- Obesity data retireved from the WHO for all countries for the years 1990 - 2022 inclusive.
- GlP-1 inhibitor data taken from Nature displaying weight loss data for the GLP-1 pipeline.

## 3. Data Preprocessing
- Obesity data was read into a dataframe from the csv file, blank columns and columns with data not required for this review were removed. 
- GLP-1 data was web scraped using BeautifulSoup, then a dataframe was created. Multiple preprocessing steps were required to clean the data into a useable format for visualisation. The data was transposed, switching columns to rows. Columns were renamed for normal naming convention and columns containing unnecessary data were removewd. The min and max weight loss were included in the same cells, so a function clean_weight_loss was created to split the data into separate columns in the dataframe. 

## 4. Analysis & Dashboard
Visualisations were greated to view the obesity & GLP1 data such as:
- Cloropleth map: This was created to give a coloured representation of the variance of obesity across all countries in the world (both sexes).
- Horizontal bar chart: This was created to visualise the top 30 obesity rates by country (both sexes).
- Seaborn line plot: This was used to view obesity rates per continent (Parent Location) across the timeframe of 1990 to 2022.
- Sunburst Charts: These were created as an interactive way to visualise the obesity rates for each year, one showing obesity rates per country grouped by continent (Parent Location) and the other showing obesity rates grouped by gender (Male & Female).
- Seaborn bar chart: This was created to visualise the change in obesity levels per continent (Parent Location) from 1990 to 2022, to learn which continent showed the highest increase.
- Seaborn line plot with **linear regression model**: This chart was created using the data from 1990 to 2022, and estimates the obesity projections each year from 2023 to 2040.
- The reported weight loss and proportion of people who achieved weight loss of ≥5%, ≥10%, ≥15% and 20% are represented graphically to evaluate different GLP-1 inhibitors.
- Taking the current approximate number of people on GLP-1 inhibitors as 837,000 (IQVIA, 2004) and the projected number of patients at 40 million (UBS, 2024), the projected number of patients by 2040 was determined by **linear regression**.
- Taking the mean weight loss reported across all GLP-1 inhibitors (10.318182), the potential imppact of GLP-1 updake to the projected obesity rates to 2040 was reviewed.

## 5. Conclusion
- Comprehensive analysis combining data from different sources to understand global obesity trends, effectiveness of GLP-1 inhibitors and how they relate to each other.
- The projected obesity rates per continent were achieved through linear regression.
- The linear models created for GLP-1 inhibitors indicated that they would likely have a negligable impact on the global obesity trend (~0.13%).
- The projected number of patients for GLP-1 inhibitors is projected to exceed 100 million by 2040.

## 6. References
World Health Organization (WHO), 2024. Prevalence of obesity among adults (BMI ≥ 30) (age-standardized estimate). [online] Available at: https://www.who.int/data/gho/data/indicators/indicator-details/GHO/prevalence-of-obesity-among-adults-bmi--30-(age-standardized-estimate)-(-) [Accessed 11 January 2025].

Parker, R., Patel, A. and Williams, S., 2024. GLP-1 receptor agonists in obesity management: Implications for treatment strategies. Nature Reviews Endocrinology, [online] 20(3), pp.147-159. Available at: https://www.nature.com/articles/s41366-024-01473-y [Accessed 11 January 2025]

IQVIA. (2024). Obesity treatment rates increase as GLP-1 inhibitors prosper. [pdf] IQVIA. Available at: https://www.iqvia.com/-/media/iqvia/pdfs/library/white-papers/obesity-treatment-rates-increase-as-glp-1-inhibitors-prosper.pdf [Accessed 9 January 2025]

UBS. (2024). GLP-1 medication: A game changer in the treatment of obesity and diabetes. [online] UBS. Available at: https://www.ubs.com/global/en/investment-bank/insights-and-data/2024/glp-1-a-medication.html [Accessed 8 January 2025].
