# Questions didn't answer yet

1. What is the best when using pandas, key-word argument or positional?
2. I don't know what is the correct name in the Series method: product or prod
3. View all functionalities of `describe()` method

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


# Useful information

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


# General Functions

* read_csv() -> DataFrame
* `class` `constructor` [Series()](https://pandas.pydata.org/docs/reference/api/pandas.Series.html) -> Series


# Types of values

* Object: 
* NaN: Not a Number
* NaT: Not a Time

# Syntax and notation

```
criteria = DataFrame['name'] == 'row_value'
DataFrame[criteria]  # -> Series (if just one name), DF with more than one name
```

Here we use `&`, `|` for logic operations

We can apply a specific core python method to pandas' objects, 
and it will be applied for each element of the object
like the following example: `object.index.str.lower()`
These are known as the "accessors" and the "mutators"


# Built in functions, operators

| Built-in | operators |
|----------|-----------|
| len()    | in        |
| type()   |           |
| dir()    |           |
| list()   |           |
| dict()   |           |



# DataFrame

| methods                                                                                 | attributes |
|:----------------------------------------------------------------------------------------|:----------:|
| head()                                                                                  |   shape    |
| tails()                                                                                 |    size    |
| sort_values()                                                                           |   dtypes   |
| sort_index()                                                                            |   iloc[]   |
| value_counts()                                                                          |   loc[]    |
| [squeeze()](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.squeeze.html) |   index    |


# Series

| methods                                                                                                    |                                    attributes                                    |
|:-----------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------:|
| between()                                                                                                  | [values](https://pandas.pydata.org/docs/reference/api/pandas.Series.values.html) |
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
| [apply()](https://pandas.pydata.org/docs/reference/api/pandas.Series.apply.html)                                                                                                    |                                                                                  |



# Index

| Method                                                                                        | Attribute |
|-----------------------------------------------------------------------------------------------|-----------|
| [value_counts()](https://pandas.pydata.org/docs/reference/api/pandas.Index.value_counts.html) |           |
|                                                                                               |           |
