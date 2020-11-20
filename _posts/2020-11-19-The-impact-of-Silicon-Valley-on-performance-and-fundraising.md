---
layout: post
title: The Impact of Silicon Valley on Fundraising and Performance Outcomes
subtitle: Exploring the other side of the entrepreneurial economy 
cover-img: /assets/img/silicon valley decision
thumbnail-img: /assets/img/Silicon_valley_title.png
share-img: /assets/img/Silicon_valley_title.png
tags: [Python, other]
---
Attention Entrepreneurs: Here's the truth behind whether Silicon Valley companies are better positioned for success

Since the dot.com boom in the mid-1990s, Silicon Valley has transformed into the global center for technology and innovation, and the home to many of the largest technology organizations and cutting-edge startup companies in the world. This phenomenon continues to reign true today as companies set up operations in or nearby the innovation hub to hire top talent and be in close proximity to a plethora of venture capitalists nearby. This surge in popularity has resulted in a meteoric rise in the hub's cost of living, particularly commercial real estate prices, which raises a very important question for US entrepreneurs: Does being located in Silicon Valley really lead to better fundraising and performance outcomes, or is an entrepreneur better off selecting a less expensive alternative?

The US Entrepreneurial Economy
The following chart illustrates the distribution of Venture Capital dollar volume across the United States from 1995 to 2018.

As you can see above, venture capital investment has steadily climbed since the dot.com crash in the early 2000s, with almost half of that going to companies located in San Francisco (North Bay Area) and Silicon Valley (South Bay Area). Given these trends, I would like to understand whether companies located in these areas are realizing better outcomes than their peers.

Data Selection
To help answer this question, I leveraged the Startup Investments dataset from Crunchbase, a platform commonly used to uncover information around public and private companies. I chose this dataset primarily because 1) this dataset has strong longitudinal features, including company data from the last 100+ years, 2) this dataset features a healthy amount of quantitative and categorical variables, allowing for some creative feature engineering, and 3) Crunchbase is a reputable website within the Technology community, leading me to believe that their data may be relatively accurate and up-to-date.

This dataset held ~50K records of company-level investment data, including company status (e.g., operating, closed, acquired), location (e.g., city, state, country), and fundraising metrics (e.g., total funding raised (USD), funding rounds), among other variables and metrics. Although, I must caveat that I removed all ex-US companies from the dataset since they likely operate under a unique regulatory environment w.r.t fundraising than their U.S. peers, bringing my dataset to ~25K company records.

Data Wrangling
Once the data was selected, I began to assess the quality of it. For the most part there were no glaring issues. In fact, outside of removing special characters and white spaces, and converting certain data types to numeric values, the data was ready to perform analytics on.
Fundraising & Performance Success Across the U.S.

To perform my analysis, which can be found on my GitHub, I employed a top-down approach, beginning with an initial data cut to get the lay of the land. For this data cut and my remaining analyses, I decided to split up the dataset into two pandas data frames by cross-checking a company's 'city' with the top 12 cities in Silicon Valley by population, according to Google.

As you'll see in the chart below, the initial data cut ended up informing the direction of my remaining analyses because of the slightly unanticipated results.

Unsurprisingly, the bulk of the funding (~76%) was allocated to the non-Silicon Valley companies, which comprise ~80% of the dataset. Additionally, Silicon Valley companies were almost twice as likely to get acquired than non-Silicon Valley companies, at least partially attributable to their close proximity to a vast VC community, in my opinion.
On the other hand, the average size of the Silicon Valley companies' fundraising round was roughly $2 million less than their non-Silicon Valley counterparts. Since this metric is calculated by dividing total fundraising dollars (USD) by number of fundraising rounds, this number can increase by increasing the total amount of fundraising dollars, decreasing the number of fundraising rounds, or a combination of both. Either way, this metric seems to entail a healthy fundraising environment for non-Silicon Valley companies. To investigate this 'a-ha' moment, I decided to dive deeper into these non-Silicon Valley companies to learn more information.

First, I analyzed the non-Silicon Valley companies by state to identify which states were contributing the greatest fundraising and performance outcomes.

As you can see in the chart above, companies from Connecticut, Georgia, and Texas experienced the highest average size of fundraising round for non-Silicon Valley companies. Meanwhile, companies from Massachusetts, Washington State, and California experienced the highest acquisition rate for non-Silicon Valley Companies. You may be wondering: how is California still in the top-10 after removing Silicon Valley / Bay Area from the results? This is because California is home to some of the most thriving metropolitan cities for startup companies, including Los Angeles and San Diego. These are interesting insights, but surely there are other factors contributing to the high performance and fundraising outcomes for non-Silicon Valley companies, right?

To pressure test this hypothesis, I decided to isolate the companies coming from the top-10 non-silicon valley states (in terms of fundraising outcomes) and identify the industries in which these companies reside.

According to the graph above, Mobile, Clean Technology, and Health and Wellness companies experienced the best fundraising outcomes. Although, if an entrepreneur's primary goal is to get acquired, it would be misguided to recommend that he or she build a Health & Wellness company given the very low acquisition rate in this industry, among other reasons. In such a case, an entrepreneur should look to build a Mobile, Software, or Clean Technology company as these industries experienced the highest acquisition rates.

Key Considerations
While this data may seem encouraging for non-Silicon Valley entrepreneurs, I would need a lot more data to increase my conviction in any recommendation to an entrepreneur. For instance, I used 'acquisition' as the sole performance success metric, which is only one piece of a much larger puzzle. Sure, there are founders who start companies with the intention or goal of being acquired, but there are also many founders who hope to achieve an Initial Public Offering (IPO) by bringing their company public. Unfortunately, this dataset doesn't feature an 'IPO' variable for me to include in my analyses.

Separately, this dataset does not provide any information related to the associated costs of operating inside or outside of Silicon Valley, which would be necessary in order to make any serious recommendations from this analysis. In addition, there are some other drawbacks of the current dataset that would need to be addressed in order to substantiate my findings.

Closing Thoughts
But, for now, it's encouraging to see that you can achieve fundraising and performance success in many geos across the U.S., especially for renters hoping to move to Silicon Valley in the future :). Therefore, let's continue celebrating and funding startup companies across the U.S., irrespective of their specific location!
