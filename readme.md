# Analysis of Reddit Post Features (Across 3 Subreddits
### Published By: Ronak Thakur
### Publish Date: 12/20/2021

## Introduction

Welcome to my Data Science Analysis tutorial! The goal of this tutorial is to have any reader be able to easily follow the steps that are involved with an analysis project such as this one. The steps illustrated within this tutorial include: data retrieval, data tidying, exploratory data analysis (EDA), and finally a bit of machine learning with decision tree classification. 

The data I use comes from posts made on the social media website called Reddit. Reddit is a hub for users to create posts on (almost) any topic imaginable and share these posts in different categories/communities called "Subreddits." Each post is formatted in the style of a "forum" post, allowing the users who read a post to comment underneath it and start a thread of replies. Each post can also be "flaired" with a custom tag depending on the subreddit (which helps users identify what type of post it is). 

For example, User A can make a post describing their family Macaroni and Cheese recipe to the "recipes" subreddit (typically referred to as /r/recipes with the "/r/" referring to the format required to access the subreddit from the search bar of a browser) and flair their post with the "Text Recipe" flair. User B can then leave a comment under User A's post saying how they used the recipe and enjoyed it. User B can then leave User A's post with an "upvote" to show their support for the post. 

The goal of this analysis is to verify or dispute my hypothesis that the number of comments has a direct correlation with the number of upvotes a post gets. Additionally, I am also curious to see how impactful different flairs can have on the success of a post (and whether or not it is possible to guess what flair a post has based on its number of upvotes and comments). Although I believe that this hypothesis will be disputed in the end (and will explain why in my conclusion), I believe that working towards this hypothesis will lead to some interesting data analysis!


### Dataset Overview

- Data Source: https://www.kaggle.com/prakharrathi25/reddit-data-huge

The overall dataset is an accumulation of data from over 5,000 reddit posts across 38 different subreddits (curated by Prakhar Rathi). Within the dataset are CSV files for each subreddit used within the dataset. Each individual subreddit's CSV file contains the following features:

- (Index)
- ID
- is_Original
- Flair
- num_comments
- Title
- Subreddit
- Body
- URL
- Upvotes

The dataset also contains a CSV file containing a merged csv file of all the posts analyzed (across all 38 subreddits), however for this project I did not choose to use this CSV file due to the features it contained not lending itself to any real EDA. 

After reviewing all of the subreddits present within Rathi's dataset, I ended up choosing 3 individual subreddits to use within my data analysis:

- /r/ApplyingToCollege
- /r/ComputerScience
- /r/COVID19

I chose these 3 specific subreddits due to the wide range of data I believed I would get for each subreddit. For /r/ApplyingToCollege, I believed that there would be a higher overall number of posts with comments due to the subreddit being a hub for high school students asking questions during their college application process. I chose /r/ComputerScience because I believed that this subreddit may follow the model of "more comments = more upvotes" that I believed to be true (as this subreddit is not primarily a QA subreddit like /r/ApplyingToCollege). Finally, I chose /r/COVID19 because I believe there may have been many posts that had many controversial comment sections, and I am curious to see how this quality would affect my hypothesis.

### Data Subset Decision — Explained
The specific data I chose to work with for this project was a subset of the larger overall dataset. I wanted to choose this dataset to illustrate that, although data analysis works best on datasets with large amounts of numerical data, it is still possible to use data analysis techniques to draw meaningful conclusions and test hypotheses. 

As you will see while reading through this analysis, I was not given a large number of features to draw relationships between, and as such I had to take a different approach for my analysis. As a result, the following project uses three different subsets (3 subreddits) of the dataset for each step of the analysis. Although this sample may not be fully representative of the entire dataset (and of every post in every subreddit on Reddit), there are still meaningful conclusions that can be drawn. The goal of this project is to find and explain those conclusions.

### Parts of the Document:
- Part 1: Data Retrieval
- Part 2: Data Tidying
- Part 3: Exploratory Data Analysis (EDA)
    - Part 3.1: (Upvotes Across Time [Scatter Plot])
    - Part 3.2 Breakdown of Top Flairs for Each Subreddit [Pie Chart]
    - Part 3.3 Relationship of Comments Vs. Upvotes [Scatter Plot]¶
    - Part 3.4 Correlation Matrices for Upvotes & Comments [Heatmap]
- Part 4: Machine Learning [Decision Tree (Classification)]

## Conclusion

And that concludes my tutorial on a Data Science Analysis project! Overall, I had quite a lot of fun getting to walk through the major steps of data analysis with a dataset of my own choosing. Coming up with my own relationships to look at was definitely stressful to think about, however getting to see the results (and seeing those results completely refute my initial hypothesis) was a very fun experience. Although my Machine Learning model did not perform extremely well, it was still interesting to see if the computer could go through and draw relations between variables that I would never have been able to. 

Additionally, working with a dataset that did not have a plethora of information to draw from definitely posed some challenges throughout my analysis, however I am proud of the ways I came up with to use as much of the data as I had as possible. Moving forward, I think that one aspect of this project that I was unable to look at (but could possibly be an area of further research) is analyzing the words used in the title of each post. Did some words perform better than others? Was a certain word being repeated which potentially influenced the number of upvotes / comments? Could my decision tree perform better if it is also fed the words of the title of the post? These are just a few of the questions that I would look into if I were to continue this project moving forward.

However, to conclude my project as a whole - I hope that this tutorial was an interesting read for anyone interested in the process of conducting a data science project! Thank you again to Prakhar Rathi for curating and providing the data.

If you would like to access my github page to see my notebook, click the link below:

- https://ronak-thakur.github.io/Reddit-Posts-Analysis/