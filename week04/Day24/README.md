# Day 24

## What I learned
- Sorting Multiple Columns -> employees.sort_values(['performance','salary']) -> 1-Sort by performance, 2-If performance is equal, sort by salary
- Different directions -> employees.sort_values(["performance", "salary"], ascending=[False, True])
- When we sort a dataframe, pandas normally places missing values at the bottom.
- Control NaN postion in sort with na_position -> employees.sort_values('salary',na_position='first')
- sort_index() -> sort based on dataframe index -> employees.sort_index(ascending=False)
- We can use head() and tail() to show top and bottom of data -> employees.sort_values('performance',ascending=False).head(3)
- nlargest() -> return n largest values based on column -> employees.nlargest(3,'performance') == employees.sort_values('performance',ascending=False).head(3)
- nsmallest() ->return n smallest values based on column -> employees.nsmallest(3,'performance') == employees.sort_values('performance',ascending=False).tail(3)
- Categorical order -> when we want to sort custom -> create categorical order : department_order = pd.CategoricalDtype( categories=["Data", "Backend", "Web"], ordered=True)
- Now after create categorical order we need to change dtype of our column : employees['department'] = employees['department'].astype(department_order)
- Finally we can sort it based on categorical order rather than alphabetical order : employees.sort_values('department')

## Exercises
- Create an employees DataFrame and sort it with different situation and condition

## Course
- 
