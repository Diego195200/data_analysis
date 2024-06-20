# Questions didn't answer yet

1. What is the best when using pandas, key-word argument or positional?


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
* 

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
| count()                                                                                                    |                                      shape                                       |
| sort_values()                                                                                              |                                    is_unique                                     |
|                                                                                                            |                             is_monotonic_decreasing                              |
|                                                                                                            |                             is_monotonic_increasing                              |