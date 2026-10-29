# Day 43

## What I learned
- Why do we need merge()? To create a bigger dataframe with more information from more than one data frame using their shared column
- Merge to dataframe based on one share column : merged = pd.merge(leftdataframe,rightdataframe,on='customer_id')
- The four types of merge : set with how='' -> inner = pd.merge(customers,orders,on='customer_id',how='inner')
	a.Inner join : Keeps only matching keys from both DataFrames.
	b.Left join : Keeps every row from the left DataFrame and adds matching information from the right.
	c.Right join : Keeps every row from the right DataFrame and adds matching information from the left.
	d.Outer join : Keeps every key found in either DataFrame.
- Handling different key names and duplicate column names : merged = pd.merge(customers2,orders2,left_on='customer_id',right_on='client_id',how='inner')
- What if both tables have columns with the same name? : result = pd.merge(customers3,orders3,on='customer_id',suffixes=['_customer','_order'],how='inner')
- Validate merge : merged = pd.merge(customers,orders,on='customer_id',how='left',validate="one_to_many") = This verifies that each customer ID occurs at most once in the left table, while allowing multiple orders per customer in the right table.
It can help catch unexpected duplicate keys.

## Exercises
- Create a dataframe of customers and practice merging on it.

## Course
- 
