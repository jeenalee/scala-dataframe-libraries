# Exploration of Data Frame Libraries for Scala

Our main purpose of using a data frame library would be matrix manipulations rather than doing math (like pandas rather than numpy in Python).

## [Breeze] (https://github.com/scalanlp/breeze/)
Breeze aims to be the `Numpy` for Scala. Selecting columns/rows, transposing matrices, joining and slicing matrices and vectors seem simple. Great documentation. Their [cheat sheet] (https://github.com/scalanlp/breeze/wiki/Linear-Algebra-Cheat-Sheet) offer a list of `breeze`, `matlab`, `numpy`, and `R` commands. Breeze supports csv io.

## [Spark] (http://spark.apache.org/docs/latest/sql-programming-guide.html)
Spark has updated their data frames API. While its default data type is `parquet`, it also supports json io. It supports slicing and joining data frames, but does not support basic linear algebra functions, such as transpose or inverse. It can be easily integrated into Spark's distributed computing and machine learning, which is another benefit.

## [Saddle] (https://saddle.github.io/)
Saddle is strongly influenced by `Pandas`. For a column to have more than one type, it requires extra effort. It supports basic lienar algebra functions like transposing and joining/slicing frames. It does not have a well written documentation.

## [Scala-Dataable] (https://github.com/martincooper/scala-datatable)
Inspired by immutable data structures. It is a light-weight data frame library, compared to others. It requires the user to specify type for each column/row. It does not support csv io.

## [Distributed DataFrame for Java] (http://ddf.io/)
DDF supports Java, Python, and R. Its syntax is very similar to R, and it claims it can do most things R does. Its main goal is to provide simple API for big-data, and offers easy integration into Spark or Hadoop MapReduce. It isn't clear from the documentation whether DDF offers linear algebra functions or easy data selection.
