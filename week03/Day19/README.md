# Day 19

## What I learned
- groupby() -> created a group of values which allotted the same values to the given columns name.
- reviews.groupby('points').points.count() = reviews.value_counts()
- after groupby : index is here = groupby('test') and values is after that = .point.count() -> so groupby by default return a Series
- We can use any of the summary functions we've used before with groupby : reviews.groupby('points').price.min()
- use apply with group by : reviews.groupby('winery').apply(lambda df: df.title.iloc[0]) = selecting the name of the first wine reviewed from each winery in the dataset -> when we use groupby with apply it return a DataFrame
- group by more than one column : reviews.groupby(['country', 'province']).apply(lambda df: df.loc[df.points.idxmax()]) = pick out the best wine by country and province
- agg() : lets us run a bunch of different functions on your DataFrame simultaneously -> reviews.groupby(['country']).price.agg([len, min, max])
- Multi-indexed : when we use groupby with more than one column we create multi-indexed DateFrame -> it is complicated with multi-indexed DataFrame -> we use df.reset_index() to convert it to regular index and convert indexes to columns
- sort_values() -> countries_reviewed.sort_values(by='len') : default sort ascending -> sort descending : countries_reviewed.sort_values(by='len', ascending=False)
- sort_index() -> sort by index : countries_reviewed.sort_index()
- sort by more than one columns : countries_reviewed.sort_values(by=['country', 'len'])
- sort by more than one columns and set them descending : students.sort_values(by=['python','math'],ascending=[False,False])

## Exercises
- practice sorting, grouping, and filtering in a students DataFrame

## Course
- Grouping and Sorting from pandas course of kaggle
