# An Analysis of Kickstarter Campaign
Performing analysis on Kickstarter data to uncover trends
# Kickstarting with Excel

## Overview of Project
Performing data analysis on several thousand crowdfunding projects to uncover any hidden trends. This analysis was conducted by reviewing the financial viability of projects similar to the proposed project by comparing campaign metrics such as goals and pledges, outcomes, and rendering the result to pertain to theater and plays. This report highlights what types of projects are successful, how much money is typically vested, and when they are most likely to succeed so the client may make an informed decision about their project. 

### Purpose
Louise wants to run a crowdfunding campaign to promote her play "Fever", she needs to know more information about how to raise her goal of $10,000 successfully.


## Analysis and Challenges
I began parceling through data and considering what data would likely be "noise" for the project. Implementing filters, conditional formatting, and [Converting Unix Timestamps](https://websiteseochecker.com/blog/what-is-timestamp/) to readable format was the first challenge. Creating Pivot tables to isolate several variables and providing a clear and concise chart that could easily represent the data was the second challenge. The third challenge was consistently debugging `#DIV/0!` `=IFERROR(value,value_if_error)`, addressing outliers, establishing the statistical value of the data provided by using measures of Central Tendencies such as mean, median, standard deviation, upper and lower quartiles, and [interquartile (IQR)](https://www.thoughtco.com/what-is-the-interquartile-range-rule-3126244) and manipulating data to be the most effective for decision making.

### Analysis of Outcomes Based on Launch Date
One of the analyses conducted was to isolate key factors in crowdfunding campaigns: time of year, outcome viability, and category-specific renderings such as "theater". The month that launched the most successful Kickstarter campaigns was in May.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/107026442/175793240-d4406252-d92b-497c-9c56-e55385894421.png)

### Analysis of Outcomes Based on Goals
Another analysis conducted was to group campaign goals in increments of $4,999 from the range of $0 to $50,000+. Counting the number of successful, failed, and canceled projects and their percentages. The criteria for this analysis were strictly regulated to count the number of "plays" within each price bracket. This was achieved with a `=COUNTIFS` function which denotes counting the number of campaign goals within each price bracket, cross-examining it with success, failure, or cancelation of a project, and lastly only viewing "plays".

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/107026442/175793284-5a946a5e-0358-4c90-b674-144cbaf6a803.png)


### Challenges and Difficulties Encountered
Some difficulties I encountered were ensuring no data was lost or corrupted. It required me to be vigilant of all columns and rows that were filtered at any given time. I was sure to take note of the range of cells affected by filtration and if I moved columns or changed the data in any way I double-checked no cells were lost. Maintaining formulas amongst different columns also posed issues. I was faced with inconsistent calculations and had to redo the analysis and find where it initially went wrong. The mistake was a minor highlighting error that causes huge repercussions. Understanding how sensitive data is to corruption was a valuable lesson. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1) The best month to launch a campaign in May. 
2) Of all the campaigns that launched in April, 62% are successful and 35% fail.
Of all the campaigns that launch in May, 67% are successful and 31% fail.
Of all the campaigns that launched in June, 65% are successful and 32% fail.
Of all the campaigns that launched in July, 63% are successful and 36% fail.
Of all the campaigns that launched in August 63% are successful and 38% fail.

- What can you conclude about the Outcomes based on Goals?
The most successful campaigns will have approximate goals of 0-5000 (73%-76%)or $35,000-$39,999 (67%).

- What are some limitations of this dataset?
Why there is a spike in the success of campaign goals at $35,000-$39,999? 
Narrowing the dataset even more to genres and the specific cities of campaigns. There isn't enough information to make a decision.

- What are some other possible tables and/or graphs that we could create?
How many backers per price bracket?
How many successful campaigns were picked by staff?
Keywords or Phrases in the Blurb or Title that correlate to success? 
