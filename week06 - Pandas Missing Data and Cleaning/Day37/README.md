# Day 37

## What I learned
- isna() = Find Missing values
- notna() = Find present values
- We can inspect with more than one condition : df.loc[(df['age'].isna()) | (df['income'].isna())]
- Count missing values per column : df.isna().sum()
- Count present values per column : df.notna().sum()
- Count rows with at least one missing value : df.isna().any(axis=1).sum()
- Count rows where every value is present : df.notna().all(axis=1).sum()
- any(axis=1) checks whether each row has at least one missing value.
- all(axis=1) checks whether every column in a row is present.

## Exercises
- Create a dataframe and practice isna() and notna().

## Course
- 
