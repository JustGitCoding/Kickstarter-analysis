# Kickstarting with Excel

## Overview of Project

### Purpose
Analyzing seasonality of Kickstarters backing Plays and determining the optimal fundraising goal.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
We started by filtering the Kickstarter data for all campaigns related to _Theater_ backing and pivoting their outcomes against campaign launch months. With this data, we tried to determine whether there were certain months in the year that were more optimal for launching a _Theater_ Kickstarter Campaign. The green line in the chart below shows the total number of successful _Theater_ Kickstarter campaigns in any given month of the year between 2009 - 2017.
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/97985062/151686984-2c2dbad8-b476-4a4b-9b60-a1a12694e6d8.png)

### Analysis of Outcomes Based on Goals
With the same Kickstarter data, we further drilled down "Theater" campaigns to look specifically at campaigns related to "Plays". After splitting the data into 12 ranges (based on initial campaign goal size), we used =COUNTIF() formulas to determine the total number of successful vs failed campaigns in each bucket. This allowed us to estimate the success rate for various ranges of Campaign goals. The green line in the chart below shows the Success rate for various ranges.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/97985062/151687535-0d98ff5a-6c99-4498-be16-86f14a410e7e.png)

### Challenges and Difficulties Encountered
One of the challenges we faced during our analysis was that the date data was provided in Unix timestamp format, which is not easily convertible to "date" format in Excel. In order to overcome this challenge, we converted these timestamps into readable data by dividing each data point by 86,400 (60 * 60 * 24 = number of seconds in a day), and adding this number to the date January 1, 1970 (this is the date that Unix timestamps are based on).

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  Based on our analysis, we concluded that May appears to be the optimal month for lanching _Theater_ Kickstarter campaigns. Additionally, we found December to be the least optimal month for launching such a campaign.   
  
- What can you conclude about the Outcomes based on Goals?

  Based on our analysis, we believe that Kickstarter campaigns with lower goals tend to have a higher success rate, with goals less than $5K experiencing the highest rate of sucess.
  
- What are some limitations of this dataset?

  This analysis does not consider various qualitative data points (such as name-recognition of actors, entertainment value of Plays, etc), which also play a role in the success / failure of a given Campaign. Additionally, for the analysis of Outcomes Based on Goals, there was limited data to analyze for kickstarter campaigns with goals greater than $10K, which makes the percentage data less reliable. For example, based on the chart above, campaigns with goals < $20K seem to indicate that lower goal amounts lead to higher success rates. However, this does not hold true when we suddenly see that Campaigns with $35K to $45K goals have higher success rates than Campaigns with $5K to $34K goals. 
  
- What are some other possible tables and/or graphs that we could create?

  Of course, there are many other ways we can analyze this data. 
  - When thinking about potential launch dates, we should also consider that while May had the highest number of successful campaigns, it was also the month with the highest number of campaign launches in total. We could also plot the percentage of successful campaigns each month, to see which month had the highest sucess "rate" as opposed to simply the highest "count" of successful campaigns. 
  - In terms of Outcomes based on Goals, we may have considered splitting the population with Goals between $1 to $20K into one thousand dollar (instead of five thousand dollar) intervals. This may allow us to see the data at a higher level of granularity, and help to confirm our theory regarding diminishing returns on higher $ Kickstarter goals. 
