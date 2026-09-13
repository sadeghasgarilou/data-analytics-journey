# Day 17

## What I learned
- Pandas indexing works in one of two paradigms : 1- index-based selection(iloc) : select based on numerical position, 2- label-based selection(loc) : select based on data index not numerical position
- iloc treats the dataset like a big matrix
- Both loc and iloc are row-first, column second. 
- iloc -> slect first row : test.iloc[0]
- get column with iloc -> test.iloc[:,3] -> : means everything
- it is also possible to pass a list as index of iloc -> test.iloc[[1,2,4],0]
- negative numbers can be used in index of iloc -> test.iloc[-5:]
- loc -> tets.loc[0, 'country']
- iloc -> 0:10 will select entries 0,...,9. 
- loc -> meanwhile, indexes inclusively. So 0:10 will select entries 0,...,10.
- isin -> isin is lets you select data whose value "is in" a list of values -> test.loc[test['country'].isin(['Italy','France'])].
- isnull and notnull -> These methods let you highlight values which are (or are not) empty (NaN) -> test.loc[test['price'].isnull()]
- csv means comma-seperated values.A CSV file stores tabular data as plain text.
- CSV files are common in data analysis because they can be exported from:
	Excel
	Databases
	Websites
	Business applications
	Kaggle datasets
- read csv in pandas : pd.reas_csv('my_csv.csv')
- write an DateFrame as csv file to system : test.to_csv('my_new_csv.csv', index=False) -> the argument of index=False prevents Pandas from saving the DataFrame index as an extra column.

## Exercises
- reviews.loc[[0,1,10,100],['country','province','region_1','region_2']]

## Course
- Indexing, Selecting & Assigning from pandas course of kaggle
