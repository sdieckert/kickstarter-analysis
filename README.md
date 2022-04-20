# Kickstarting with Excel

## Overview of Project

### Purpose 
Louise's play Fever came close to it's fundraising goal in a short amount of time. Louise would like a better understanding of how different campaigns fared in relation to their launch dates and funding goals in order to refine her next campaign to successfully reach it's full fundraising goal. The purpose of this analysis on the KickStarter dataset will be to identify trends in the data in order for Louise to better understand what elements make a campaign successful in regards to time of year it's launched and what goal ranges have the highest success rates.

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date 

To help Louise understand if there was any coorelation between when a campaign is launch and it's likelihood of being successful, we needed to look at historical trends based on the launch date. We had already reformatted the date to a standard format but we needed to use the Year() function to capture the launch date year in order to allow for filtering on our chart. Using a Pivot table, we grouped the KickStarter data by launch month and counted the number of campaigns by outcomes. Since Louise is interested in plays, we filtered the data by Parent Category, "theater". Building a chart off of our pivot chart, we're able to create a visual that allows Louise to see how successful versus failed and canceled campaigns trend over the year. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/87085239/164118679-58f414a6-ad10-4a14-87d7-e05ef3a6c62d.png)

### Analysis of Outcomes Based on Goals 

To dive further into our analysis, we next looked at the outcome of campaigns, specifically plays, based on their goal amount. The range in goal amounts for plays is large so to help break the amounts down into groups we created a summary table that grouped the goal amounts into goal brackets. Using the COUNTIFS() function, we counted the number of successful, failed and canceled outcomes in the KickStarter dataset by filtering based on the goal amount grouping, the outcomes and the subcategory of "plays". Next, we used the SUM() function to total up the number of plays per goal grouping and then used the total to determine the percentage of outcome using the =ROUND('count of outcome'/total,2). Formatting the field to Percentage, we then had a percentage of outcomes by goal groupings that we could chart. Charting the results shows that smaller goals have a higher occurance of being successful with the intercept being around !5,000 to 19,999 and failed outcomes have a higher percentage. There does appear to be some outliers in the $35,000 to $44,999 range that warrents some investigation.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/87085239/164118706-6a18d589-777f-4e88-b9dd-491869c8aa5e.png)



### Challenges and Difficulties Encountered 

For this analysis, we provided Louise with a chart displaying theaters to then go on and filter for plays. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. The largest number of theater projects are launched in May along with the highest number of successful outcomes. Projects with a launch date in the summer months of May - August have the highest number of successful outcomes with a steady decrease from May to September. 
2. The months of November and December have the lowest successful theater projects with December being roughly 50/50 on sucessful/failed.

- What can you conclude about the Outcomes based on Goals?
1. Plays with a goal of "Less than 1000" and "1000 to 4999" have the highest percentage of success. Once a goal surpasses 15,000 then there's a higher degree of failing. 

- What are some limitations of this dataset?
For this challenge, we looked at the whole set of data rather than limiting it to the US. Filter for just US for the Outcomes Based on Goals, you'll see a slightly higher percentage successful and lower percentage failed in the 10000 to 4999 range than the whole set of data. 

It would be helpful to break down the Kickstarters by regions, particularly in the US. It would help to see if Kickerstarters in urban areas had a higher degree of success verses less urban areas.  

Other data elements that would help wtih the analysis would be how the project was spotlighted and what channels were used to advertise the Kickstarters. In addition, a dataset with the names and demographics of the backers would allow a deeper dive into who is donating, are they repeat donors, their average donations and what Kickstarters they tend to donate to. 

- What are some other possible tables and/or graphs that we could create?
Other possible tables could be looking at outcomes based on the number of days the project was open. Did KickStarters that were open longer overall generate more funding? In addition, analyzing the affect that spotlighting could have on a successful outcome. There are some larger goal projects in the 35000 to 44999 range that standout as successful. It appears the difference in their success versus those that failed in the same goal range could depend on whether they were spotlighted or not. The spotlighted projects had considerably more backers. Also, an better understanding into the reason behind a KickStarter being spotlighted or not would useful. 
