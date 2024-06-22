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
3. 

# Useful information

* We can't use sets to create Series. If we have sets, we have to convert to another type, like a list
* Numpy is a dependency of Pandas. Some objects are built into Numpy objects
* Most mathematical methods ignore missing values by default. We can pass an argument False to the `skipna` parameter for the inclusion of nan values
* We can perform operations with +, -, *, /, //, %, ==, != in a Series object. The behavior is element-wise and **the operation is performed by labels. Pandas align shared index to perform operations**
* Also, we can work thr arithmetic operator with methods: `add()`, `substrac()`, `multiply()`, `div()`, `floordiv()`...
* Series values are stored in a numpy ndarray under the hood
* Broadcasting: 
* We can a Series to any Python's built-in function

# General Functions

* read_csv() -> DataFrame
* `class` `constructor` [Series()](https://pandas.pydata.org/docs/reference/api/pandas.Series.html) -> Series

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

| methods        | attributes |
|:---------------|:----------:|
| head()         |   shape    |
| tails()        |    size    |
| sort_values()  |   dtypes   |
| sort_index()   |   iloc[]   |
| value_counts() |   loc[]    |
|                |   index    |


# Series

| methods                                                                                                    |                                    attributes                                    |
|:-----------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------:|
| between()                                                                                                  | [values](https://pandas.pydata.org/docs/reference/api/pandas.Series.values.html) |
| [str.replace()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.replace.html) |  [index](https://pandas.pydata.org/docs/reference/api/pandas.Series.index.html)  |
| [astype()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.astype.html)           |                                      dtype                                       |
| [mean()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.mean.html)               |                                       size                                       |
| [count()](https://pandas.pydata.org/docs/reference/api/pandas.Series.count.html)                           |                                      shape                                       |
| sort_values()                                                                                              |                                    is_unique                                     |
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
|                                                                                                            |                                                                                  |