- axis = 0 - rows, 1 - cols
- Summary of Key Steps and Functions:
  - Load Data: pd.read_csv(), pd.read_excel(), pd.read_json()
  - Inspect Data: df.head(), df.info(), df.describe()
  - Handle Missing Data: df.isnull(), df.dropna(), df.fillna()
  - Handle Duplicates: df.duplicated(), df.drop_duplicates()
  - Transform Data: df.rename(), df.astype(), df.apply()
  - Filter Data: df[df['column'] > condition]
  - Sort Data: df.sort_values()
  - Group and Aggregate: df.groupby(), df.agg()
  - Merge and Join: pd.merge(), pd.concat(), df.join()
  - Pivot: df.pivot_table()
  - Visualize: df.plot()
  - Export: df.to_csv(), df.to_excel()

--------------------
- Data Cleaning
  - Handling Missing Data (Imputation, Removal) https://pandas.pydata.org/pandas-docs/stable/user_guide/missing_data.html
    - filling missing data
      - fillna
        - value: The value(s) to replace missing data with.
        - method: Method of filling ('ffill' or 'bfill').
        - axis: Axis along which to fill (0 for rows, 1 for columns).
        - inplace: Whether to modify the DataFrame in place (default is False).
        ```python
        df.fillna(value=None, method=None, axis=None, inplace=False)
        ```
      - interpolate
      - replace
    - dropping missing data -
      - dropna
        - axis: Specifies whether to drop rows (0) or columns (1).
        - how: Drop rows or columns if all or any values are missing ('any' or 'all').
        - thresh: Require that many non-NA values before dropping.
        - subset: Specify which columns to check for missing values.
        - inplace: Whether to modify the DataFrame in place (default is False)
        ```python
                df.dropna(axis=0, how='any', thresh=None, subset=None, inplace=False)
        ```
    - flag missing values
      - None, but returns a DataFrame of the same shape with True for missing values and False otherwise.
      - isnull
        ```python
        df.isnull()
        ``` 
    - detect missing values:- isna, notna - consider None as missing value
      - to summarize missing values for each column use sum()
  - Removing Duplicates
    - check for duplicates
      - duplicated
        - subset: Columns to consider for duplicates (default is None to check all columns).
        - keep: Which duplicates to mark ('first', 'last', or False to mark all duplicates).
        - returns bool that indicates whether a row is a duplicate or not
        ```python
        df.duplicated(subset=None, keep='first')
        ```
    - remove duplicates
      - drop_duplicates
        - subset: Columns to consider for duplicates (default is None to check all columns).
        - keep: Which duplicates to keep ('first', 'last', or False to drop all duplicates).
        - inplace: Whether to modify the DataFrame in place (default is False)
      ```python
      df.drop_duplicates(subset=None, keep='first', inplace=False)
      ```
    - count duplicates = duplicated.sum
  - Handling Outliers (Winsorization, IQR Method)
  - Inconsistent Formatting (Date formats, Text normalization)
  - Dealing with Noise (Smoothing techniques)

- Data Loading
  - read_csv
  - read_excel
  - read_json

 - summary of data - data types, non null counts, etc - info
 - basic statistics - mean, min, max, quartiles - describe
 - Transformation and cleaning
   - change datatype - astype
   - rename column - rename
   - apply function - .apply
 - Filter data
 - Sorting data - sort_values
 - Grouping and aggregating data - groupby
 - merging and joining - merge, concat
 - Pivot ables - pivot table
 - data visualization - plot
 - exporting data - to_csv, to_excel





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

