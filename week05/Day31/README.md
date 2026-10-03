# Day 31

## What I learned
- With one column: How much revenue did each product generate? -> sales.groupby("product")["revenue"].sum()
- #With two columns: How much revenue did each product generate within each region? -> sales.groupby(['region','product'],as_index=False)['revenue'].sum()
- we use a list of column names instead of just one column name when we want group by more than one columns.
		
## Exercises
- Create a product DataFrame and practice grouping + aggregation and sorting and filtering on it

## Course
- 
