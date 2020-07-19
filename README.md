# An Analysis of Kickstarter Campaigns
## Overview of Project
Project is to analyze Kickstarter information and provide feedback on the best timing and goal amounts to start and achieve a successful campaign.

### Purpose
The client had a previously failed Theater/Play campaign and has requested this study to assist in making a future decision.  The analysis compared two markers, Launch Date and Funding Goals, to assess if these two characteristics correlated to successful campaigns. Results, written as well as visual, has been provided.

## Analysis and Challenges
Analysis began with general inspection of the data.  There were 4,114 records covering the period of May 2009 through May 2017.  For the most part, the data was clean but did notice the “id” identifier started at zero (0).  Ideally, a unique identifier would not be zero.  When verifying counts, manual adjustments were made to maintain accuracy.  
Most notable issues were the two date fields, “deadline” and “launched_at” as they were formatted in Unix time.  Two new fields were created, “End Date” and “Launch Date” respectively, to store the converted Unix to Human-Readable Dates.  

Other fields were also created to assist in the analysis: “% Funded”, “Avg Donation” and “Days to Complete”.  % Funded was calculated by Pledged Amount divided by Goal Amount.  Avg Donation was calculated by Pledged Amount divided by number of donations made.  Days to Complete was calculated by taking the End Date less Launch Date - essentially the difference in the number of days. 

To perform the requested analysis, the data was filtered for only “Successful”, “Failed” and “Canceled”, which totals 4,064 records.  The remaining 50 (of 4,114) were classified as “Live” and were excluded from the study.  The dataset included all countries and all categories.

## Results
### Analysis of Outcomes Based on Launch Date
Two conclusions were drawn regarding Theater Outcomes based on Launch Date.  The first is that most successful outcomes launch in May.  Since the average days to complete the campaign is slightly under a month, one would expect to be fully pledged by June.  The second conclusion is that failed outcomes occur evenly (for the most part) across all months.  Please see [chart](https://github.com/Eblakeiii/Kickstarter_Analysis/blob/master/Resources/Theater_Outcomes_vs_Launch.png.png)

### Analysis of Outcomes Based on Goals
Analysis about the Outcomes based on Goals was that two Goal amount levels have the highest success rate.  The dollar levels are less than $1,000 and $1,000 to $4,999.  These success rates are 71% and 66% respectively.  As expected, the failure rates increased with larger Goal amounts, ranging from 37% to 58%.  The combined failure rate for campaigns over $5,000 is 45%.  Please see [chart](https://github.com/Eblakeiii/Kickstarter_Analysis/blob/master/Resources/Outcomes_vs_Goals.png.png)

### Challenges and Difficulties Encountered
Limitations of the dataset: 1) unable to validate any of the components; 2) unable to determine if  campaigns were excluded – no way to verify a completeness of dataset; 3) unable to determine if online marketing – or other non-quantitative circumstances - had a role in its success or failure.

## Alternatives
A possible alternative study would be to perform statistical analysis of Goal and Pledged amounts as well as Launch Dates.  The resulting information would provide some insight into the validity of the dataset and how confident one can be with predicting future trends.  Statistics used would be Mean, Median, Standard Deviation and Quartiles for both Goal and Pledged amounts.  The data could be shown either in graphical or table format.  This would be performed for both the Successful and Failed campaigns.


