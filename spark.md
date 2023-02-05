# Apache Spark

You can easily package up a PySpark project into a wheel file to deploy it in production.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/001-powers-deploying-poetry.png" width="700" />

PySpark User Defined Functions (UDFs) cannot be optimized by Spark and require you to explicitly handle the null / None edge case. You can oftentimes use built-in Spark functions for the same functionality. Here's an example of an unnecessary UDF.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/009-avoid-udfs.png" width="700" />

You can make a few easy tweaks to speed up your Spark test suite by 70% or more. Lowering the number of shuffle partitions, limiting I/O, and reusing the SparkSession will dramatically improve #apachespark test suite runtimes.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/007-powers-speed-spark-tests.png" width="700" />

Spark is extensible and you can write your own Spark native functions that leverage the Catalyst optimizer, just like built-in Spark functions. The yaooqinn/itachi project uses this design pattern to expose Postgres syntax for Spark users.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/003-powers-postgres-syntax-with-spark.png" width="700" />

PySpark's fluent interfaces let you write beautiful, legible code.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/004-powers-pyspark-beautiful-api.png" width="700" />

Make sure you set mergeSchema to true when reading Parquet files with different schemas into a PySpark DataFrame.  Otherwise, you won't read in all the columns, which probably isn't what you want.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/spark/005-powers-pyspark-mergeschema.png" width="700" />

