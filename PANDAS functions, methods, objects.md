# Questions didn't answer yet

1. What is the best when using pandas, key-word argument or positional?
2. I don't know what is the correct name in the Series method: product or prod
3. View all functionalities of `describe()` method
4. use of loc[]
5. STUDY MORE ABOUT MULTIINDEX


# Data Analysis process

1. The process of cleaning data is called **wrangling or munging**
2. Reshaping
3. 


# Modules, Libraries

1. datetime
2. 

# FAQ

1. [Why is the dtype of string Object?](https://stackoverflow.com/questions/21018654/strings-in-a-dataframe-but-dtype-is-object)
2. What does says the number in the data type?
   float64,
   int64 and so on indicate that each floating-point/integer value in a pandas object occupies 64 bits
   (8 bytes) of the RAM

# Concepts
1. A function is a *first-class* object in Python, which means that the language treats it like
any other data type. A function may feel like a more abstract entity, but it’s as valid a
data structure as any other.
2. A regular expression is a search pattern that looks for a sequence of characters within a string
3. A MultiIndex is an index object that holds multiple levels.
4. A class method is a method we invoke on a class rather than an instance.

# Useful information

* it’s optimal to sort our index before we look up any row
* A MultiIndex is an index made of multiple levels.
* A MultiIndex uses tuples of values to store its labels.
* A DataFrame can store a MultiIndex on both its row and column axis.
* The sort_index method sorts MultiIndex levels. Pandas can sort index levels individually or as a group.
* The label-based loc and the position-based iloc accessors require additional arguments to extract the proper combination of rows and columns.
* Pass tuples to the loc and iloc accessors to avoid ambiguity.
* The reset_index method integrates index levels as DataFrame columns.
* Pass the set_index method a list of columns to build a MultiIndex from existing DataFrame columns.
* The order matters when setting a multiindex, first must be the categorical data with less values
* Columns with a small number of unique items usually represent categorical data and are good candidates for index levels
* The xs method allows us to extract rows by providing a value for one MultiIndex level
* The form `df['name2':'name2']` just is valid, and it extract multiples rows. **it is not valid `df['name']` for this use `df.loc['name']` 
* When should use in multiIndex`df['outer category']` to extract the level 0, if we can't extract at once the level 2
* The `loc[]` accessor extracts by index label, and the `iloc[]` accessor extracts by index position.
* Indices can hold various data types: strings, numbers, datetimes, and more
* The pandas documentation recommends the following indexing strategy to avoid uncertainty. Use the first argument to loc for row index labels and the second argument for column index labels.
* pandas distinguishes between list and tuple arguments to accessors. Use a list to store multiple keys. Use a tuple to store the components of one multilevel key
* A good way to start thinking about the MultiIndex object as an index in which each label can store multiple pieces of data.
* Pandas Series has one dimension, DataFrames two dimensions, but actually it is possible to work in more dimensions with the `MultiIndex`
* In pandas terminology, the collection of tuple values at the same position forms a level of the MultiIndex.
* Delete a column with `df.drop(columns='columname')` or with `del df['columname']`
* How can we know all different values a column can contain? With the `unique()` method
* The process of cleaning data is called wrangling or munging
* The accessor for the string methods on values of a DF is `str`; `df.Column.str`
* this: `print` is a function, this: `print()` is the **invocation** of the function
* We can't use sets to create Series. If we have sets, we have to convert to another type, like a list
* Numpy is a dependency of Pandas. Some objects are built into Numpy objects
* Most mathematical methods ignore missing values by default. We can pass an argument False to the `skipna` parameter for the inclusion of nan values
* We can perform operations with +, -, *, /, //, %, ==, != in a Series object. The behavior is element-wise and **the operation is performed by labels. Pandas align shared index to perform operations**
* Also, we can work thr arithmetic operator with methods: `add()`, `substrac()`, `multiply()`, `div()`, `floordiv()`...
* Series values are stored in a numpy ndarray under the hood
* Broadcasting: 
* We can a Series to any Python's built-in function
* We can change from data frame to a Series simply with have one column setting an index
* `read_csv` function has a parameter `parse_dates` that changes the date string to type Date
* `read_csv` function has a parameter `usecols` where we specify what columns import
* We can sort a Series by its values or its index, in ascending or descending order
* `sort_values()` parameters more useful: `ascending`, `na_position`
* Use `dropna()` method to remove nan values. **No valid for drop nan in index**
* It is possible so sort values or sort the index with `sort_values()` or `sort_index()` respectively
* `nlargest()` method returns the five largest values from a Series. **Only works with numbers**
* `nsmallest()` method returns the five smallest values from a Series. **Only works with numbers**
* The `inplace` parameter of some methods **modify the original object**  when is set to True
* The `inplace` parameter of some methods **return a copy**  when is set to False
* The `inplace` parameter is not recommended
* `value_counts()` counts the number of occurrences of values in a Series. Return a new Series where the index are the values of the original series
* To identify trends in numeric data sets, it can be more beneficial to group values into predefined intervals rather than count distinct values.
* The `bins` parameter of `value_counts()` group the values in half-open intervals. It accepts the intervals as a list, or a int of how bins we want
* When working with dates, use `datetime` module; `strftime('%')`, `date`, `datetime`
* When using dictionary to feed the data, the keys will be the column name and the values the column values
* Transpose is swap colum headers with the index labels in a DataFrame with the `T` or `transpose()`method
* We can set a customize index label With the `index` parameter of `DataFrame` constructor we pass an iterable to change the index labels, they have to match the same number of rows
* We can modify the column names with the `columns` parameter of `DataFrame` constructor, we pass an iterable to change the names, they have to match the same number of columns
* All dataframe methods, works on the axis 0, the rows
* We can set an index column from `read_csv()` function or with the `set_index()` method
* With the `accessor` `loc[]` we can extract rows, rows and columns and also do **slicing** but this time inclusive in both start and end
* Remember with `df['name']` we extract **COLUMNS**; with `df.loc[]` **ROWS**
* We can change the column names with the `df.columns=list` OR with the `rename()` method using the `columns` parameter
Or also we can change the index label using the `index` parameter
* The loc attribute extracts rows or columns by index label
* about reducing memory: Whenever importing a data set, it’s important to consider whether each column stores
its data in the most optimal type. The “best” data type is the one that consumes the
least memory or provides the most utility
* With the following syntax we compare each value of a Series with the other value
`Series == value` -> Series of booleans
* The `how="all"` parameter in the `dropna()` method only removes the row if ALL values of that row are NaN
* The `subset` parameter in `dropna()` method just looks for NaN in the column 
* The `thresold` parameter in `dropna()` method just specify for a minimum of missing values for remove the row
* The category data type is ideal when a Series has a small number of unique values.
* Helper methods such as `isnull`, `notnull`, `between`, and `duplicated` return boolean Series that we can use to filter data sets.
* The `fillna` method replaces NaNs with a constant value.
* The `dropna` method removes rows with null values. We can customize its arguments to target missing values in all or some columns.
* 

# General Functions

* read_csv() -> DataFrame
* `class` `constructor` [Series()](https://pandas.pydata.org/docs/reference/api/pandas.Series.html) -> Series
* `class` `constructor` [DataFrame()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) -> DataFrame


# Types of values

* Object: 
* NaN: Not a Number
* NaT: Not a Time
* int64
* float64
* category: ideal for a column consisting of a small number of unique values relative to its total size like gender,
blood type, weekdays, planets, and income groups, for example. We use `"category"` in code

# Syntax and notation

```
criteria = DataFrame['name'] == 'row_value'
DataFrame[criteria]  # -> Series (if just one name), DF with more than one name
```

Here we use `&`, `|`, `~` for logic operations

`~` is an inverser, so True becomes False

![Alt text](/home/diego/Documents/practicing_data_analysis/Pandas in action book/img/boolmeth.png)

We can apply a specific core python method to pandas' objects, 
and it will be applied for each element of the object
like the following example: `object.index.str.lower()`
These are known as the "accessors" and the "mutators"

We can extract a single column from a dataframe with `df.name` or `df['name']` and returns a Series with the respectively key
**it is recommended to use `df[`name`]` because `df.name` does not recognize spaces as `~~df.my name~~`**

With `df[['columname1', 'columname2']]` we can extract more than one column from a df

To extract rows that meet some criteria we can do `df[[list of bools]]` where list of bools must be the same number of rows


# Built in functions, operators

| Built-in     | operators |
|--------------|-----------|
| len()        | in        |
| type()       | for       |
| dir()        | []        |
| list()       |           |
| dict()       |           |
| strip()      |           |
| lstrip()     |           |
| rstrip()     |           |
| lower()      |           |
| upper()      |           |
| title()      |           |
| capitalize() |           |
| slice()      |           |
| replace      |           |



# DataFrame

| methods                                                                                                             |                                      attributes                                       |
|:--------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------:|
| head()                                                                                                              |   [shape](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.ndim.html)    |
| tails()                                                                                                             |    [size](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.size.html)    |
| sort_values()                                                                                                       |                                      dtype**s**                                       |
| sort_index()                                                                                                        |   [iloc[]](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iloc.html)   |
| value_counts()                                                                                                      |    [loc[]](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html)    |
| [squeeze()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.squeeze.html)                             |   [index](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.index.html)   |
| [transpose()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.transpose.html)                         |       [T](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.T.html)       |
| [count()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.size.html)                                  | [columns](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.columns.html) |
| [sample()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sample.html)                               |    [ndim](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.ndim.html)    |
| [nunique()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.nunique.html)                             |     [at[]](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.at.html)     |
| [max()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.max.html)                                     |    [iat[]](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iat.html)    |
| [min()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.min.html)                                     |                                                                                       |
| [nlargest()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.nlargest.html)                           |                                                                                       |
| [nsmallest()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.nsmallest.html)                         |                                                                                       |
| [sum()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sum.html)                                     |                                                                                       |
| [mean()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.mean.html)                                   |                                                                                       |
| [median()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.median.html)                               |                                                                                       |
| [mode()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.mode.html)                                   |                                                                                       |
| std()                                                                                                               |                                                                                       |
| var()                                                                                                               |                                                                                       |
| [set_index()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.set_index.html)                         |                                                                                       |
| [reset_index()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.reset_index.html)                     |                                                                                       |
| [select_dtypes()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.select_dtypes.html)                 |                                                                                       |
| [rename()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.rename.html)                               |                                                                                       |
| [info()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.info.html)                                   |                                                                                       |
| [astype()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.astype.html)                               |                                                                                       |
| [isin()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.isin.html)                                   |                                                                                       |
| dropna()                                                                                                            |                                                                                       |
| [duplicated()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.duplicated.html)                       |                                                                                       |
| drop_duplicates()                                                                                                   |                                                                                       |
| replace()                                                                                                           |                                                                                       |
| [drop()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.drop.html)                                   |                                                                                       |
| [xs()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.xs.html)                         |                                                                                       |
| [reorder_levels()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.reorder_levels.html) |                                                                                       |


# Series

| methods                                                                                                    |                                    attributes                                    |
|:-----------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------:|
| [between()](https://pandas.pydata.org/docs/reference/api/pandas.Series.between.html)                       | [values](https://pandas.pydata.org/docs/reference/api/pandas.Series.values.html) |
| [str.replace()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.replace.html) |  [index](https://pandas.pydata.org/docs/reference/api/pandas.Series.index.html)  |
| [astype()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.astype.html)           |                                      dtype                                       |
| [mean()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.mean.html)               |                                       size                                       |
| [count()](https://pandas.pydata.org/docs/reference/api/pandas.Series.count.html)                           |                                      shape                                       |
| [sort_values()](https://pandas.pydata.org/docs/reference/api/pandas.Series.sort_values.html)               |                                    is_unique                                     |
| [head()](https://pandas.pydata.org/docs/reference/api/pandas.Series.head.html)                             |                             is_monotonic_decreasing                              |
| [tail()](https://pandas.pydata.org/docs/reference/api/pandas.Series.tail.html)                             |                             is_monotonic_increasing                              |
| [sum()](https://pandas.pydata.org/docs/reference/api/pandas.Series.sum.html)                               |                                                                                  |
| prod()                                                                                                     |                                                                                  |
| [cumsum()](https://pandas.pydata.org/docs/reference/api/pandas.Series.cumsum.html)                         |                                                                                  |
| [pct_change()](https://pandas.pydata.org/docs/reference/api/pandas.Series.pct_change.html)                 |                                                                                  |
| [median()](https://pandas.pydata.org/docs/reference/api/pandas.Series.median.html)                         |                                                                                  |
| [std()](https://pandas.pydata.org/docs/reference/api/pandas.Series.std.html)                               |                                                                                  |
| [max()](https://pandas.pydata.org/docs/reference/api/pandas.Series.max.html)                               |                                                                                  |
| min()                                                                                                      |                                                                                  |
| [describe()](https://pandas.pydata.org/docs/reference/api/pandas.Series.describe.html)                     |                                                                                  |
| [sample()](https://pandas.pydata.org/docs/reference/api/pandas.Series.sample.html)                         |                                                                                  |
| [unique()](https://pandas.pydata.org/docs/reference/api/pandas.Series.unique.html)                         |                                                                                  |
| [nunique()](https://pandas.pydata.org/docs/reference/api/pandas.Series.nunique.html)                       |                                                                                  |
| [add()](https://pandas.pydata.org/docs/reference/api/pandas.Series.add.html)                               |                                                                                  |
| sub() subtract()                                                                                           |                                                                                  |
| mul() multiply()                                                                                           |                                                                                  |
| div() divide()                                                                                             |                                                                                  |
| [floordiv()](https://pandas.pydata.org/docs/reference/api/pandas.Series.floordiv.html)                     |                                                                                  |
| [mod()](https://pandas.pydata.org/docs/reference/api/pandas.Series.mod.html)                               |                                                                                  |
| [eq()](https://pandas.pydata.org/docs/reference/api/pandas.Series.eq.html)                                 |                                                                                  |
| [ne()](https://pandas.pydata.org/docs/reference/api/pandas.Series.ne.html)                                 |                                                                                  |
| [dropna()](https://pandas.pydata.org/docs/reference/api/pandas.Series.dropna.html)                         |                                                                                  |
| [sort_index()](https://pandas.pydata.org/docs/reference/api/pandas.Series.sort_index.html)                 |                                                                                  |
| [nlargest()](https://pandas.pydata.org/docs/reference/api/pandas.Series.nlargest.html)                     |                                                                                  |
| [nsmallest()](https://pandas.pydata.org/docs/reference/api/pandas.Series.nsmallest.html)                   |                                                                                  |
| [value_counts()](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html)             |                                                                                  |
| [round()](https://pandas.pydata.org/docs/reference/api/pandas.Series.round.html)                           |                                                                                  |
| [apply()](https://pandas.pydata.org/docs/reference/api/pandas.Series.apply.html)                           |                                                                                  |
| [isnull()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.isnull.html)                      |                                                                                  |
| notnull()                                                                                                  |                                                                                  |
| [str.contains()](https://pandas.pydata.org/docs/reference/api/pandas.Series.str.contains.html)             |                                                                                  |
| str.len()                                                                                                  |                                                                                  |
| [str.split()](https://pandas.pydata.org/docs/reference/api/pandas.Series.str.split.html)                   |                                                                                  |
| [str.get()](https://pandas.pydata.org/docs/reference/api/pandas.Series.str.get.html)                       |                                                                                  |
| [str.replace()](https://pandas.pydata.org/docs/reference/api/pandas.Series.str.replace.html)               |                                                                                  |



# Index

| Method                                                                                        | Attribute |
|-----------------------------------------------------------------------------------------------|-----------|
| [value_counts()](https://pandas.pydata.org/docs/reference/api/pandas.Index.value_counts.html) |           |
| get_level_values()                                                                            |           |


# MultiIndex

| Method                                                                                                       | Attribute |
|--------------------------------------------------------------------------------------------------------------|-----------|
| `classmethod` [from_tuples()](https://pandas.pydata.org/docs/reference/api/pandas.MultiIndex.from_tuples.html) | index     |
|                                                                                                              | columns   |
|                                                                                                              | names     |
