# Kickstarting with Excel

## Overview of Project

### Purpose
We have conducted quantitavive, descriptive analysis of a broad swathe of Kickstarter campaign data to extract trends and commonalities present in successful Kickstarter campaigns. Ultimately, this serves to provide instruction and guidelines to err on the side of to maximize the likelihood of a Kickstarter campaign successfully meeting its funding goal.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
In addition to other trends visible within the data, the time of year appears to possess a high degree of correlation with the success or failure of a Theater-related kickstarter.

By stratifying the data to include only datapoints relevant to the theater category, and plotting their outcomes across the months of the year, it becomes possible to rapidly visualize the relative success or lack-thereof of the campaigns launched during each portion of the year.

![SuccessByLaunchDate](https://github.com/Patchwork-Chimera/Kickstarter_Challenge/blob/main/Theater_Outcomes_vs_Launch.png)

Visible in the graph, certain months appear to be highly favorable (and others unfavorable) for the success of a Theater campaign. The most favorable month to launch appears to be May, during which 66.8% of kickstarters attained their funding goal. This is also the month seeing the largest number of Theater kickstarters launched, at a total of 166 campaigns.

Worth considering is that these traits may be due to students with an interest in theater who have either graduated, or are otherwise beginning a break period, launching their campaigns as school ends. This must be considered as a potential data-skew, as larger portions of kickstarters are likely started earnestly by those with newfound time and with requisite competence to appeal to potential donors during these months. This factor is not possible to assess with the data at hand however, and follow up analysis is necessary to quantify the effect this has on campaign success. 

### Analysis of Outcomes Based on Goals

When setting a goal, there does appear to be a "sweet spot" range of about $1,500 to $5,000 USD for both successful play campaigns as well as successful musical campaigns. It is possible to visualize this by creating a chart which stratifies the campaign goals into 12 elements of $5000 each (excluding the $50,000 and up category); and plotting campaign outcomes across the range of strata.

![SuccessByGoal](https://github.com/Patchwork-Chimera/Kickstarter_Challenge/blob/main/Outcomes_vs_Goals.png)

By identifying the decreasing percentage of successful campaigns as the campaign goals increase, it is reasonable to conclude that lower campaign goal figures are strongly correlated with overall success of the campaign. In fact, by analyzing the measures of central tendancy for the data, we can observe that approximately 50% of *all* successful campaigns had budgets between $1,500USD and $5,000USD. 

![DescriptiveStats](https://github.com/Patchwork-Chimera/Kickstarter_Challenge/blob/main/Plays%20Descriptive%20Statistics.png)

This grouping is likely to be caused by a myriad of reasons, one of the most important being that the achievability of lower goals is likely attractive to potential backers. When searching for campaigns to contribute to, backers are unlikely to be as swayed by campaigns they can only make insignificant, drop in the bucket sized contributions to; whereas campaigns of this size can be assisted meaningfully by fairly "everyday" quantities of money.

### Challenges and Difficulties Encountered
As with any analytical approach to decision making, there remain a number of challenges in applying any findings to reality. First and foremost, the problem of conflation takes center stage. As previously specified, it is *exceedingly* difficult to determine, using the data at hand, whether or not these trends are inherently descriptive and resultant from input factors relevant to their datapoint generation, or whether they are prescriptive trends that are resultant from the factors we have examined. 

To ilustrate, while it is possible to conclude for certain that, for example, campaigns launched in May enjoy higher rates of success than campaigns launched in December, it is not feasible with our current dataset to conclude that launching a campaign in may will give the individual campaign a higher chance of success. 

Another challenge encountered is the difficulty of separating out "serious" campaigns from simple cash-grabs and low effort campaigns. There are very notable outliers in the data, with some campaign goals reaching the 9 figures mark, which skew some of the less robust measures of central tendancy. This points to the existance of data within our set that may be non-illustrative due to the datapoints being generated via irrelevant means. To put it simply, we do not care about campaigns that someone put up with the goal of scamming money, but it is near impossible with the data at hand to expunge the invalid datapoints while not risking the integrity of the overall dataset. This may manifest as data appearing to be more varied than it meaningfully is, and likely over-localizes the "acceptable" range of both launch dates as well as campaign goals.

## Results

From the data available on campaign success versus launch date, it is possible to make two conclusions relevant to the goals of the analysis:

- As it stands, despite inability to generate a clear causal link, May presents a statistically significant amount of campaign success relative to other months, and thus would likely be the best timeframe to launch.
- The duration of campaigns also appears to be worth nothing. The average time it takes for successful campaigns to reach that point is 33.4 days. This value is overwhelmingly concrete, as only a very small percentage of successful campaigns resulted in the following 30 days, the 60 day mark being the other "spike" of successes and failures. These are near certainly due to campaigns being pre-timed for 30 or 60 days, and thus the vast majority of campaigns will culminate at this point. However, of the campaigns that do not reach their funding goal by this point, only relatively few reach it by day 60 of the campaign. Thus, if the campaign does not reach its goal by day 30, it may be prudent to re-evaluate the advertising and description for the campaign to make it more appealing. 


From the data analyzed in the context of campaign success by goal amount, a very clear conclusion can be reached:

- The campaign is likely best initialized with a goal of ~$5,000, that being the upper quartile point for successfully funded campaigns. If the campaign is successful, it has a non-insignificant likelihood of exceeding the goal by enough to make even projects which require slightly more feasible. However, by setting the goal at $5,000, it is more attractive to potential donors than higher amounts, which increases the likelihood of it getting there in the first place.

There is a notable limitation of the dataset in that it does not contain the requisite information to stratify by post-funding performance, which would aid in expunging fluke cash-grabs that managed to achieve their funding goal. Additionally, the inability to see causes of donations (be it comments, reviews, or other metrics) prevents us from determining if there is a causal link between the identiied correlations in the data.

Other graphs that could potentially be created are durations of given campaigns, to further illustrate the length of time needed before a campaign should be re-assessed to improve performance in another round of funding. Another graph that would be helpful is a graph of campaign outcome by length of blurb. This would allow us at least a baseline understanding of the correlation between blurb length and outcome of the campaign. One notable drawback to this would be that it is difficult to parse text data beyond basic characteristics on a large scale without the usage of NLP models or other advanced computing methodology, which increases project scope significantly. However, if this can be reasonably achieved, it would be possible to examine blurbs for trends that indicate "seriousness" or "competence" of a campaign, expunge that data, and examine a purer set of data for further descriptive analysis; or to generate prescriptive trends in successful campaigns' blurbs that can be applied when writing the blurb for a new campaign.
