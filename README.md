# **An Analysis of Kickstarter Campaigns for Louise**

## **Overview**
The purpose of the analysis was to provide Louise with more information on how to manage her fundraising campaign for the play Fever.  She has come close to reaching her goal in a short amount of time.  We can use information from ‘Kickstarter’, a global dataset detailing the outcomes of various fundraising campaigns from 2009 to 2017, to analyze outcomes of previous campaigns.  These data will be used to visualize the success of campaigns in relation to their launch dates during the calendar year and determine if there are any relationships between the outcome and fundraising goals.  
## **Analysis and Challenges**
###  **Analysis of Theater Campaign Outcomes Based on Launch Date**

####   *Add a new column for the Year & populate the table using Date function*
To better understand the outcome of various campaigns by launch date, we will analyze the data for trends in campaign outcomes over time.  First, the original dataset was copied and the new file was saved as ‘Kickstarter_Challenge.xlsx’.  Using the Kickstarter dataset, add a header row titled “Years” to a blank column (Column U).  Calculate the year the campaign launched from the ‘Date Created Conversion’ column (Column S) using the Year function ‘YEAR ()’ in Excel. Set the formula for cells U2 as follows = YEAR(S2) and paste this formula to all rows in the dataset as Illustrated in Figure 1. The year of launch is displayed in the column for each campaign. 

![image](https://user-images.githubusercontent.com/94234511/143689735-a4c2200b-4bb4-47cc-a871-b61e05f0ef51.png)

    [^note:    Figure 1: Add "Years" Column & Calculate Year of Launch]
####   *Create a Pivot Table in a new worksheet ‘Theater Outcomes by Launch Date’* 
The amount of information in the dataset is significant and it is difficult to visualize any relationships by reviewing the entire table.   The Pivot table function in Excel can be used to select and filter specific data into smaller tables to make analysis easier to present and describe.  After highlighting the Kickstarter worksheet, insert a Pivot table comparing the campaign outcomes to the launch date as shown in Figure 2. 

![image](https://user-images.githubusercontent.com/94234511/143689995-ddb987e4-aa05-48be-b6f2-f5bc7e279695.png)

    [^note:    Figure 2: Pivot Table Theater Outcomes by Launch Date]
    
Add the pivot table to a new worksheet titled ‘Theater Outcomes by Launch Date’.  Set the pivot table display by adding  ‘Outcomes’ field to the columns area and the Date Created Conversion field to the rows area, see Figure 3.

![image](https://user-images.githubusercontent.com/94234511/143690080-80870193-e626-4bbe-8407-85a806673697.png)

    [^note:    Figure 3: Creating the Pivot Table to Compare Outcomes]
    
To calculate the sum of each outcome by launch date, add the “outcomes filed to the Values area.  The sum of each row and column are automatically calculated and added to the data table.   From the table, we can determine the total number of live, successful, failed and cancelled for all 4114 campaigns from 2009 to 2017.   The summed data can be seen in the upper left of Figure 4.

![image](https://user-images.githubusercontent.com/94234511/143690120-581b411c-42f0-4726-a9dd-e167f83c10cc.png)

    [^note:   Figure 4: Pivot table Outcomes by Year]
    
####  *Set grouping and format the display of data* 
The data in the rows is grouped by year and then by quarter which may be useful for trending historical campaign performance.  However, to understand if the launch date impacts the ability of the campaign to be success, this grouping is not needed.  The ‘Quarters’ and ‘years2’ fields are removed from the pivot chart area for Rows.   The rows now reflect the month of the year the campaign was launched and the total count of successful, canceled, and failed campaign outcomes are displayed as illustrated in Figure 5 below.
![image](https://user-images.githubusercontent.com/94234511/143690560-50a6b364-653a-4986-90d3-c72a17c7e75b.png)

    [^note: Figure 5: Pivot table: Outcomes by Month
####   *Add Filters to the Pivot Table*
Fundraising outcomes similar to the Fever play campaign are of primary interest to Louise.  The pivot table generated so far contains all campaign types and outcomes.  From the Kickstarter file we can see that plays are a Subcategory of a broader Parent group of theatre campaigns.  After adding a filter to the pivot table, we can compare outcomes for only the “theater” parent category.  Add an additional filter for “Years”, this may be a useful tool for visualizing the results of smaller date ranges.  After adding both filters to the pivot table,  one for parent category and the other for “Years”, a drop-down menu can be seen in the Pivot table as illustrated in Figure 6 below. 
![image](https://user-images.githubusercontent.com/94234511/143690612-d7ae44dd-be5a-4fe4-a8dd-358f4b040d80.png)

   [^Figure 6: Filtered Pivot Table]
   
Finally, filter the columns to remove “live” campaigns and sort the column in descending order.  Now, the data for successful campaign outcomes are displayed first in each row.  When the number of successful campaigns is compared to the total, most outcomes were successful. This data will be easier to visualize if the successful campaigns are listed first. The pivot table appears as displayed Figure 7 below. 

![image](https://user-images.githubusercontent.com/94234511/143690653-f4fecb7f-1683-4d73-9182-5934d6216eaf.png)

####   *Create a line chart*
A line chart was created to visualize the data and placed next to the pivot table on the same worksheet. The title ‘Theatre Outcomes by Launch Date” was added to the chart and the pivot table fields were hidden.  After a few finishing touches, the line chart will appear as shown in Figure 8. 

![image](https://user-images.githubusercontent.com/94234511/143690686-5682ff5e-bc9b-49ce-8f35-15ab32f556fb.png)

    [^Figure 8: Line Chart - Theatre Outcomes by Launch Date]
    
If Louise is looking to compare outcomes for other types of fundraising campaigns this would be a quick way to provide additional analysis without creating a new pivot table.  Similarly, Louise campaign outcomes could be filtered by other date ranges to determine if there have been trends in campaigns over time.  
###   **Analysis of Outcomes Based on Goals**
Given the speed of Louise’s fundraising success, it may be interesting to see if a relationship between the fiscal goal and campaign outcome exists.  From the Kickstarter data file, the goal amount for each campaign can be seen in column D, the values range from $1.00 to $100,000.00.  This is a large range of values that could be grouped to summarize and make the data easier to visualize and interpret.  
####   *Create New worksheet & Define Goal Ranges*
A new worksheet was added and the sheet labeled Outcomes Based on Goals.  A series of ranges was defined and added to column A as illustrated in Figure 9 below.  
![image](https://user-images.githubusercontent.com/94234511/143690806-63fbfa2a-3de0-48ae-a46f-7b9703ee4206.png)

    [Figure 9: A series of ranges of goal amounts]
    
Expand the table by creating header rows in cells B1 to D1 containing the values “Number Successful”, “Number Failed”, Number Canceled”.  Since the fundraising goal is expected to be based on financial need for each campaign event, the data for this analysis will be limited to the subcategory “plays”.   

####   *Filter the data using COUNTIF statements*
Use COUNTIFS to filter the data in the Kickstart worksheet for each goal range, campaign outcome for the subcategory of “Plays”.   The code in example 1 below illustrates the use of Countifs statements to count data that meets multiple conditions.  For the Kickstarter data in this analysis, “outcome” is the only variable, the value for goal (</=$1000) and subcategory “Plays” does not change across the row. 
**Example 1**
Number Successful (Cell B2):  
=COUNTIFS(Kickstarter!$D:$D, "<=1000", Kickstarter!$F:$F,"successful", Kickstarter!$O:$O,"plays")
Number Failed (Cell C2):
=COUNTIFS(Kickstarter!$D:$D, "<=1000", Kickstarter!$F:$F,"failed", Kickstarter!$O:$O,"plays")
Number Canceled (Cell D2): 
=COUNTIFS(Kickstarter!$D:$D, "<=1000", Kickstarter!$F:$F,"canceled", Kickstarter!$O:$O,"plays")
