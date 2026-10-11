# Day 38

## What I learned
- By default, dropna() removes every row that contains at least one missing value : df.dropna()
- df.dropna() = df.dropna(axis=0, how="any")
- axis=0 for rows, and axis=1 for columns
- how="any": remove a row if at least one value is missing, and how="all": remove a row if all of values is missing.
- Remove columns containing any missing value : df.dropna(axis=1)
- Keep rows where at least one value is present : df.dropna(axis=0, how='all')
- IMPORTANT : Removing a row because any value is missing can be too aggressive. Real datasets often have thousands of rows, and we don't want to throw away useful information unnecessarily.
- Check only important columns : subset -> df.dropna(subset=['income']) -> This removes rows where income is missing, while allowing missing values in other columns.
- Require a minimum number of non-missing values : thresh -> df.dropna(thresh=3) -> keep a row if it has at least 3 non-missing values.
- Combine thresh with axis : df.dropna(thresh=4,axis=1)
- df.dropna(inplace=True) : This modifies df directly instead of returning a separate cleaned DataFrame.
- why the data is missing -> data intution -> Is this value missing because it wasn't recorded or because it doesn't exist?
- If a value is missing becuase it doesn't exist (like the height of the oldest child of someone who doesn't have any children) then it doesn't make sense to try and guess what it might be. These values you probably do want to keep as NaN. On the other hand, if a value is missing because it wasn't recorded, then you can try to guess what it might have been based on the other values in that column and row. This is called imputation.
- fillna() : to fill in missing values 
- replace all NA's with 0 : df.fillna(0)

## Exercises
- Create a dataframe and practice dropna in different situation.

## Course
- Handling missing values in Data Cleaning kaggle course
