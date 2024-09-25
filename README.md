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


















![Call-Centre-snippet](https://github.com/user-attachments/assets/fbc0c14d-5bb3-45fc-997f-f5842203df00)
