# Day 26

## What I learned
- rename() -> change index names and/or column names -> reviews.rename(column={'points':'score'}) 
- rename index -> reviews.rename(index={0:"First",1:"Second"})
- set_index() -> more convenient way to change index.
- rename_axis() -> change axis name attribute -> reviews.rename_axis("wines",axis='rows').rename_axis("fields",axis='columns')
- combine different dataframes or series : concat() and join()
- concat() -> is useful when have different dataframe or series but having the same fields(columns). -> pd.concat([canadian,british])
- join() -> let combine different dataframe which have an index in common -> 
    left=left.setindex(['title'])
    right=right.setindex(['title'])
    left.join(right, lsuffix='_CAN', rsuffix='_UK') -> The lsuffix and rsuffix parameters are necessary here because the data has the same column names in both British and Canadian datasets.
- When you receive a business question, identify what it asks you to do:
    1- Which rows? Use filtering with .loc.
    2- What order? Use .sort_values().
    3- What summary? Use .sum(), .mean(), .agg(), or another aggregation.
    4- Summary by category or person? Use .groupby().
    
## Exercises
- create a dataframe of products and practice sort,filter, and aggregation on it.

## Course
- Renaming and Combining from pandas kaggle course
