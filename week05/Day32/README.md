# Day 32

## What I learned
- agg() = Perform several aggregation operations and give the results together.
- There are 2 style that we can use agg() :
	1- Dictionary aggregation : Good when we want a quick summary :
		df.agg({
			"column_1": ["function1", "function2"],
			"column_2": ["function3", "function4"]
		})
	2- Named aggregation : prefer for analytical reports :
		df.agg(
			name_of_the_output_column_1 = ("source_column_1","function1"),
			name_of_the_output_column_2 = ("source_column_2","function2")
		)
		
## Exercises
- Create a product DataFrame and practice aggregation on it

## Course
- 
