# Kickstarting with Excel
Performing analysis on Kickstarter data to uncover trends 

## Overview of Project

### Purpose and Background

Louis's play _Fever_ came close to its fundraising goal in a short amount of time. She wants to know how different campaigns fared in relation to their launch dates and their funding goals. Using the Kickstarter dataset (specfically the category of theaters/plays), we wanted to visualize campaign outcomes based on their launch dates and their funding goals. 


## Anaylsis and Challenges

### Analysis of Outcomes Based on Launch Date

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/107021231/175805827-35091fd8-cfc5-4952-8bfe-6dfd2f31595d.png)

To create the _Outcomes Based on Launch Date_ chart, we had to create a pivot table based off the original Kickstarter spreadsheet data in Excel. Our goal was to visualize the outcomes-- successful, failed, and cancelled-- based on the launch dates. For the pivot table, we filtered "Parent Category" and "Years." The rows of the chart was set to show the  launch dates by month (January to December), and the columns of the chart was set to show the outcomes (successful, failed and cancelled). To reveal the data that we want to analyze, we will use the filter feature of the pivot table. We filtered the "Parent Category" to show only the data for "theater". For chart type, a line chart (with markers) will greatly help us visualize the relatinoship between outocmes and launch month. The line chart will reveal three lines to show the outcomes of successful, failed, and cancelled according to each month (Jan-Dec).


### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/107021231/175806067-11afd0e1-cec4-47a1-9d9e-4a1c26737c21.png)

To create the _Outcomes Based on Goals_ chart, we first had to create a 8-column-by-12-row chart. The 8 columns consisted of: Goal, Number Successful, Number Failed, Number Cancelled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Cancelled. The 12 rows consisted of amount brackets for Goal (Less than 1000, 1000 to 4999, 5000 to 9999, 10000 to 14999, 15000 to 19999, 20000 to 24999, 25000 to 29000, 30000 to 34999, 40000 to 44999, 45000 to 49999, 50000 or more). To calculate the results for each Goal amount bracket, we used the **COUNTIFS()** function and the following Excel formula: =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickerstarter!$F:$F,"successful",Kickstarter!$N:$N,"theater/plays"). Depending on the column or row, the formula would reflect the chosen results (i.e. successful, failed, cancelled; less than 1000,5000 to 9999, etc.). For total projects, we used the **SUM** function to calculate Excel B cells to D cells (B2:D2). And for the percentages, we just divided the chosen column cells (e.g. B2) with the total project column cells (e.g. E2) by using a slash (B2/E2). After calculating all the numerical data, we click under the "Insert" tab of Excel, to find the "Recommended Charts" to create the Line Chart to provide a visualization to analyze our results better. 

### Challenges and Difficulties Encountered

There was not much difficulty creating The first chart ( _Outcomes Based on Launch Date_). However, the second chart ( _Outcomes Based on Goals_) was a lot more challenging for me. To create the _Outcomes Based on Goals_, we first had to create 8-column-by-12-row chart. Unlike the first chart, where we just pull data off an orignal dataset and used the convenience of a Pivot Table to create our table, the second chart required our own accurate knowledge of Excel functions (e.g. COUNTIFS, SUM, percentag) to type out formulas for each result we wanted to calculate. My formula was correct, but I came to realize that I might have accidentally tweaked the original Kickstarter data (by accident) while working on it throughout my module sessions. As a result, my results/numbers did not provide correct numbers. Luckily, I saved an extra copy of the original Kickstarter data (the version that was untouched). This time, after typing in the same formulas into Excel, the results/numbers came out accurately to reflect a Line Chart that matched the chart provided in UCB Module Canvas. Also, had to be mindful of adding/omitting parantheses (), commas, quotations marks "".


## Results 

#### What are two conclusions you can draw about the Outcomes based on Launch Date?

Based on the _Outcomes Based on Launch Date_ chart, we filtered the following outcomes (successful, failed, and cancelled) according to the twelves months of the year (January-December). In terms of success, the two months with the most success were May (most successful) and June (second most successful), followed up by July as well (third most successful). In terms of failed, all months were relatively close in numbers (around 30ish, 40ish, 50ish). The most failed were in the following three months: May (52), and July & October tied with the same (50). The most cancelled (7) was in the early month of January. 

#### What can you conclude about the Outcomes based on Goals?

Based on the _Outcomes Based on Goals_ chart, reflecting upon the percentages, the most successful was for the Goal Amount Bracket of less than $1000, followed up by the Goal Amount Bracket of $1000 to $4999.The _Percentage of Succecssful_ dips toward the middle amount brackets, but rises again at the Goal Amount Brackets of $35,000 to $39,999 and $40,000 to $44,999. The Goal Amount Bracket of $45,000 to $49,000 was an 100% _percentage failed._, and there were no projects cancelled. 

#### What are some limitations of this dataset?

In terms of limitations of this dataset, it could help if there was more context to the data provided. Also, the country (US, GBP, EUR, etc) may provide insight on the data results, because the months may be different depending on which country. And gaining more background on the demographics of the type of people that gravitate or enjoy theaters/plays would be useful.

#### What are some other possible tables and/or graphs that we could create? 

Other possible table/graph that we could create would be a bar graph for the _Outcomes Based on Launch Date_ chart, or a pie chart for the _Outcomes Based on Goals_ to show the percentages or different goal amount brackets. 
