# Kickstarting with Excel
- [Kickstarter_Challenge_Workbook](path/to/Kickstarter_Challenge.xlxs)
---
## Overview of Project
- The goal of this project is to assist Louise with her project campaign specifically around theater treands. Using Excel, we are performing an analysis on the Kickstarter and manipulating the data to make it more readable and uncover any trends on previous projects in order to support Louise in her new campaign. 
### Purpose
- Louise’s play Fever came close to its fundraising goal in a short amount of time. She wants to know how different campaigns fared in relation to their launch dates and their funding goals. Using the Kickstarter dataset that we practiced in the modules, we will use this assignment to visualize campaign outcomes based on their launch dates and funding goals.
- Within this exercise, I learned how to:
  - convert Unix Timestamps into month/day/year format
  - use Pivot Tables to condense and focus on specific data points 
  - create Pivot Charts to provide a visual summary of outcomes
  - apply Statistical Formulas to identify outliers and/or determine deviations (sum, percentage, mean, median)
  - use V/HLookup and IFStatement formulas to use data from one worksheet to another based on specific metrics
---
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
How Time Will Determine the Outcome?
... let's visualize campaign outcomes of theaters ("successful," "failed," and "canceled") based on launch date
![Outcomes_Based_on_Launch_Date_Chart](path/to/image_name.png)
- Campaigns launched in the Spring were more successful than those launched in the Winter. This means that the best time to start the campaign would be in May/June. In the chart below, we see that there were more than 100 campaigns in May and June that were successfully funded compared to less than 60 in November and less than 40 in December. We can only assume that people are less likely to support a campaign due to the Winter holiday season.
### Analysis of Outcomes Based on Goals
Does Setting a Reasonable Goal Make a Difference?
... let's visualize the percentage of successful, failed, and canceled plays based on the funding goal amount
![Outcomes_Based_on_Goals_Chart](path/to/image_name.png)
- Campaigns with goals less than $5000 saw an average of 74% =AVERAGE(76%,74%) success rate compared to the other ranges with an average of $5602 funded vs the average goal of $5049. The average pledged amount were 10% =(5602-5049)/5602 better than the goal. When you analyze why campaigns failed, the results showed that the average goal for failed campaigns was greater than $10554 with only an average of $559 funded. This would mean that the higher the goal, the less likely it would succeed due to campaign length of time and number of backers that would be needed.
### Challenges and Difficulties Encountered
In the module, I learned how to fill any missing components such as... the Percent Funded =ROUND(E2/D2*100,0), Average Donation (replacing errors with a zero) =IFERROR(ROUND(E2/L2,2),0).
  - Unix timestamp formula returned values, but the format did not appear as mm/dd/yyyy. Used the "date" format function in order to convert to the correct format... convert the Unix Timestamp for the launch and deadline date =(((J2/60)/60)/24)+DATE(1970,1,1)
  - When pivoting this data, I couldn't break down the date field by month in order to display the "month" only. So I had to use =TEXT(S2,"mmmm") to parse out the month from the results after the Unix Timestamp was converted.
---
## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Drawing conclusions from the line graph, the best time with highest success rates to launch a theater campaign would be in May and/or June. 
  - In contrary, it would not be recommended to have campaigns in the Winter months, from November-January. This might be because of the holiday season during the winter break.
### What can you conclude about the Outcomes based on Goals? 
- From the line graph, we can draw some conclusions that campaigns with more reasonable goals are more likely to be successful. Particularly campaigns with an average goal of less than $5000 were very successful. Whereas campaigns with average goals of greater than $15000 have a much higher failure rate, with the exception around the $35000 to $45000 range. 
### What are some limitations of this dataset?
Some of the limitations:
- Distinguishing by social measures such as gender and age. This would allow more data breakdown based on a target audience.
- Differentiate why some campaigns failed and others succeed... is it influenced by the length of time, launch date or maybe unreasonable goals?
- Was there a marketing tool used and what method to advertise the campaign was more successful?
### What are some other possible tables and/or graphs that we could create?
- We could compare theather outcomes in different countries
