# Kickstarting with Excel

## Overview of Project

Louise has requested an analysis of previous Kickstarter campaigns and how their outcomes may have been affected by the funding goal amount and the launch date. In this project Kickstarter data has been analyzed allowing us to filter only campaigns related to funding theater/plays, the pertinent area of the client's interest, and charts created to visualize campaign outcomes based on their initial goal and also on their launch date.

### Purpose

The purpose of this project is to be able to make educated assertions about what factors contribute to successful Kickstarter campaigns in the relevant category for possible future campaigns.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

The first step to analyzing Kickstarter campaign outcomes based on launch date was to create a Pivot Table which filtered the campaign categories and the date launched and then broke down the possible outcomes (successful, failed, or canceled) by the month the campaign was launched. This information is represented in the following chart:
![image](https://user-images.githubusercontent.com/94754972/147420353-5f23719e-22dc-40c1-a456-aa71d049fa1b.png)

### Analysis of Outcomes Based on Goals

In order to analyze the Kickstarter campaign outcomes based on fundraising goal a seperate spreadsheet was created and using the COUNTIFS() function data was imported from the original data set, breaking down each outcome into goal brackets from "Less than 1000" to "Greater than 50000". This data was then used to calculate the percentage of projects with each outcome within each bracket. The final percentage data was then used to create the following chart: 

![image](https://user-images.githubusercontent.com/94754972/147420481-73c0aa95-c8e0-4d90-9f1f-ddb5dbc91ffb.png)

### Challenges and Difficulties Encountered

One technical challenge came from having several brackets where no campaigns had goals which led to calculation errors when converting the results into percentages. This was solved by nesting the ROUND() function within the IFERROR() function, substituting those errors with zeroes. From an analysis one challenge is the sample size, especially in the Outcomes Vs Goals portion. Looking at the chart, for example, we can say that 100% of Kickstarter campaigns in the play category with fundraising goals of 35000 to 39999 failed however looking at the data we can see that is based on a single failed campaign. 

## Results

From the Outcomes Based on Launch Date analysis we can conclude that campaigns launched mid-year, specifically May-June, tend to be vastly successful compared to the rest of the year and we can also conclude that campaigns launched in the winter, specifically December-January, have a lower rate of success. From the Outcomes Based on Goals data we can conclude that the higher the fundraising goal, the greater risk there is of a campaign failure. These conclusions need to taken in context with the data limitations however, within the Outcome vs Goal data there are only campaigns total with goals over 15000 so any percentages calculated in those brackets are based on very little data. There is also a limitation with the Launch Date data. It is clear in the visual that more campaigns are successful in the late spring/early summer but the toal number of campaigns launched during that time is also higher. For example there are more successfull campaigns in the month of May than there are total campaigns in December. A possibility for further future analysis would be to create a chart representing the Launch Date data but rather than the number of campaigns with each outcome we could show the percentage.
