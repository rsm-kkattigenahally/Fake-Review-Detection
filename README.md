# Fake-Review-Detection Unsupervised Learning
Predicting fake reviews on Amazon product reviews.

## Dataset
Amazon product review dataset is used for this project. Only the 'All_beauty' product category is used in this project to make it computationally less expensive. This can be exted to other categories as well.
The data set is sources from https://amazon-reviews-2023.github.io/

## Use case 
1.Loaded the `All_Beauty.jsonl.gz` file and converted it into a dataframe.

2.Filtered the `review` DataFrame to include only rows where `verified_purchase` is `True`.

3.Converted the `timestamp` column from UNIX time (milliseconds) to a human-readable datetime format.

4.Checked & removed for duplicate rows based on the combination of `user_id`, `asin`, `text`, and `parent_asin` and stored them in `duplicate_rows`.

5.Converted the `text` column to lowercase for uniformity.

6.Dropped the `images` column.

7.Extracted the year and month from the `timestamp` column and added them as new columns (`year` and `month`). not sure if needed but just in case.

8. Similarly loaded the meta data and verified if there are any missing values or duplicates. parents_asin is the primary key in the metadata data.
   
10. Dropped unwanted columns and checked for missing values and made sure it was merged properly with the review data.
    
12. Filtered data for the years 2015 to 2023
    
14. After merging the data, checked if there are any missing values in the merged data.

16. Data pre-processing and text processing

18. Feature engineering

20. Text vectorization and categorical feature encoding

22. Implementation of K-means clustering and HDBSCAN to classify data as 'Fake' and 'Not Fake'


