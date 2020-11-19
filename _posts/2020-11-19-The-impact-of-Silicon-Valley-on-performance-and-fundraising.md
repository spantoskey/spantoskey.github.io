---
layout: post
title: The impact of Silicon Valley on Fundraising and Performance Outcomes
subtitle: Excerpt from Soulshaping by Jeff Brown
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [Python, other]
---
Attention Entrepreneurs: Here's the truth behind whether Silicon Valley companies are better positioned  for success

Since the dot.com boom in the mid-1990s, Silicon Valley has transformed into the global center for technology and innovation, and the home to many of the largest technology organizations and cutting-edge startup companies in the world. This phenomenon continues to reign true today as companies set up operations in or nearby the innovation hub to hire top talent and be in close proximity to the plethora of venture capitalists nearby. This surge in popularity has resulted in a meteoric rise in the hub's cost of living, particularly commercial real estate prices, which raises a very important question for US entrepreneurs: Does being located in Silicon Valley really lead to better fundraising and performance outcomes, or is your company better off selecting a less expensive alternative?

To help answer this question, I leveraged the Startup Investments dataset from Crunchbase, a platform commonly used to uncover information around private companies. I chose this dataset primarily because 1) this dataset has strong longitudinal features, including company data from the last 100+ years, and 2) this dataset features a healthy amount of quantitative and categorical variables, allowing for some creative feature engineering. That said, I had to wrangle the data to remove special characters and white spaces, and convert certain data types to numeric values prior to performing my analyses. Additionally, I removed all ex-US companies from the dataset since they likely operate under a unique regulatory environment w.r.t fundraising, bringing my dataset to ~25K company records.

To perform my analysis, which can also be found on GitHub, I employed a top-down approach to get the lay of the land. As you'll see in the chart below, your initial data cut can inform the direction of your remaining analyses.

Unsurprisingly, the bulk of the funding (~76%) was allocated to the non-Silicon Valley companies, which comprise ~80% of the dataset. Additionally, Silicon Valley companies were almost twice as likely to get acquired than non-Silicon Valley companies, at least partially attributable to their close proximity to a vast VC community.

On the other hand, the average size of the Silicon Valley companies' fundraising round was roughly $2 million less than their non-Silicon Valley counterparts. To investigate this 'a-ha' moment, I decided to delve into these non-Silicon Valley companies to learn more about their demographics.

First, I analyzed the non-Silicon Valley companies by state to identify which states were contributing the greatest fundraising and performance outcomes.

As you can see in the chart above, companies from Connecticut, Georgia, and Texas experienced the highest average size of fundraising round for non-Silicon Valley companies. Meanwhile, Massachusetts, Washington State, and California companies saw the highest percentage of companies acquired for non-Silicon Valley Companies. These are interesting insights, but surely there are other factors contributing to the high performance and fundraising outcomes, right?

To investigate this further, I decided to isolate the companies coming from top-10 non-silicon valley states (in terms of fundraising outcomes) and narrow in on the industries from which these companies are coming.

According to the graph above, Mobile, Clean Technology, and Health and Wellness companies experienced the best fundraising outcomes. Although, if an entrepreneur's primary goal is to get acquired, it would be misguided to recommend that he or she build a Health & Wellness company given the very low acquisition rate in this industry. In such a case, the entrepreneur should look to build a Mobile, Software, or Clean Technology company as they experienced the highest acquisition rates.

In conclusion, I would need a lot more data to increase my conviction in any recommendation to an entrepreneur, including their goals and interests, and whether the non-acquired companies within this dataset achieved an IPO, among other data. But, for now, it's encouraging to see that you can achieve fundraising and performance success in many cities across the U.S., especially for renters hoping to move to Silicon Valley :).
