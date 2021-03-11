# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends

Kickstarter Analysis


Overview

In this project we are using the data in Kickstarter_Challenge to analyze different campaign outcomes. We want to know the outcomes of campaigns based on their launch date and their funding goals. Campaigns are categorized as either successful, failed, or canceled and we want to know if the date in which the campaign was launched has any effect on the outcome. We also want to know if the amount spent on the campaign, or the funding goal, has any effect on the outcome of the campaign. We will look at this information by calculating the percentage of successful, failed, and canceled plays based on the funding goal amount.


Purpose

The purpose of this analysis is to help determine if there is a relationship between the data and the campaign outcome. The launch date of a campaign and its relationship to the campaign’s success is one of the relationships we are interested in. The campaign goal amount and its success is another relationship we are going to look at. These two relationships will help us to determine if there are any variables that effect the success of a campaign.


Analysis and Challenges

Analysis of Outcomes Based on Launch Date:

To start the analysis, three columns had to be added to the Kickstarter worksheet. The first and second columns added were “Date Created Conversion” and “Date Ended Conversion” so that the dates were easier to manipulate and see. The formula used for the “Date Created Conversion” was (((launched_at column/60)/60)/24) + DATE(1970,1,1).The formula used for the “Date Ended Conversion” was (((deadline column/60)/60)/24) + DATE(1970,1,1). The third column added was “Years” where the year of the “Date Created Conversion” was displayed by using the YEAR()function. These three new columns will be helpful later on in the analysis.

Pivot Table:

To be able to look at this data more easily, a pivot table was created. The pivot table was created with rows as the months in descending order and the columns as the number of successful, failed, and canceled campaigns. At the bottom of rows and at the end of the columns were each a grand total. Filters were put on parent category to display only theater campaigns and a filter was put on years to include all years. Therefore, we can see the number of successful, failed, and canceled campaigns per month.


Line Chart:

To visualize the data a line chart was created. The line chart “Theater Outcomes by Launch Date” has months on the x-axis and count of outcomes on the y-axis. Each line on the chart is represented by a color corresponding to a specific campaign outcome. The number of canceled campaigns is almost the same amount for every month whereas the number of failed and successful campaigns vary. The number of failed campaigns does not fluctuate too much and stays around forty per month. The number of successful campaigns fluctuates a great deal more than the other outcomes. The months with more success seem to be May through June and the months with the least success seem to be November and December. Overall, there are more successful campaigns with a launch date during the summer months.


Analysis of Outcomes Based on Goals:

A new sheet was created and named “Outcomes Based on Goals” with twelve rows and eight columns. The columns were labeled “Goal”, “Number Successful”, “Number Failed”, “Number Canceled”, “Total Projects”, “Percentage Successful”, “Percentage Failed”, and “Percentage Canceled”. The Rows were goal ranges “less than 1000”, “1000-4999”, “5000-9999”, “10000-14999”, “15000-19999”, “20000-24999”, “25000-29999”, ”30000-34999”, “35000-39999”, “40000-44999”, “45000-49999”, and “Greater than 50000”. To calculate the “Number Successful”, “Number Failed”, and “Number Canceled” columns we used the COUNTIFS() function with columns based on “outcome”, “goal”, and “plays” for each goal range. To calculate the “Total projects” column for each goal range the SUM() function was used to sum the number successful, failed, and canceled. For the “Percentage Successful” column the “Number Successful” was divided by the “Total Projects” for each goal range. The “Percentage Failed” and “Percentage Canceled” columns were calculated in the same way as the “Percentage Successful”. 

https://github.com/skylarblack96/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png
 
Line Chart:

To visualize the information in the “Outcomes Based on Goals” sheet we created a line chart. On the x-axis is the goal ranges and on the y-axis is the percentage. The outcomes are categorized by color. There were no canceled campaigns for any of the plays. The most successful play campaigns seem to have goals less than $5000 and the goals that had the least success were $25000 - $29999 and $45000 - $44999. 

Challenges and Difficulties:

Some difficulties or challenges were harder than others, but they were mostly solved fairly quickly. The most difficult challenge was creating the line charts and making sure the axis displayed what they were supposed to display. It might have been more difficult because of the version of Excel or using a Mac in comparison to a different laptop. Most of these difficulties could be eliminated by becoming better acquainted to Excel.




Results

Outcomes based on Launch Date Conclusions:

Based on the data from the “Outcomes Based on Launch Date”, campaigns that launched during the months of May and June had more success.
Campaigns that launched in the month of December have the least amount of success with almost the same number of successful outcomes as failed outcomes.



Outcomes Based on Goals Conclusion:

Campaigns with goals less than $1000 and goals between $1000 and $4999 were the most successful. Therefore, this analysis shows that campaigns that spend less than $5000.00 should have the most success.

Dataset Limitations:

There are so many different variables it is hard to see if one specific variable had all the influence or which variables had no influence at all. Also, it is difficult to see if the combination of certain variables would have a certain effect on the outcome of a campaign. We cannot determine if the outcome based on goals or the outcome based on launch date have all the influence on the success of a campaign.

Extra Tables or Graphs:

There are many other tables and graphs we could create to see if there are any other factors that influence the success of a campaign. The outcome based on average donation to see if the higher the donation the more successful the campaign. The outcome based on length of campaign, if the campaign is longer is the outcome more successful. The outcome based on years, was there a certain year that did not do as well or a year that did better than the rest. The outcome based on the number of backers, if the campaign had more backers was it more successful. The outcome based on the country, was there a country where the campaign did particularly well or one that did not do well. The outcome based on the pledge amount. If the pledge amount was lower or higher than the goal, how did the campaign fare. 

