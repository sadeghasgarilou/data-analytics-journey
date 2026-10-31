# Day 44

## What I learned
- What is a merge key? A merge key is a column (or combination of columns) that Pandas uses to identify matching records between two DataFrames.
- Use on when the matching column has the same name in both DataFrames.
- Using left_on and right_on when two systems store the same information using different column names.
- Because both columns contain the same matching identifiers, you might not need both in your final output : result = result.drop(columns='client_id')
- Sometimes a single key isn't sufficient to identify the correct match : result = pd.merge(targets,sales,on=['product','region'])
- Multiple keys with different names : result = pd.merge(left_df,right_df,left_on = ['product','region'],right_on = ['item','sales_region'])
- Index-based merging : result = pd.merge(employees,salaries,left_index=True,right_index=True,how='outer')
- Key arguments recap :
1. Argument	        What it matches
2. on	                Same-named columns
3. left_on	            Named column(s) on left
4. right_on	        Named column(s) on right
5. left_index=True	    Left DataFrame's index
6. right_index=True	Right DataFrame's index


## Exercises
- Create two dataframes and practice different merging on them.

## Course
- 
