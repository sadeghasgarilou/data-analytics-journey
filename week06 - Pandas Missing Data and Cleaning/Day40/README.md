# Day 40

## What I learned
- For cleaning text data at first we need to inspect it -> df['city'].unique() and df['city'].value_counts(dropna=False)
- This is an important analyst habit: inspect first, clean second, validate afterward.
- Pandas provides a powerful string accessor called .str. It lets you apply text operations to an entire Series without writing a loop.
- Make all letters upper/lower case : upper().lower() -> df['city'] = df['city'].str.upper()/lower()
- title() make the first letter upper case and other lower case -> df['city'].str.title()
- Remove extra spaces with .str.strip() -> df['customer'] = df['customer'].str.strip()
- Combine operations :
	df['city'] = (
		df['city']
		.str.strip()
		.str.upper()
		.replace({
			'say':'said'
		})
	)
- replace whole word wit .replace() or part of word with .str.replace() -> categories = categories.replace({'electronic':'electronics'}) / product_ids.str.replace('-','',regex=False) 
- Search text with .str.contains() -> df.loc[df['city'].str.contains('teh',na=False,case=False)]
- Useful parameters:
    case=False: ignore capitalization.
    na=False: treat missing values as False.
    regex=False: search for a literal substring rather than a regular expression.
- Search prefixes and suffixes with .startswith() and endswith() -> df.loc[df['city'].str.startswith('S',na=False)] / df.loc[df['city'].str.endswith('Z',na=False)]

## Exercises
- Create a customers Dataframe and practice text cleaning on it.

## Course
- 
