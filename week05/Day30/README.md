# Day 30

## What I learned
- pattern of multiple aggregation + grouping :
	sales.groupby('product', as_index=False).agg(
		total_revenue=('revenue','sum'),
		average_revenue=('revenue','mean'),
		minimum_revenue=('revenue','min'),
		maximum_revenue=('revenue','max'),
		total_quantity=('quantity','sum')
	)
- Total pattern : 
		FILTER
		   ↓
		GROUP
		   ↓
		AGGREGATE
		   ↓
		SORT
		
## Exercises
- Create a product DataFrame and practice grouping + aggregation and sorting and filtering on it

## Course
- 
