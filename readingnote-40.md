# Reading 12 - Pandas

## Pandas in 10

### Pandas

1. **Import pandas as pd**
2. then create *series* by passing a list of values. It creates an integer index
  ie. s = pd.series([1, 3, 5, np.nan, 6, 8])
  output:
    0   1.0
    1   3.0
    2   5.0
    3   NaN
    4   6.0
    5   8.0
    dtype:float64

### Data Frame

Create a DataFrame by:

1. passing *NumPy* array with labeled *columns* and *index*.

  ie. passing dictionary of objects to create a chart
    df2 = pd.DataFrame(
      {
          "A": 1.0,
          "B": pd.Timestamp("20130102"),
          "C": pd.Series(1, index=list(range(4)), dtype="float32"),
          "D": np.array([3] * 4, dtype="int32"),
          "E": pd.Categorical(["test", "train", "test", "train"]),
          "F": "foo",
      }
  )

  df2
  Out[10]:
      A          B    C  D      E    F
  0  1.0 2013-01-02  1.0  3   test  foo
  1  1.0 2013-01-02  1.0  3  train  foo
  2  1.0 2013-01-02  1.0  3   test  foo
  3  1.0 2013-01-02  1.0  3  train  foo

**DataFrame.to_numpy()** - NumPy physicality of data.
*note* expensive in terms of memory

*Panda* vs *NumPy*
-*NumPy* arrays have one dtype per entire array
-*pandas* have one dtype per column.

In Pandas, multiple dtypes will take alot of memory

*note* df.to_numpy() doesn't include index or column labels in output.

**.describe()** - shows summary of data

**.T()** - transpose data

**.sort_index()** - sort by axis
  ie .sort_index(axis = 1, ascending = False)

**.sort_values()** - sort by values

**df["A"]** - selects column (selects all of column A)

**df[num: number]**- slices row

### Selection by Label

**df.loc[dates[num]]** - cross section using label

### Selection by Position

**df.iloc[]** - select via the position

### Boolean Indexing

**df[df["A"] > 0]** - single columns value to select data

**.isin()** - filters DataFrame

### Missing Data

**np.nan** - represents missing data

**.dropna(how = "any")** - drop rows that are missing data

**.fillna()** - fills missing data

**.isna(df1)** - boolean where values are nan

### Operations

**df.mean()** - initiates descriptive statistic

### Apply

**.apply(np.cumsum)** - apply function to data

### Histogramming

?? 

### Merge

**.concat()** - *concatenating* panda objects together

### Join

**.merge()** - merges two DataFrame objects together

### Grouping

1. **Splitting** - *split* data into groups that meet conditions

2. **Applying** - *apply* function to each group

3. **Combining** - *combine* results into data structure.

### Time Series

pd.date_range("date", periods= num, freq="") - setting up the date rage

**ts.tz_localize("UTC")** - time zone representation (UTC representation)

**ts_utc.tz_convert("US/Eastern")** - convert to another time zone (US/Eastern)

### Categorical

**df["grade"] = df["raw_grade"].astype("category")** - converts raw grades to data type categorical

**Series.cat.categories()** - rename categories to more meaningful names

**Series.cat()** - return new series by default

### Plotting

**close()** - close a figure window

**plot()** plot all columns with labels

### Getting Data In/Out

**.to_csv()** - write to csv file

**.read_csv()** - read from csv file

[<==BACK](README.md)
