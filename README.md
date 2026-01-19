# PWC CALL CENTRE PROJECT

![Call centre logo](https://github.com/user-attachments/assets/cb64bf91-796c-4db1-8792-0c7f8daa9ceb)


## OVERVIEW

This project was developed as part of the **PwC Switzerland Data Analytics Virtual Case Experience**. The goal was to create an interactive **call centre dashboard in Power BI** that visualises key performance indicators (KPIs) and uncovers insights to support operational decisions for a telecom client.

## PROJECT TASK
Create a Power BI dashboard that reflects the following call centre metrics:

- Overall customer satisfaction  
- Total calls answered vs abandoned  
- Call volumes by time and date  
- Average speed of answer  
- Agent performance (e.g., average handle time vs calls answered) 

## Datasource :

The dataset used for this task was provided by [Pwc](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) :

Dataset: 
[01 Call-Center-Dataset.xlsx](https://github.com/user-attachments/files/17128509/01.Call-Center-Dataset.xlsx)

## Data Preparation:

- Datatypes: Date, Time and AvgTalkDuration fields were formatted to reflect the proper data types in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.
- Missing Values: 946 missing values were removed from the dataset so as not to skew the analysis report, leaving 4054 clean data points for analysis.
- Data Validation: Each of the columns in the table were validated to have the correct data type

## Data Modeling:

- A date dimension table was created using DAX codes and marked as Date Table for the analysis
- I created a one-to-many relationship between the Dataset table (Sheet1) and the DateDimension table.

![ERD1](https://github.com/user-attachments/assets/714967e9-b6fa-470a-a58a-afd52e8155dc)

## Data Analysis:

The following DAX measures were created for this analysis :

- MaxSatisfactionRating = MAX(Sheet1[Satisfaction rating])
- SatisfactionRating Target = 4.5
- Total Calls Answered = CALCULATE(COUNTROWS('Sheet1'),'Sheet1'[Answered (Y/N)] = "Y")
- Total Calls Resolved = CALCULATE(COUNTROWS('Sheet1'),'Sheet1'[Resolved] = "Y")
- Total Calls Unresolved = CALCULATE(COUNTROWS('Sheet1'),'Sheet1'[Resolved] = "N")

## Data Visualization (Dashboard) 

Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:

![Call-Centre-snippet](https://github.com/user-attachments/assets/fbc0c14d-5bb3-45fc-997f-f5842203df00)

### Key Metrics
- KPI card: This shows an Average Customer Satisfaction Rate of 3.45
- Total calls answered = 4054
- Total calls resolved = 3646
- Total calls unresolved = 408
- Interactive Slicers for Agents, Months and Topics filters for drilling down into specific subsets of the data.

## INSIGHTS
The Power BI visuals reveal the following:

- **Customer Satisfaction:** Average rating ~3.45, below target, pointing to service experience gaps.  
- **Volume Trends:** Most calls were answered in January and February; March saw lower demand.  
- **Resolution Rates:** Approximately 90% of answered calls were resolved, indicating solid issue handling.  
- **Agent Performance:** Some agents resolve more calls but take longer to answer, others answer quickly with variable outcomes.  
- **Speed of Answer:** Variability across agents suggests opportunities for training or process improvements. 

## Conclusion/Recommendations
Use visual trends and metrics to:

- Investigate drivers of lower satisfaction (e.g., slow response, specific topics).
- Tailor agent support and coaching based on performance patterns.
- Align staffing with peak periods to reduce wait times.

View dashboard [here](https://app.powerbi.com/view?r=eyJrIjoiZDBiYjgwMTgtM2NlZi00ZmY5LWFlYzAtMmYyNzYyMTI3MTE5IiwidCI6ImFlNmFhZDgzLWRmNmYtNDkwZi1iMTU5LWNhZDVjNjUyYjhmMCJ9)
