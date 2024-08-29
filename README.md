
<h1 align="center">Enhancing Student Enrollment: A Data-Driven Strategy for Optimizing Course Inquiries and Conversions</h1>


### Introduction 
In the ever-evolving landscape of education, institutions and training centers must leverage data to optimize their outreach and enrollment strategies. This project, titled "Enhancing Student Enrollment Using Power BI," aims to utilize data analysis to improve student enrollment rates by understanding patterns in inquiries and identifying key factors that influence conversion.

Through this project, we have analyzed a dataset containing 74 inquiries over a period of 141 days, focusing on various aspects such as weekly, monthly, and daily trends, age group preferences, course popularity, and the impact of prior coding experience on course interest. By leveraging Power BI, we have visualized these insights to create a comprehensive understanding of the data, enabling us to develop targeted strategies to enhance student engagement and increase enrollment.

The findings from this analysis will provide actionable recommendations for improving follow-up processes, optimizing communication channels, addressing concerns about fees, tailoring course content to specific age groups, and enhancing overall course presentation. By applying these strategies, educational institutions can better meet the needs of prospective students and boost their enrollment rates.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Project Overview  
**"Enhancing Student Enrollment Using Power BI"** is a data analysis project aimed at improving student enrollment rates by leveraging data-driven insights to optimize inquiry handling and conversion strategies. The primary focus of this project is to analyze patterns in course inquiries and identify key factors that can influence the decision-making process of potential students.  

**Key Objectives:**

- Analyze Inquiry Data: Examine a dataset of 74 inquiries collected over 141 days to identify trends in student interest based on various parameters such as day of the week, time of day, month, age group, and course type.  

- Identify Inquiry Trends: Use Power BI to visualize data trends and understand which days and times receive the most inquiries, which age groups are most interested in specific courses, and how previous coding experience affects course preferences.  

- Address Barriers to Enrollment: Investigate reasons for non-conversion such as high fees, lack of interest post-demo, and non-responsiveness to inquiries. Identify actionable insights to reduce these barriers.  

- Develop Targeted Strategies: Create data-driven recommendations to improve follow-up processes, optimize communication, adjust course offerings to meet the needs of different age groups, and address concerns related to course fees and interest.  

- Enhance Engagement and Conversion: Implement strategies to increase student engagement and conversion rates by targeting the right audiences with the appropriate messaging and course offerings.

**Approach:**

- Data Collection and Analysis: Collected data from inquiry logs was analyzed to identify patterns in student interest and behaviors. Key metrics such as inquiry volume by day, time, age group, and course type were evaluated using Power BI.

- Visualization and Insight Generation: Power BI was used to create interactive dashboards and visualizations to better understand the data trends and identify areas for improvement.

- Strategy Development: Based on the insights gained from the data analysis, tailored strategies were developed to enhance follow-up, engagement, and conversion processes.

**Expected Outcomes:**

By understanding the factors that influence student inquiries and leveraging targeted strategies, educational institutions can improve their enrollment rates, effectively engage prospective students, and optimize their course offerings to meet the needs of their audience. This project aims to provide a framework for data-driven decision-making that can be applied to enhance student enrollment and satisfaction.



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Data Sources
The dataset contains 1 excel file:
1. Inquiry Information.excel
   
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Tools
- PowerBI -Data Cleaning, Data Visualization and creating dashboards

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Data Cleaning/Preparation
For this project, a thorough data cleaning process was undertaken to ensure the dataset was accurate, consistent, and ready for analysis. The following steps were carried out:  

**Splitting Timestamp:**  

- The original timestamp data was split into two separate columns: Date and Time. This allowed for more granular analysis of inquiry trends by day and time.  

**Name Formatting:**  

- The Name column was standardized by capitalizing the first letter of each name. Additionally, only the name before the comma was retained to simplify the data and focus on the primary identifier.  

**Standardizing the "Number of Children" Column:**  

- The "Number of Children" column was renamed to "Count of Children Enrolled" for clarity.  
- All instances of the word "One" were replaced with the numeral "1" for consistency.  
- Entries labeled "Online coding live interaction" were replaced with "0" to indicate no children were enrolled.  
- Null values were replaced with "0" to avoid missing data issues during analysis.  
- Responses such as "2 or 1 maybe depends" were standardized to "1" to simplify categorization.  

**Age Data Standardization:**    

-  Inconsistent age entries were standardized  
- "13 years" was replaced with "13".  
- "Age 12" and "9" were both replaced with "12" to correct any errors.  
- "12yrs" was also replaced with "12".  
- The entry "Adam" was corrected to "6" based on contextual understanding.   

**Course Interest Data Standardization:**

- Ambiguous or detailed course descriptions were simplified to align with primary course categories:  
- "Whatever appropriate for this age group" was replaced with "Python".  
- Descriptive phrases like "Interested for my kids for coding, Java python c++ scratch web development IoT stem robotics artificial intelligence coding etc" were shortened to "Java".  
- Multi-course requests such as "Web development and Robotics and Python Please" were categorized under the first mentioned course, "Web development".  
- Similarly, "Python and Robotics" was standardized to "Python".  
- These data cleaning steps helped ensure the dataset was consistent, accurate, and ready for comprehensive analysis using Power BI. This process also allowed for more reliable insights and actionable recommendations to be derived from the data.  


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### DASHBOARD
