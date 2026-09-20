# Day 23

## What I learned
- Know data type of DateFrame or Series : reviews['price'].dtype or reviews.dtypes
- Convert a column of one type into another wherever such a conversion makes sense by using the astype() ->  reviews['points'].astype('float64')
- Entries missing values are given the value NaN, short for "Not a Number". For technical reasons these NaN values are always of the float64 dtype.
- reviews['points'].isna() / .notna() -> to find NaN and not Nan
- Replacing missing values : fillna() -> reviews['points'].fillna('Unknown')
- We may have a non-null value that we would like to replace : replace() ->  reviews['taster_twitter_handle'].replace("@kerinokeefe", "@kerino")
- We can exclude between boundaries -> employees["age"].between(25,30,inclusive="neither")
- We can use inclusive="left" and inclusive="right"
 
## Exercises
- create a employees DataFrame and filter it in different ways and with different conditions.

## Course
- Data Types and Missing Values from pandas course of kaggle
