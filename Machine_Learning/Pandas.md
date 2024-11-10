# Join Tables
- merge - sql like joins, inner, outer, left, right on keys
  - **If both key columns contain rows where the key is a null value, those rows will be matched against each other. This is different from usual SQL join behaviour and can lead to unexpected results.**
  - how = left, right, outer, inner, cross, default = inner
  - on = Column or index level names to join on
  - sort = bool, default false
  - left_on = lable or list, column or index level names to join on in left dataframe
  - right_on = lable or list, column or index level names to join on in right dataframe. 
```python
result = pd.merge(df1, df2, how='inner', on='key')
```
- join  - joins on index or key columns with on
  - other: DataFrame, series, or a list ocntaining any combination of them
  - on - str, list of str, or array-like, opotional
    - column or index level names in the caller to join on the index in other, otherwise joins index on index.
    - If multiple values given, the other DataFrame must have a multiIndex. Can pass an array as the join key if it is not already contained in the calling DataFrame.
  - how - left, right, outer, inner, cross, default left
    -   

  ```python
  result = df1.join(df2, how='left')
  ```
- concat - concatenation along rows or columns
- appendconbine_first - combines data frames, filling missing values


 | Method            | Primary Function                                      | Axis-Based | Joins | Index/Key-Based |
|-------------------|-------------------------------------------------------|------------|-------|-----------------|
| **`merge()`**      | SQL-like joins (inner, outer, left, right) on keys    | No         | Yes   | Key-Based       |
| **`join()`**       | Joins on index (or key columns with `on`)             | No         | Yes   | Index-Based     |
| **`concat()`**     | Concatenation along rows or columns                   | Yes        | No    | N/A             |
| **`append()`**     | Append rows to a DataFrame                            | Yes        | No    | N/A             |
| **`combine_first()`** | Combines DataFrames, filling missing values         | No         | No    | Index-Based     |

