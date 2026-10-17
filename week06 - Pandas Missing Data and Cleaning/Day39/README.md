# Day 39

## What I learned
- fillna() : to fill NaN values in a DataFrame or Series.
- The central rule of fillna() : a replacement should make sense for the meaning of the column.
- Fill missing values with fixed value : 
    1- Replace missing values in one column : df['age'] = df['age'].fillna(0) or df['city'] = df['city'].fillna('Unknown')
    2- Fill different columns with different values :
        df_clean = df.fillna({
            'age':0,
            'city':'Unknown',
            'income':0
        })
    3- Mean, median, and mode: df_clean['age'] = df_clean['age'].fillna(df_clean['age'].median())
    or df_clean['income'] = df_clean['income'].fillna(df['income'].more()[0]) -> Why [0]? Because mode() returns a Series, and there can be more than one mode if multiple values tie for the highest frequency.
- The mode is the most frequent value. It is useful for categorical columns. 
- Check NaN after filling : df_clean.isna().sum()
- df_clean = df.copy() : Notice df.copy(). It lets you keep the original DataFrame unchanged while creating a cleaned version.
- Forward fill and backward fill : Sometimes, the order of the data matters. This is particularly common with dates, measurements, and time series.
- ffill() : Forward fill uses the most recent preceding non-missing value -> daily['temperature'] = daily['temperature'].ffill()
- bfill() : Backward fill uses the next available non-missing value -> daily['temperature'] = daily['temperature'].bfill()
- Remember: forward fill and backward fill depend on the order of the rows. If you're working with dates, sort by date first.
- This fills at most one consecutive missing value at a time : daily["temperature"].ffill(limit=1)

## Exercises
- create a customers dataframe and practice different way of fillna on it.

## Course
- 
