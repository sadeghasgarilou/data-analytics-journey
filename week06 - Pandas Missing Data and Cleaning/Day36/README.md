# Day 36

## What I learned
- missing values refers to values that is not exist in our dataframe and they're shown with NaN or None. In data analysis, missing values can appear for many reasons.
- For example here Sara's Salary and Reza's age are missing Value :
		name 	age 	salary
	0 	Ali 	25.0 	1200.0
	1 	Sara 	30.0 	NaN
	2 	Reza 	NaN 	1500.0
	3 	Neda 	28.0 	1800.0
- Detect missing values : data.isna() or data.isnull() : They are effectively equivalent :
		name 	age 	salary
	0 	False 	False 	False
	1 	False 	False 	True
	2 	False 	True 	False
	3 	False 	False 	False
- At the above Each True means: There is a missing value here. True is 1 and False is zero. so we can use agg functions to get information about NaN.
- Count Missing Values for every columns : data.isna().sum() : Whenever we receive a new dataset, one of the first things we should do is: data.insna().sum()
- Missing percentage for every columns : data.isna().mean() * 100
- Finding Rows With Missing Values : data.loc[data['age'].isna()]
- Find rows with missing values anywhere : data.loc[data.isna().any(axis=1)] -> .any(axis=1) --> means: Does this row contain at least one True.
- How many missing values are there in the entire DataFrame? : practice.isna().sum().sum()
- Most important principle: Detect first. Understand second. Clean third.

## Exercises
- Create a dataframe and practice what I've learned about detecting NaN values in dataframe.

## Course
- 
