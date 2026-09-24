# Day 25

## What I learned
- Aggregation means taking many values and producing a summary value.
- sum(),mean(),median(),max(),min(),count(),nunique() are basic aggregation functions
- aggregation multiple columns : sales[['a','b','c']].sum()
- Multiple columns, multiple functions : sales[['a','b','c']].agg(['sum','min','max '])
- Different aggregations for different columns : agg() -> sales.agg({'a':['min','max'],'b':['sum','median'],...})

## Exercises
- Create an products DataFrame and practice aggregation on it

## Course
- 
