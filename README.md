
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
1. Inquiry Information
   
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
**1.	Inquiry Volume Over Time: Identify any trends in the number of inquiries over time (e.g., weekly or monthly trends)**

Computed number of inquiries made  
```No of Inquiries = COUNTROWS('Inquiry Information')```   

Calculated total number of days for inquiry information collection  
```Total No. of Days = DATEDIFF(MIN('Inquiry Information'[Date]), MAX('Inquiry Information'[Date]), DAY)```  

Created calculated column DayOfWeek to find number of inquiries made in a day of a week  
```DayOfWeek = FORMAT([Date], "dddd")```   

Created calculated column InquiryMonth  to find number of inquiries made in a month  
```InquiryMonth = FORMAT('Inquiry Information'[Date], "YYYY-MM")```    

Created calculated column InquiryHour to find number of inquiries made in a hour    
```InquiryHour = HOUR([Time])```    



**2. Age Analysis: Determine which age groups are most interested in our courses**  
a) Created a calculated column Age category to categorize age of children inquired to different categories   
![image](https://github.com/user-attachments/assets/3b320779-739e-4c26-a45c-1cda7fbeb046)    

b) Created Stacked Column Chart: Age Categories vs. Number of Inquiries by Course    
The stacked column chart provides a visual representation of the number of inquiries made for different courses across various age categories. This chart is useful for understanding which age groups are most interested in specific courses, helping to tailor marketing efforts and course content to target the right audience.     
![image](https://github.com/user-attachments/assets/2be6eb62-5e12-4f5a-ac07-1ae8e2a036e2)  



**3.	Course Popularity: Analyze which courses are most in demand and if there's a correlation between the age of the kid and the course chosen.**  
a) Created Stacked Column Chart: Interested Course vs. Number of Inquiries by Age Category    
The stacked column chart visualizes the relationship between the courses of interest and the number of inquiries across different age categories. This chart is effective for identifying which courses are most popular among various age groups, providing insights into age-specific preferences and guiding targeted marketing and curriculum development strategies.  
![image](https://github.com/user-attachments/assets/6050f66c-c3bc-4822-b597-6f6e4e527a44)   


**4. Inquiry Status Analysis: Examine the status of inquiries to understand how many have led to enrollment, and identify any common reasons for not enrolling (e.g., fee is high, not interested).**
Conditions and Corresponding Categories:  
Interested: If the status is "Enrolled", the response category is set to "Interested".  
Not Interested: If the status is "Not Interested", "Demo Given. Not interested", "Fee is High", or "Different course Enquiry", the response category is set to "Not Interested".
No Response: If the status is "No response", the response category is set to "No Response".
Other: If the status is "Marketing spam inquiry" or "Marketing inquiry", the response category is set to "Other".
 A new calculated column named Response Category created based on the status of inquiries in the 'Inquiry Information'[Status]

![image](https://github.com/user-attachments/assets/e43e177d-ee2a-4b28-bb47-d41643a2972e)


### Insights
**Total Inquiries:**
The data collected shows a total of 74 inquiries over a period of 141 days. This gives an average of approximately 0.52 inquiries per day.  
  
**Weekly Inquiry Trends:**  
Wednesday has shown the highest number of inquiries, indicating it’s the most active day of the week for inquiries.  
Sunday follows as the second highest, with Saturday and Monday also showing significant activity.  


**Monthly Inquiry Trends:**  
July exhibited the highest number of inquiries, suggesting it is the peak month for inquiry activity.  
May and June also show high inquiry volumes but are less than July.  


**Daily Inquiry Trends:**  
The peak hour for inquiries is 2 PM, suggesting that this time is optimal for receiving inquiries.
6 PM and 8 PM are also notable, indicating that late afternoon and early evening are busy times for inquiries.


**Age Analysis**   
The age groups 11-13 and 13-15 years had the most inquiries, with Python being particularly popular in these age groups followed by Robotics  


**Age Category Trends:**  
The 11-13 years age category consistently shows the highest interest  for Python, Robotics, and Web Development courses.  
The 13-15 years age category is also notably active, particularly in Python, Robotics and Web Development courses.  
Interest in courses declines in the age groups outside 11-15 years, with fewer inquiries in the 7-9 years and 5-7 years categories.  


**Higher Interest from Novices:**  
Individuals with no previous coding experience show greater interest in Python and Robotics courses compared to those with prior coding experience.   


**High No-Response Rate (41 inquiries):**  
A significant number of inquiries resulted in no response.   


**High Fees (16 inquiries):**  
Concerns about the fees are a notable barrier for 16 individuals.  


**General Lack of Interest (7 inquiries):**  
A small number of inquiries were marked as “not interested.”    


### Recommendations for Improving Enrollment  

**Enhance Follow-Up and Engagement**  
Structured Follow-Up: Implement a structured follow-up process to address the high no-response rate. This could include automated emails, phone calls, or personalized messages to re-engage potential students.  
Timely Response: Ensure prompt responses to inquiries, especially during peak hours like 2 PM, 6 PM, and 8 PM when inquiries are most frequent.  

**Optimize Communication Channels**  
Preferred Contact Times: Schedule follow-ups and communications around peak inquiry times. For example, sending emails or making calls in the late afternoon and early evening could improve engagement.  
Multichannel Approach: Use multiple channels (email, phone, social media) to reach out to prospects, catering to their preferred communication method.  


**Address Fee Concerns**  
Flexible Payment Options: Introduce flexible payment plans, discounts, or scholarships to make the courses more accessible and address concerns about high fees.  
Value Proposition: Clearly communicate the value and benefits of the courses to justify the fees. Highlight unique features, outcomes, and success stories.  



**Leverage Peak Inquiry Times**  
Special Offers: Consider offering limited-time promotions or discounts during peak inquiry periods (e.g., Wednesdays and Sundays) to capitalize on higher engagement.  
Enhanced Outreach: Increase marketing and outreach efforts around peak times to maximize the number of inquiries and conversions.  



**Tailor Courses to High-Interest Age Groups**  
Customized Content: Develop and promote content specifically targeted at the 11-13 years and 13-15 years age groups, as they show the highest interest in Python, Robotics, and Web Development.  
Engaging Workshops: Create engaging and age-appropriate workshops or introductory sessions to attract these age groups and increase enrollment.  


**Cater to Beginners**  
Beginner-Friendly Materials: Provide resources and introductory content tailored for individuals with no prior coding experience. Highlight the ease of getting started with Python and Robotics.  
Supportive Environment: Offer support and mentoring for beginners to help them feel more comfortable and confident in their learning journey.  



**Address Lack of Interest**  
Gather Feedback: Reach out to those marked as “not interested” to understand their reasons. Use this feedback to refine course offerings and improve engagement strategies.  
Targeted Messaging: Develop targeted messaging and campaigns that address the specific needs or concerns of potential students who initially showed a lack of interest.  



**Improve Course Presentation**  
Demo Optimization: Enhance the quality and appeal of course demos to increase interest. Ensure that demos clearly showcase the course benefits and value.  
Engaging Content: Develop engaging and interactive content for demos and promotional materials to capture and retain interest.  

Check dashboard here: https://mavenanalytics.io/project/18947
