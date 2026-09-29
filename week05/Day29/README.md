# Day 29

## What I learned
- groupby() lets Pandas:
	1- Split rows into groups based on a column.
	2= Apply a calculation to each group.
	3- Combine the results into a summary.
- structure :
    sales
    .groupby("group_column", as_index=False)
    .agg(
        total=("numeric_column", "sum"),
        average=("numeric_column", "mean"),
        count=("id_column", "count")
    )
    .sort_values("total", ascending=False)
- as_index=False keeps product as a regular column not index : sales.groupby('product',as_index=False)['revenue'].sum().sort_values(by='revenue',ascending=False)
- Use this format(use name of column and a tuple contain column name and aggregation methode) with agg NOT a dictionary: 
	.agg(
        total=("numeric_column", "sum"),
        average=("numeric_column", "mean"),
        count=("id_column", "count")
    )
- User this orfer : Filter → Group → Aggregate → Sor

## Exercises
- Create a product DataFrame and practice grouping on it

## Course
- 
