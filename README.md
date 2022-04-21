# Kickstarting with Excel

## Overview of Project

### Purpose 
Louise's play Fever came close to its fundraising goal in a short amount of time. Louise would like a better understanding of how different campaigns fared in relation to their launch dates and funding goals in order to refine her next campaign to successfully reach its full fundraising goal. The purpose of this analysis on the KickStarter dataset will be to identify trends in the data in order for Louise to better understand what elements make a campaign successful in regard to time of year it's launched and what goal ranges have the highest success rates.

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date 

To help Louise understand if there is any correlation between when a campaign is launch and its likelihood of being successful, we need to look at historical trends based on the launch date. We had already reformatted the date to a standard format but we needed to use the Year() function to capture the launch date year in order to allow for filtering on our chart. Using a Pivot table, we grouped the KickStarter data by launch month and counted the number of campaigns by outcomes. Since Louise is interested in theater, we filtered the data by Parent Category, "theater". Building a chart off our pivot chart, we're able to create a visual that allows Louise to see how successful, failed and canceled campaigns trend over the year. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/87085239/164118679-58f414a6-ad10-4a14-87d7-e05ef3a6c62d.png)

### Analysis of Outcomes Based on Goals 

To dive further into our analysis, we next looked at the outcome of campaigns, specifically plays, based on their goal amount. The range in goal amounts for plays is large so to help break the amounts down into groups we created a summary table that grouped the goal amounts into goal groups. Using the COUNTIFS() function, we counted the number of successful, failed and canceled outcomes in the KickStarter dataset by filtering based on the goal amount grouping, the outcomes and the subcategory of "plays". Next, we used the SUM() function to total up the number of plays per goal grouping and then used the total to determine the percentage of outcome using the =ROUND('count of outcome'/total,2) for that goal grouping . Formatting the field to Percentage, we then had a percentage of outcomes by goal groupings that we could chart. Charting the results shows that smaller goals have a higher occurrence of being successful with the intercept being around 15,000 to 19,999 and failed outcomes then having a higher percentage. There does appear to be some outliers in the $35,000 to $44,999 range for successful campaigns that warrants some investigation.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/87085239/164118706-6a18d589-777f-4e88-b9dd-491869c8aa5e.png)

### Challenges and Difficulties Encountered 

We showed Louise the parent group "theaters" in the chart Theater Outcomes Based on Launch Date without breaking out the subcategory and more specifically plays. Although our client can see the overall trend of all theater campaigns, I think it could create a situation where we're not able to answer more specific  questioning on plays in general. 

In addition, for the analysis of Outcomes Based on Goal, we grouped the goal amount without taking into consideration it's currency. Converting the currencies to US dollars would have provided a better comparison on goal amounts. You can immediately tell from looking at the chart that the unusual spike in successful plays between $35,000 and $44,999 is an outlier that would warrant further investigation into the success of their campaign. It would be important to research these plays prior to meeting with Louise in order to explain the outliers.

## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?
1. The largest number of theater projects are launched May through August along with the highest number of successful outcomes. All of the months trend toward a positive success rate with December being close to 50/50 on success/failed. 

   While May through August saw its highest numbers of successful outcomes, it also saw its highest continuous trend of failed campaigns. Looking at the chart, Louise's chances of success would appear higher if launch in February, April, May, June, July or August.

2. The months of November and December have the lowest successful theater projects with December being roughly 50/50 on successful/failed. Although October has a rather high number of successful outcomes, in comparison it has a visible spike in failed campaigns. If Louise wanted to avoid the possibility of her campaign failing, she should avoid these months.

### What can you conclude about the Outcomes based on Goals?
1. Plays with a goal of "Less than 1000" and "1000 to 4999" have the highest percentage of success. Once a goal surpasses 15,000 then there's a higher degree of failing. Starting in the goal grouping of 35,000, we see some outliers that would require us to dive deeper in to understand their success story. 

   Looking at the outcomes by percentage among the goal groupings does give the appearance of more of a balanced volume of plays across the groups whereas if you look at the outcomes by count, it shows a right skewed distribution. I think showing the two charts together would provide a better visualization for Louise and understanding for what goal range has the greatest success. 

![Number of Outcomes By Goal](https://user-images.githubusercontent.com/87085239/164359433-b4d532b0-7e03-44a3-aa34-2c1f7a6d8d07.png)


### What are some limitations of this dataset?
For this challenge, we looked at the whole set of data without taking into account the different currencies. It would be helpful to have the currency converted to US dollars. 

It would be helpful to break down the KickStarters by regions, particularly in the US. It would help to see if KickerStarters in urban areas had a higher degree of success as compared to suburban or rural as well as among the different states. 

Other data elements that would help with the analysis would be how the project was spotlighted and what channels were used to advertise the KickStarters. There are some larger goal projects in the 35000 to 44999 range that standout as successful. It appears the difference in their success versus those that failed in the same goal range had a difference on whether they were spotlighted or not. The spotlighted projects had considerably more backers. A better understanding into the reason behind a KickStarter being spotlighted or not would useful. 

### What are some other possible tables and/or graphs that we could create?
Other possible tables could be looking at outcomes based on the number of days the project was open. Did KickStarters that were open longer generate more funding or was there a optimal time frame that leads to greater success? 

A chart that analyzes the affect that spotlighting could have on a successful outcome would be beneficial. 

In addition, a dataset with the names and demographics of the backers would allow a deeper dive into who is donating, are they repeat donors, their average donations and what Kickstarters they tend to donate to. 
