# Quinn

Quinn contains a collection of PySpark helper methods.

You can use quinn to validate the presence of columns in a PySpark DataFrame.  You may want to validate the columns in your DataFrame before appending to a Parquet data lake for example.  These types of checks aren't necessary with Delta Lake because it supports built-in schema enforcement.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/001-quinn-validate-presence-of-columns.png" width="700" />

You can use quinn to validate the schema of a PySpark DataFrame.  You may want to validate the schema of your DataFrame before appending more data to a CSV/Parquet table for example.  Schema checks aren't necessary with Delta Lake because it supports built-in schema enforcement.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/002-quinn-validate-schema.png" width="700" />

You can use quinn to validate the absence of columns in a PySpark DataFrame.  Suppose you're running a transformation that adds a column to a DataFrame.  You can use this function to validate that the column is missing before running the transformation.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/003-quinn-validate-absence-of-columns.png" width="700" />

You can use quinn to make sure the schema of the DataFrame you're appending matches the existing Parquet table schema.  These types of manual schema checks aren't necessary when you're using Delta Lake (because it has built-in schema enforcement), but are important when you're writing to Parquet tables.

TODO: Update quinn functionality (https://github.com/MrPowers/quinn/issues/51) and add image

You can create PySpark DataFrames with built-in methods, but they require really verbose syntax if you want to specify the schema exactly.  Quinn is a good alternative because it let's you specify the schema exactly with concise syntax.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/005-quinn-create-df.png" width="700" />

These snippets demonstrate how the built-in PySpark createDataFrame code requires verbose syntax when you're specifying the schema exactly.  Quinn let's you specify the schema and use concise syntax.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/006-quinn-create-df2.png" width="700" />

Quinn has a create_df function that extends the core pyspark.sql.SparkSession class.  The following image illustrates how to "monkey patch" a core PySpark class.  Note: this is almost always a bad programming practice / bad idea.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/007-quinn-create-df3.png" width="700" />

Quinn makes it easy to single space all the whitespace in a string.  This is great to fix strings with with inconsistent spacing.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/008-quinn-single-space.png" width="700" />

