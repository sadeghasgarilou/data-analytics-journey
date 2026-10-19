# Day 41

## What I learned
- To Identify Duplicate rows, at first, we need inspect data with : df.info(), df.dtypes.
- Find duplicates : df.duplicated() -> Pandas returns a Boolean Series: True for rows considered duplicates and False otherwise.
- Inspect the duplicate rows : df.loc[df.duplicated()]
- Count duplicate rows : df.duplicated().sum()
- Remove duplicate rows : df.drop_duplicates() -> This keeps the first occurrence and removes subsequent identical rows.
- Find duplicates based on selected columns : df.loc[df.duplicated(subset=['order_id'])]
- inspect every row belonging to a repeated order ID : df.loc[df.duplicated(subset=['order_id'],keep=False)]
- The keep argument controls what duplicated() marks and what drop_duplicates() removes.
	1- keep="first"	Keep the first occurrence (default)
	2- keep="last"	Keep the last occurrence
	3- keep=False	Mark or remove every occurrence in a duplicate group
- Important analyst warning: Don't automatically remove every repeated order ID. In a real dataset, one order may contain several product lines. Before deleting records, determine whether the repeated ID represents a genuine duplicate or a legitimate multi-line order.
- Before removing duplicates, ask:
	1- Are all columns identical?
	2- Is the identifier supposed to be unique?
	3- Could repeated IDs represent separate products within one order?
	4- If records conflict, is there a reliable rule for deciding which one to retain?
- Data types tell Pandas how to interpret the values in each column. Common Pandas data types include: int64, float64, object, string, bool, datetime64[ns].
- Inspect data types : df.dtypes
- Convert text to numbers with astype() : df['sales'] = df['sales'].astype(float)
- Handle messy numeric columns with pd.to_numeric() : df['sales']= pd.to_numeric(df['sales'], errors='raise')
- The errors argument matters:
	1- "raise" — raise an error when conversion fails; useful when you want to catch unexpected values.
	2- "coerce" — convert invalid values to missing values (NaN).
- Convert text to dates with pd.to_datetime() : df['order_date'] = pd.to_datetime(df['order_date'], errors='raise')
- After converting a column to datetime we can extract the year, month, or day: df['order_year'] = df['order_date'].dt.year


## Exercises
- Create a messy sale dataframe and clean it.

## Course
- 
