# Day 15

## What I learned
- There are two core objects in pandas: the DataFrame and the Series : 1-A DataFrame is a table. 2-A Series is a sequence of data values.
- If a DataFrame is a table, a Series is a list.
- Create DataFrame : pd.DataFrame({'Yes': [50, 21], 'No': [131, 2]}) ->  keys of dictionary are label of columns and by default it uses an ascending count from 0 (0, 1, 2, 3, ...) for the row labels.
 	Yes   No
0 	50 	  131
1 	21 	  2
- Assign row index to DataFrame instead of default numbers for row label : pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 'Sue': ['Pretty good.', 'Bland.']},index=['Product A', 'Product B'])
			Bob 			Sue
Product A 	I liked it. 	Pretty good.
Product B 	It was awful. 	Bland.
- Create a Series : pd.Series([1, 2, 3, 4, 5])
- A Series is, in essence, a single column of a DataFrame.
- Assig index to series values : pd.Series([30, 35, 40], index=['2015 Sales', '2016 Sales', '2017 Sales'], name='Product A')
- CSV file is a table of values separated by commas. Hence the name: "Comma-Separated Values", or CSV.
- Read from csv to pandas DataFrame : pd.read_csv("Address of file")
- DataFrame_name.head() -> grabs and return first five rows of DataFrame
- DataFrame_name.head(2) -> return first two rows
- DataFrame_name.tail(2) -> return last two rows
- DataFrame_name.columns -> return column names
- DataFrame_name.index -> check index of DataFrame
- DataFrame_name.dtypes -> check data types
- DataFrame_name.info() -> check general information
- DataFrame_name['column_name'] -> select a column -> is Series
- DataFrame_name[['column_name1','column_name2']] -> select 2 columns -> is DataFrame
- DataFrame_name["score"]       : Series
- DataFrame_name[["score"]]     : DataFrame
- iloc select data by numerical position : students.iloc[0] -> return first row
- students.iloc[0:2] -> select first two rows
- students.iloc[1,2] -> select a specefic value
- loc select data by index label : students.loc[1] -> select second rows
- select specific value -> students.loc[1,'age']
- filter the DataFrame : students[students['score'] > 80]
- select only the names of high scores students -> students.loc[students['score'] > 80,'name']
- filter by more than one condition : students[(students['score'] >= 80) & (students['age']>22)]
- and : & --- or : | --- Always put each condition inside parentheses
- Basic analysis with mean(), max(), min(), idxmax() : students.loc[students["score"].idxmax(), 'name'] -> return name of student with top score
- Get Descriptive Statistics -> students.describe()
- Create new column to DataFram : students['average'] = (students['math'] + students['python'] + students['statistics']) / 3
- Sort DataFrame : sorted_students = students.sort_values("average", ascending=False)
- index_col -> a read_csv() parameters to determine that which column set as pick as row index : wine_reviews = pd.read_csv("../input/wine-reviews/winemag-data-130k-v2.csv", index_col=0) -> first column picked as index 
- save a DataFrame in disk : DataFrame_name.to_csv("NameToSave.csv") -> animals.to_csv('cows_and_goats.csv')

## Exercises
- Define a DataFrame of students and inspect Data, Display some data, calculate statistics, and sort it.

## Course
- Creating, Reading and Writing from pandas course of kaggle
