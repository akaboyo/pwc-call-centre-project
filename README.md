# PWC CALL CENTRE PROJECT

![Call centre logo](https://github.com/user-attachments/assets/cb64bf91-796c-4db1-8792-0c7f8daa9ceb)

## OVERVIEW

The digital revolution and our fast-changing world requires a skills revolution. And it’s not just about the digital skills. The skills revolution is about helping people build their digital awareness, emotional intelligence and creativity to fully participate in the digital future workplace — and it needs to start now.

At PwC, we are working with other organisations across the world, building on our work with clients and on upskilling our 276,000 people. Still, more must be done if we are to ensure everyone has the opportunity to learn, work and participate in the digital world. This is at the heart of our purpose.

We are enabling employees who are motivated to further accelerate their skills to do so by offering them a “career pivot” to become what we call “Digital Accelerators”. Accelerators rapidly deepen their skills in digital specialties, such as data, automation, AI, and digital storytelling by learning a variety of self-service tools and coding languages and applying these skills across our business.

## PROJECT TASK
It’s omnipresent: telecom marketing. Better price here. Better service there. Best for small businesses here. Best for young urbanites there. But what do customers really want? Our client, a big telecom company needs to know. 
Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

- Overall customer satisfaction
- Overall calls answered/abandoned
- Calls by time
- Average speed of answer
- Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

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
  
### Interactive Elements

Slicers for Agents, Months and Topics were added so that users can drill down into specific subsets of the data.

## INSIGHTS

From the call center analysis dashboard, several insights can be gathered. Here are some key observations based on the visual elements:

### Customer Satisfaction Trends
- Average Satisfaction Rate: The overall customer satisfaction rate is 3.45, which is below the target of 5. This indicates an area for improvement in customer service.
- Daily Average Satisfaction: The line chart on the top right shows that satisfaction fluctuates over time, but no clear upward or downward trend is noticeable. The performance remains consistently below the target throughout the period.

### Call Volume
- Total Number of Calls Answered: A total of 4,054 calls were answered during the analysis period. This number could be used to measure the workload and capacity of the call center.
- Monthly Breakdown: A donut chart shows that the majority of the calls were answered in January (35.89%) and February (32.02%), while March saw fewer calls. This seasonal or monthly variation could imply higher demand at the start of the year.

### Resolution Rate
- Resolved vs. Unresolved Calls: Out of the total calls, 3,646 were resolved, and 408 remained unresolved. The unresolved call rate (around 10%) indicates a need to investigate why these calls aren't getting resolved to improve service quality.
- Day of Week Performance: Calls are most frequently resolved on Tuesday and Friday, while the weekend sees fewer resolutions. This suggests that staffing or workload distribution might vary across days.

### Agent Performance
- Individual Agent Metrics: The table breaks down performance by agent, showing:
- Total Calls Answered: Agents such as Jim (536 calls) and Dan (523 calls) handled the highest number of calls.
- Resolution Rate: Despite answering fewer calls, agents like Becky and Stewart are resolving the majority of their calls, which highlights their efficiency.
- Speed of Answer: There’s some variability in how quickly agents answer calls, with Becky being the fastest at 52 seconds and Jim being the slowest at 66 seconds.
- Satisfaction: Martha and Stewart consistently receive the highest satisfaction ratings, indicating better performance in customer handling.

### Operational Bottlenecks
The average speed of answer across agents varies from 52 to 69 seconds, which shows inconsistency in how quickly customers are being attended to. Agents with higher call volumes tend to have slower response times.

## Conclusion
- Improvement Areas: Customer satisfaction is below the target, and some agents are slower to answer calls. Investigating what affects customer satisfaction and call resolution (e.g., agent training, issue complexity) could help improve these metrics.
- Agent Performance: Some agents are more efficient at resolving calls, which could be leveraged to mentor others or optimize the call center’s processes.
- Call Distribution: There’s an uneven distribution of call volumes across days and agents. A more balanced workload could improve both speed of answer and overall customer satisfaction.
