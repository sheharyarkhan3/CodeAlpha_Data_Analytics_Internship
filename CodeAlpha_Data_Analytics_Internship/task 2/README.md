# Task 2: Exploratory Data Analysis

## Objective
Explore the books dataset from Task 1 to find patterns, test a hypothesis, and detect data issues.

## Tools Used
Python, pandas, matplotlib, seaborn, scipy, Jupyter Notebook

## What I Did
 Defined questions before analysis
 Explored structure and data types
 Cleaned the Price column (text to number)
 Visualized price distribution, ratings, and price vs rating
 Detected outliers using the IQR method
 Tested a hypothesis (5-star vs 1-star prices) with a t-test

 ##Key Findings
 (A key finding is something the data told you. It answers the questions you wrote at the start of the notebook.

Prices are spread evenly from about £10 to £60. The histogram has no single peak, and the median price is around £36. Cheap, medium, and expensive books are all about equally common.
There are no price outliers. The boxplot has no points outside the whiskers, and the IQR check gave 0 outliers. No book is unusually cheap or expensive compared to the rest.
Ratings are fairly balanced. Each rating (1 to 5) has roughly 180 to 225 books. Rating 1 is the most common and rating 4 the least common, but the differences are small.
Price and rating are not related. The correlation is 0.028, which is almost zero, and the boxplots of price by rating look nearly identical. A higher rating does not mean a higher price.
The hypothesis test found no significant difference. The t-test gave p = 0.567, which is greater than 0.05. So we fail to reject H0: there is no evidence that 5-star books cost different amounts than 1-star books. The Spearman test agrees (r = 0.029, p = 0.356).)

##Data Issues
(A data issue is a problem or limitation in the dataset that could affect later analysis.

Price was stored as text. It had a £ symbol, so pandas treated it as an object, not a number. It had to be converted to float before any calculation.
Availability is the same in every row. All 1000 books are "In stock", so this column has no variation and is useless for analysis. It should be dropped.
No missing values and no duplicates. This is good news: the dataset is complete, and no rows needed removing.
The dataset is artificial. books.toscrape.com is a practice website, so the even price spread and lack of any price-rating relationship probably reflect how the site was built, not a real book market. Conclusions should not be generalized to real-world books.
Limited columns. With only title, price, rating, and availability, there is little to analyze. Fields like category, description, or product details would allow deeper analysis.)