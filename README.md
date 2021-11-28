# Play-Store-App-Review-Analysis-Capstone-Project
# Problem Statement:
The Google Play Store is the largest app market in the world. It generates
more than double the downloads of the Apple App Store but makes only half
the money as the Apple Store. Explore and analyze the data to discover the
key factors responsible for app engagement and success.

# Objective:
The objective of this project is to deliver insights to understand customer
demands better and thus help developers to popularize the product.
# Data set used:
1. Play_store_df
2. User_review_df
3. Merged_df (resultant of above two df after merging them)
# Scientific Computing tool & Data manipulation:
1. Numpy
2. Pandas
# Visualization libraries used:
1. Matplotlib
2. Seaborn
3. Plotly
# Steps involved:
# Loading the dataset 
We created a directorial path for the play store dataset, using the Pandas read function we read it. It has a shape (10841,13) which means it has 10841-row labels and 13 features or column labels.

After reading it we found which are the dependent variables and which are the independent variables, there is one dependent variable which is the number of installs or just installs, others are independent variables.

# Cleaning and Transforming Data
Cleaning is the process of removing undesired features, values, or any suffix, prefix, or anything which can produce an exception. 
Transforming is completely a different process, transforming is required to ensure the consistent data type of features because inconsistent data type will generate an obstacle during the execution of the program. 
These two processes have specific subprocesses as follows.

# Unwanted Data Removal
In this step we ensured to make a data type of feature consistent by removing characteristics from the values of features, to make them usable. Our data set has features installs which store the number of installs as per categories, but it has a 
(+) sign added at the end of its values, therefore we removed that plus sign. Feature size contains values regarding the application size, it has Mb and k as a suffix in its values, that’s why it is needed to replace k with k/1024, remove MB and k.
Feature reviews have the values of the number of reviews for each category, it is coming with some unwanted characteristics with its values, hence we removed.
The last update is a feature that stores the date of the last update for each application of each category. But it was given as an object we feed to pandas to the Date Time method and there we go; we have successfully converted it into a Date Time object.

# Removing duplicate values:
The app column has identical rows but with different categories and difference in number of reviews. It may have happened that for the same app, the data has been scraped at different points of time. So we have kept rows of an app based on the category with maximum number of reviews, assuming it to be the latest one.

# Null values Treatment
Two features of our data set have many null values, the first one is size and the second one is rating feature, so we filled null values with a mean, median and mode because we can assume that the size of the application could be an average of sizes available for a particular category and talking about rating, we have taken the median of rating for each category, and then we filled Nan with a mode for categorical data.

# Average Rating Distribution Plotly Bar Plot:
We grouped by category and took mean as aggregation operations on rating feature, we calculated rating mean for each category, and then we visualized that using Plotly bar plot. The average rating distribution for every category in the entire play store data set is around 4.2 out of 5. That’s incredible

Your app's rating will affect its chances of being featured. Apps with Rating 3 or lower will not be featured. The app rating is an important aspect of ASO (app store optimization). Negative mobile app reviews combined with a poor rating will hurt your app's rank, but great app reviews and high ratings will help increase your app's rank.
![Screenshot 2021-11-28 191538](https://user-images.githubusercontent.com/60994606/143770641-e5a85747-bd85-42dd-a5c0-f6ee2d63c0ac.png)

# Free vs Paid doughnut graph:
Here we can see that 92.22% apps are free and 7.78% apps are paid on Google Play Store, so we can say that Most of the
apps are free on Google Play Store.

![Screenshot 2021-11-28 191643](https://user-images.githubusercontent.com/60994606/143770710-a1c82a94-f76c-4335-83ea-a52ab2e28755.png)

# Last Update vs App line plot:
we can conclude that before 2011 there were no paid apps, but with the years passing free apps has been added more in comparison to paid apps, by comparing the apps updated or added in the year 2011 and 2018 free apps are increases from 0.01% to 80% and paid apps are goes from 0.27 to 4%. So, we can conclude that most people are after free apps.

![Screenshot 2021-11-28 192612year](https://user-images.githubusercontent.com/60994606/143770893-21e3da6f-2319-4f01-a2f2-63ada64296f5.png)

# Conclusion
The Google Play Store is the largest app market in the world.
As per our EDA, an ideal application on the google play store should obey the following properties/characteristics
1. Category Type: Before 2011 there were no paid apps, but with the years passing free apps has been added more in
comparison to paid apps, By comparing the apps updated or added in the year 2011 and 2018 free apps are increases from
80%% to 96% and paid apps are gone from 20% to 4%. So, we can conclude that most people are after free apps.
2. Installs vs Rating: Some Semi-popular apps are crossing a Million and then 10 Million, and only a few apps are able to go
beyond the 500M and 1B mark. Popular apps under Social media category like Facebook, WhatsApp, Instagram have more
than 1B installations.
3. Rating vs Installs vs Type: Free apps are preferred over paid apps and the rating are in range of 4 to 5.Therefore the free
Apps are most downloaded as compared to paid apps, Hence Developer should focus more on free apps.User prefer more of
free apps.Most of the apps present in playstore are more or less of the same size so size doesn’t affect their decision much.
4. The most installed category: As we have explored applications belong to the category gaming and followed by
communication are being installed the most , this is the clue to choose the category
5. User Reviews : User Reviews often contain valuable feedback and suggestions for improving the app. Analyzing the top trends
and issues for the app enables us to assess which parts of the app or game to focus on. It also shows where to invest in the business to improve the offering and create a more successful app or game.
6. Ratings : App rating is a reflection of how users respond to app. Learn what affects rating and what we can do to influence it.




