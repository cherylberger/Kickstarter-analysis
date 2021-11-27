# **An Analysis of Kickstarter Campaigns for Louise**
## **Overview**
The purpose of the analysis was to provide Louise with more information on how to manage her fundraising campaign for the play Fever.  She has come close to reaching her goal in a short amount of time.  We can use information from ‘Kickstarter’, a global dataset detailing the outcomes of various fundraising campaigns from 2009 to 2017, to analyze outcomes of previous campaigns.  These data will be used to visualize the success of campaigns in relation to their launch dates during the calendar year and determine if there are any relationships between the outcome and fundraising goals.  
## **Analysis and Challenges**
###  **Analysis of Theater Campaign Outcomes Based on Launch Date**
####   *Add a new column for the Year & populate the table using Date function*
To better understand the outcome of various campaigns by launch date, we will analyze the data for trends in campaign outcomes over time.  First, the original dataset was copied and the new file was saved as ‘Kickstarter_Challenge.xlsx’.  Using the Kickstarter dataset, add a header row titled “Years” to a blank column (Column U).  Calculate the year the campaign launched from the ‘Date Created Conversion’ column (Column S) using the Year function ‘YEAR ()’ in Excel. Set the formula for cells U2 as follows = YEAR(S2) and paste this formula to all rows in the dataset as Illustrated in Figure 1. The year of launch is displayed in the column for each campaign.  
![image](https://user-images.githubusercontent.com/94234511/143689480-a15ec807-2162-455b-a344-bad3fba1df4b.png)
####   *Create a Pivot Table in a new worksheet ‘Theater Outcomes by Launch Date’* 
