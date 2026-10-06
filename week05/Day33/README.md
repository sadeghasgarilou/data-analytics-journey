# Day 33

## What I learned
- GENETAL PATTERN :
	FILTER
	  ↓
	GROUPBY
	  ↓
	AGGREGATE
	  ↓
	SORT
- EXAMPLE :
	result = (
		sales[CONDITION]
		.groupby(GROUP_COLUMNS, as_index=False)
		.agg(
			metric_1=("column", "aggregation"),
			metric_2=("column", "aggregation")
		)
		.sort_values("metric_1", ascending=False)
	)
		
## Exercises
- Create a product DataFrame and practice groupby, sorting, filtering, and aggregation on it

## Course
- 
