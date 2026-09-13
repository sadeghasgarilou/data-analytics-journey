# Day 18

## What I learned
- summary functions : describe(), mean(), unique() : to see a list of unique values, value_counts() : to see unique values and how often they occured, median()
- map : In data science we often have a need for creating new representations from existing data, or for transforming data from the format it is in now to the format that we want it to be in later. 
- mapping methodes : map() and apply()
- map() : reviews['points'].map(lambda p: p - review_points_mean)
- map() returns a new Series where all the values have been transformed by your function.
- apply() is the equivalent method if we want to transform a whole DataFrame by calling a custom method on each row :
	def remean_points(row):
		row.points = row.points - review_points_mean
		return row
	reviews.apply(remean_points, axis='columns')
- If we had called reviews.apply() with axis='index', then instead of passing a function to transform each row, we would need to give a function to transform each column.
- Note that map() and apply() return new, transformed Series and DataFrames, respectively. They don't modify the original data they're called on. 
- We can do map by operator like row.points - review_points_mean but they are not as flexible as methodes

## Exercises
- 

## Course
- Summary Functions and Maps from pandas course of kaggle
