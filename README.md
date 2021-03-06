# **Kickstart Analysis**

## Overview of Project

### Purpose

Our initial analysis revealed that “Theatre Plays” were the most successful of any category and subcategory. Further analysis revealed that campaigns held in May had a tendency of having the most successful outcomes. With that information Louise was able to launch a fairly successful campaign that came close to its fundraising goals. Now Louise wants to compare different theatre campaigns by launch dates and goals in order to see how her campaign faired overall. 

## Analysis and Challenges

In order to properly analyze the launch dates we must create a line chart in order to properly view any trends that occur over time. The first challenge we run into is when we create our pivot table in order to properly visualize the data. When our pivot table Axis is created with the "Date created conversions" column we see that there are tabs within each colomn, first by years, then quarters and finally the date created. 
![](Challenge_1.png)

In order to fix this issue we must remove the years and quarters colomn from our axis, since we already have a years filter that is derived from the date created conversions tab and to remove the quarters because we are interested in the specific dates that are seen. Making these two changes will make for a cleaner and much easier to read pivot chart. 
![](Challenge_2.png)

### Analysis of Outcomes Based on Launch Date

It is worth noting that the successful and failed outcomes seem to follow the same trends in terms of rising and falling of outcomes by month; in fact outside of December the data trends share the same peak (May) as well as low point (November). The following of the points seem to indicate that there may be other factors at play in terms of success and failure of theatre outcomes other than time of production.  

December proved to be the worst date to launch fundraising campaigns with only a 2 point difference between successful campaigns vs failed. There could be many reasons for the data in December, including but not limited to, the holiday shopping season as well as the major increase of theatre activity during the holiday season potentially playing a cannibalistic role. 

### Analysis of Outcomes Based on Goals

Before creating the chart, and pulling the data for succesful outcomes it is easy to run into some issues. Creating and Editing the CountIFS() function can present some challenges, especially after that deceptive ">1000" success you have in the B2 cell. After this it is natural to expand the formula that we have in our cell and expand the argument of the ">1000" cell that we have in B2 to B3 and get something like this. 
![](Issue.png)

This issue will create a 0 in the cell value colomn and that is because the stacked arguments create confusion for excel. We have to remember to write out the arguments for the count if functions one at a time like below. 
![](Solution.png)

Creting our commands like this is important because the code reads each argument one at a time and specifies results based on the argument added. After this we are ready to advance and eventually create our table chart. 

When viewing outcomes based on goals we would approach it expecting an almost supply and demand like curve, with successful campaigns decreasing the higher the goal and failures increasing. While the graphs begin and eventually end on that note, our line graph takes a flew flips near the end of the data, before eventually regrouping. We would definitely need to take a deeper look at the campaigns between 35000 and 44999 in order to see what drove the unexpected outcomes. However for the most part the data seems to show that increasing campaign goals increase the likelihood of a failed campaign goal, so it is possible that if Louise did not reach her goal she might have set the bar too high. 
 
## Results

The results from our analysis outside of a few anomalies shows two things that would have increased the likelihood of Louise earning her goal; the first would be a unique campaign starting in March, with a lower goal. Our analysis does however present some limitations, it is clear that there are other factors at work when it comes to analyzing the outcomes of these fundraising campaigns. Something that could affect the fundraising outcomes are things like salary demographics that would have a dramatic effect on the amount raised. A table column showing the median household income of the cities/towns where the fundraising efforts occurred could provide some meaningful insights on the campaign outcomes regardless of category.  

