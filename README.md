# 3459046_BD2_Assignment
# Introduction

In this project, I took the initiative to assist JC Penney better understand the relationships between their consumers, their online product reviews, and their online product reviews. JC Penney is a major retailer in the United States, and they are large quantity of customer product reviews. My objective was to analyze this data to determine the most frequent reviewers, and if different age demographic and geographical divisions, and product pricing, affect the level of interest in a product.

For my analysis, I utilized five primary data files. The products.csv contains the core product data, including the product's unique identification codes, names, prices, and ratings. The reviews.csv contains the user reviews, the ratings of the reviews, and we can determine which products receive the most reviews. The users.csv provides the most demographic information of the purchasers, including username, region, and age. I also utilized two json files, jcpenney_products.json which contains additional data about the products, and jcpenney_reviewers.json which provides background information about reviewers, their reviews and histories to assist in my analysis.

In Python, I cleaned and merged all these files to ensure I had dependable information that was easy to work with.

**Objectives**
The main objectives of my project are:
1. To improve data quality and usability through cleaning and merging multiple datasets from JC Penney.
2. To analyze how factors like product price and category affect consumer satisfaction and activity level in reviews.
3. To analyze product reviews by age and region in order to identify differences in shopping behaviors of specific customer segments.
4. To provide valuable and actionable information for JC Penney's marketing, pricing, and assortment planning decisions.
5. Achieving these objectives will help JC Penney gain valuable insights into their customer base, leading to more effective business decisions.

# Data Preparation and Cleaning
**2.1 Data Sources**

The coding files interacted directly with users.csv, jcpenney_reviewers.json, reviews.csv, products.csv, and jcpenney_products.json. The product information is real, while the user information is fictitious. This ensured consistency among the business insights and reproducibility among the Python workflows.

**2.2 Loading & Validation**

Leveraging pandas and the json library in Python to access CSV as well as JSON files, I began the process of loading the files and doing an initial inspection by outputting the first and the last rows of the data. I performed username checks to validate the merging keys, and I pruned the duplicated usernames in the data by utilizing the drop_duplicates() function. Initially, I checked for missing values and applied appropriate treatment on them, and I transformed the date columns to datetime objects to facilitate further profiling.

**2.3 Variable Engineering**

The primary engagement variable, Activity, was created with the use of pandas .apply() and a lambda in code, categorizing every user with one or more reviews as Active and as Inactive otherwise. In parallel with the review count, state, and user name, this variable formed the foundation of all subsequent code and analysis involving groupby and aggregation.

**2.4 Quality Check**

Recorded mitigation actions and verification rationale were incorporated sequentially into the code for the purposes of facilitating audits and providing clarity for the academic community and business professionals alike. User datasets underwent testing for duplicates and completeness as well as validation for key matching criteria prior to analytics generation.

# 3. Key Analyses & Visualizations

**a) Overall User Engagement: pie Chart**

**Code:** After an Activity variable was generated utilizing Pandas, value_counts, along with Matplotlib and Seaborn, were used to visualize the proportions of active and inactive individuals.

**Insight:** Identified from the code output and chart labels, the corresponding data indicate that 19% of the users, which translates to approximately one-fifth of the users for this app, are inactive users. This is one of the major marketing opportunities to capture this sector of the potential users.

**Business Meaning:** This segment is most likely to return high engagement when investing resources such as emails, discounts, or prompts. The code for the pie chart and the chart output are the most significant for reporting to the executives. The comments noted the alternative styles for the bar or comparison chart.


**b) Distribution of Users Review Activity: Histogram**

**Code:** To understand the engagement of users, I evaluated the number of products reviewed by each user based on the Reviewed column and .apply(len). then presented this data as a num_reviews column of the original dataframe. then added the summary statistics, such as mean, and maximum, as well as the number of people not providing any reviews.tthen plotted data as a histogram, utilizing Matplotlib to distribute the reviews, with rounded sky blue bars, and easily readable x and y axis.

**Insight:** The data illustrated in the histogram indicates that the majority of users only submit a limited number of reviews, whereas a small number of users submit a large quantity of reviews. This illustrates that the user engagement is concentrated to a small portion of the entire user population.

**Business Meaning:** With this information JC Penney can start implementing strategies on how to communicate effectively with this large group of less-active users while rewarding the active users with “super user” status to keep them engaged. The histogram can be utilized to know what part of your business needs to be changed to increase user activity and increase the number of reviews given.


**c) Top 10 States by active user %**

**Code:** I did the segmentation of users based on the user ‘State’ and I found the percentage of users within each state who were tagged as “Active” as per their review counts. I created a function in pandas utilizing a lambda function to determine the proportion of active users per state, and I sorted the data to obtain the first ten states. I represented this data using a horizontal bar chart in Matplotlib, as it was the best way to visualize and compare the level of user engagement per state. I emphasized the bars in specific colors, as I titled the chart as “Top 10 States by % of Active Users” to provide a clearer understanding of the data.

**Insight:** The chart displayed a strong engagement discrepancy with a majority of states in the US falling within a low percentage tier, and a select few with a high percentage of active users. This indicates that some states have a considerable number of customers available who submit reviews, thus categorizing those states as a feedback and engagement review hotspot.

**Business Meaning:** These states on the peak of the list are the marketing sweet spots for JC Penney in terms of promotional and campaign efforts. They also provide a more efficient way of utilizing business resources to improve engagement and foster closer relationships with customers.The chart is good in helping executives figure out which services to invest in to increase reviews and customer interaction.

**d)Engagement with age group : Bar Chart**

**Code:** Using the year of birth to determine age and placing users into age bands (e.g. 20-29, 30-39, etc.). I calculated the engaged participants of each age band using pandas and plotted the data in gold colored bar charts using the Matplotlib package. The data from the participants of each age range were represented in a visual manner allowing for easy engagement analysis of the age segments.

**Insights:** Bar diagrams made it easy to determine which age group(s) had higher engagement in reviews, especially the 30-49 age range. The engagement in this age range was much higher in JC Penney reviews than that of younger users (<= 20) and the older age group (>= 60) which resulted in a peak engagement in review participation.

**Business Maning:** Based on the age segments and engagement level in review participation, business marketing and review resourcing efforts would be best spent on the 30~49 age group, which would generate a higher possibility of engaging participants and feedback. Strategies to motivate participation of the younger and older group on reviews would also widen the low engagement user base.


**e) Price Band vs Average Review Score : Heat Map**

**Code:** Products data was cleaned by removing negative prices, and reviews, for each price range, were averaged and visualized on a Seaborn heatmap, which presented a tidy finish along with discrete average score values.

**Insights:** The heatmap made evident that a clear trend was absent. Review scores were consistent, across each range, which indicates that pricing was likely not a determining factor for the ratings.

**Business Meaning:** JC Penney ought to enhance product quality and customer experience across every price point. Marketing and quality improvements initiatives can be directed towards any price tier, concentrating on the lower-rated products irrespective of the price point.








