# **Pandas For Python**

_Day 12 - Tuesday, Jun. 28th. 2022_

## **What kind of data does pandas handle?**

**First of all**, to **load the pandas package** and start working with it, import the package. The community agreed _alias_ for pandas is `pd`, so loading pandas as `pd` is assumed standard practice for all of the pandas documentation.

        import pandas as pd

To **manually store data in a table**, create a `DataFrame`. When using a Python dictionary of lists, the _dictionary keys will be used as column headers_ and the values in each list as columns of the DataFrame.

 A **`DataFrame`** is a _2-dimensional data structure that can store data of different types_ (including characters, integers, floating point values, categorical data and more) in columns. It is similar to a `spreadsheet`, a `SQL table` or the `data.frame` in R. [1]

### **_Each column in a DataFrame is a Series_**

When selecting a single column of a pandas DataFrame, the result is a pandas Series. To select the column, use the column label in between square brackets

> If you are familiar to Python dictionaries, the selection of a single column is very similar to selection of dictionary values based on the key. [1]

### **_A pandas Series has no column labels, as it is just a single column of a DataFrame. A Series does have row labels._**

You can do things with a DataFrame or Series. pandas provides a lot of functionalities, each of them a method you can apply to a DataFrame or Series. As methods are functions, do not forget to use parentheses `()`. [1]

The `describe()` method provides a quick overview of the numerical data in a _DataFrame_. Many pandas operations return a DataFrame or a Series. The `describe()` method is an example of a pandas operation returning a _pandas Series_ or a _pandas DataFrame_.


## **Notes**

- Import the package, aka `import` `pandas` `as` `pd`

- A table of data is stored as a pandas `DataFrame`

- Each column in a `DataFrame` is a `Series`

- You can do things by applying a method to a `DataFrame` or `Series`.

- Getting data in to pandas from many different file formats or data sources is supported by `read_*` functions.

- Exporting data out of pandas is provided by different `to_*` methods.

- The `head/tail/info` methods and the `dtypes` attribute are convenient for a first check.

- When selecting subsets of data, square brackets `[]` are used.

- Inside these brackets, you can use a single column/row label, a list of column/row labels, a slice of labels, a conditional expression or a colon.

- Select specific rows and/or columns using `loc` when using the row and column names.

- Select specific rows and/or columns using `iloc` when using the positions in the table

- You can assign new values to a selection based on `loc/iloc`.

- String methods are available using the `str` accessor.

- String methods work element-wise and can be used for conditional indexing.

- The `replace` method is a convenient method to convert values according to a given **dictionary**.

- Valid date strings can be converted to datetime objects using `to_datetime` function or as part of read functions.

- Datetime objects in pandas support calculations, logical operations and convenient date-related properties using the `dt` accessor.

- A `DatetimeIndex` contains these date-related properties and supports convenient slicing.

- `Resample` is a powerful method to change the frequency of a time series.

- The `.plot.*` methods are applicable on both Series and DataFrames.

- By default, each of the columns is plotted as a different element (line, boxplot,…).

- Any plot created by pandas is a Matplotlib object.














### Check this [tutorial](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html) to have a better idea about the _**how to**s_ of using banda as a beginner



## Things I want to know more about:
1. NumPY.
2. Pandas.
3. Statisticss.




[1]: https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/01_table_oriented.html

[2]: 