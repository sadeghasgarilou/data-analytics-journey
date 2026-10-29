# Day 44

## What I learned
- Types of merge :

| Join | What it preserves | Typical use |
|---|---|---|
| `inner` | Matching keys only | Analyse matched transactions |
| `left` | All left-side rows | Analyse all customers |
| `right` | All right-side rows | Preserve all orders |
| `outer` | All rows from both sides | Audit datasets |

- Merge using multiple keys : result = pd.merge(sales,targets,on=['product','region'],how='inner') -> Pandas matches a row only when both columns match.
- A practical warning : Imagine the left table contains a sales total of 1,000, and the right table contains three matching records. A many-to-many merge might repeat the 1,000 across multiple rows.
Before merging, ask:
1. Is the key unique in the left DataFrame?
2. Is the key unique in the right DataFrame?
3. Should the relationship be one-to-one, one-to-many, or many-to-many?
- Validate merges with validate : It checks whether the key relationships match your expectations : pd.merge(left_df,right_df,on='key',validate='one_to_one')
- Professional habit: When you know the expected relationship, use validate=. It can catch data problems before they silently affect your analysis.
- Different types of validate :

| validate value | Left key | Right key |
|---|---|---|
| `"one_to_one"` | Unique | Unique |
| `"one_to_many"` | Unique | May repeat |
| `"many_to_one"` | May repeat | Unique |
| `"many_to_many"` | May repeat | May repeat |

- Use indicator=True to investigate unmatched rows : audit = pd.merge(customers,orders,on='customer_id',how='outer',indicator=True)
- Pandas adds a _merge column with one of three values:

| `_merge` value | Meaning |
|---|---|
| `left_only` | The key exists only in the left DataFrame |
| `right_only` | The key exists only in the right DataFrame |
| `both` | The key exists in both DataFrames |

- This is particularly useful when combining data from different sources, such as customer databases, sales reports, and inventory systems.
- Remember: An unmatched record is not automatically an error. It is a record that deserves investigation.

## Exercises
- Create two dataframes and practice different merging on them.

## Course
- 
