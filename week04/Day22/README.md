# Day 22

## What I learned
- Not = ~ -> employees.loc[~(employees['department']=='Data')] -> find employes who are not work at Data department
- isin() -> employees.loc[employees['department'].isin(['Data','Backend'])] -> find employees from either: Data, Backend
- between() -> employees.loc[employees['age'].between(25,30)] -> find employees between 25 and 30 years old. By default, between() includes both endpoints.
- string filtering : in pandas we use .str
- string filtering : 1- startwith : employees.loc[employees['name'].str.startswith('A')] -> find employees whose names starting with "A"
- string filtering : 2- endswith : employees.loc[employees['name'].str.endswith('a')] -> find employees whose names end with "a"
- string filtering : 3- contains : employees.loc[employees['department'].str.contains('data', case=False, na=False)] -> find employees whose departmant contain "data" -> case=False means case doesn't matter. and na=False is useful when the column contains missing values.
- missing values are None values that is shown NaN in DataFrame.
- Find rows where salary is missing -> employees.loc[employees['salary'].isna()]
- Find rows where salary is NOT missing -> employees.loc[employees['salary'].notna()]
- Don't do this: employees["salary"] == None, For Pandas missing-value detection, prefer: .isna() and .notna()
- Pandas has another elegant filtering syntax : query() -> employees.query('salary > 3000')
- multiple conditions with query : employees.query('salary > 3000 and age > 30')
- range with query : employees.query(' 25 < age < 30')
- For complex Pandas code, Boolean expressions with .loc are often more explicit. query() can be very readable for straightforward conditions.

## Exercises
- Create an employee DataFrame and do different filters on it

## Course
- 
