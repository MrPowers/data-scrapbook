# Quinn

Quinn contains a collection of PySpark helper methods.

You can use quinn to validate the presence of columns in a PySpark DataFrame.  You may want to validate the columns in your DataFrame before appending to a Parquet data lake for example.  These types of checks aren't necessary with Delta Lake because it supports built-in schema enforcement.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/001-quinn-validate-presence-of-columns.png" width="700" />

