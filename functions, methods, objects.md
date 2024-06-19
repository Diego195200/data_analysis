# General Functions

* read_csv() -> DataFrame

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

| methods                                                                                                    | attributes |
|:-----------------------------------------------------------------------------------------------------------|:----------:|
| between()                                                                                                  |            |
| [str.replace()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.replace.html) |            |
| [astype()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.astype.html)           |            |
| [mean()](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.mean.html)               |            |
| count()                                                                                                    |            |
