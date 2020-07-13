# Kaggle_microCourses
 this repository is used for recording my exercise notebooks of Kaggle Courses:
 ### Pandas 
 #### Check course materials via [Kaggle Pandas](https://www.kaggle.com/learn/pandas).
  - [x] Creating, Reading and Writing
    
  | Command | Description |
  | --- | --- |
  | `pd.DataFrame()` | generate a DataFrame object |
  | `pd.Series()` | generate a Series object |
  | `mydata = pd.read_csv(filepath, index_col=0)` | read the data into a DataFrame |
  | `mydata.shape` | check how large the DataFrame is |
  | `mydata.head(n)` | examine the first *n* rows of the DataFrame |
  | `mydata.tail(n)` | examine the last *n* rows of the DataFrame |
  
  - [x] Indexing, Selecting and Assigning
    
  | Command | Description |
  | --- | --- |
  | `mydata.col_name` | select a specific Series out of a DataFrame (cannot handle column names with resevered char in them) |
  | `mydata[col_name]` | select a specific Series out of a DataFrame (can handle column names with resevered char in them)|
  | `mydata[col_name][index]` | drill down to a single specific value|
  | `mydata.iloc[i]` | **index-based selection** get the *ith* row of data in DataFrame|
  | `mydata.iloc[:, i]` | **index-based selection** get the *ith* column of data in DataFrame|
  | `mydata.loc[i, 'col_name']` | **label-based selection** get the *col_name* value of *ith* entry in DataFrame|
  | `mydata.loc[:, ['col_name1', 'col_name2']` | **label-based selection** get the *col_name1, col_name2* column of data in DataFrame|
  | `mydata.loc[(conditional_selection_1) & (conditional_selection_2)` | select the entries that satisfiy conditional selection 1 **AND** 2|
  | `mydata.loc[(conditional_selection_1) \| (conditional_selection_2)` | select the entries that satisfiy conditional selection 1 **OR** 2|
  | `mydata.loc[mydata.col_name.isin([value1, value2])` | select data whose value is in a list of values|
  | `mydata.loc[mydata.col_name.notnull()` | highlight values which are not empty `NaN`|
  | `mydata.loc[mydata.col_name.isnull()` | highlight values which are empty `NaN`|
  
  - [x] Summary Functions & Maps
      
  | Command | Description |
  | --- | --- |
  | `mydata.describe()` | generates a high-level summary of the DataFrame |
  | `mydata.col_name.describe()` | generates a high-level summary of the attributes of the column *col_name* |
  | `mydata.col_name.mean()` | see the mean of a column |
  | `mydata.col_name.unique()` | see a list of unique values |
  | `mydata.col_name.value_counts()` | see a list of unique values and how often they occur in the dataset |
  | `mydata.col_name.map(function)` | transform a Series by calling a custom method on each value in *col_name* |
  | `mydata.apply(function, axis='columns')` | transform a whole DataFrame by calling a custom method on each row|
  | `mydata.apply(function, axis='index')` | transform a whole DataFrame by calling a custom method on each column |
  
  - [x] Grouping and Sorting
      
  | Command | Description |
  | --- | --- |
  | `mydata.groupby()` | group DataFrame using a mapper or by a Series of columns |
  | `mydata.groupby().col_name.agg()` | run a bunch of different functions on DataFrame simultanuously |
  | `mydata.reset_index()` | reset index for DataFrame |
  | `mydata.sort_value(by='col_name')` | sort DataFrame by the values of *col_name* **default: ascending** |
  | `mydata.sort_value(by=['col_name1', 'col_name2'])` | sort DataFrame by more than one column |
  | `mydata.sort_index()` | sort DataFrame by index value |
 
 - [x] Data Types and Missing Values
      
  | Command | Description |
  | --- | --- |
  | `mydata.col_name.dtype` | ge the data type of the *col_name* column in the DataFrame |
  | `mydata.dtypes` | return the data type of every column in the DataFrame |
  | `mydata.col_name.astype('int64')` | convert *col_name*'s data type to *int64* |
  | `mydata.index.dtype` | a DataFrame or Series index has its dtype too |
  | `pd.isnull()` | select empty entries |
  | `pd.notnull()` | select non-empty entries |
  | `mydata.col_name.fillna('Unknown')` | repalce each missing value with an 'Unknown' |
  | `pd.col_name.replace('value_1', 'value_2')` | replace a non-null value *value_1* with *value_2* |  

- [x] Renaming and Combining
      
  | Command | Description |
  | --- | --- |
  | `mydata.rename(columns={'col_name_A':'col_name_B'})` | change the column name form *'col_name_A'* to *'col_name_B'* |
  | `mydata.rename(index={0:'col_name_A', 1:'col_name_B'})` | change some elements of the index |
  | `pd.concat([df1, df2])` | concat DataFrame or Series that have the same columns |
  | `left_df.join(right_df, lsuffix='_left, rsuffix='_right')` | combine different DataFrame objects which have an index in common |
 
  
