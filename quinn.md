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

You can easily remove non-word characters from a PySpark string column using the quinn library.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/009-quinn-remove-non-word-characters.png" width="700" />

You can use quinn to convert a column of a PySpark DataFrame to a Python list, but watch out.  This collects all the data to the driver node and won't work for large datsets.  Make sure to filter the column to reduce the data size before running this method.  It's best to look for alternatives.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/010-quinn-column-to-list.png" width="700" />

You can use quinn to convert to columns of a PySpark DataFrame to a Python dictionary, but watch out.  This collects all the data in the two columns to the driver node.  This will cause the driver node to die with an out of memory exception if the dataset is too large.  Filter the data as much as possible before running this command.  It's best to look for alternatives.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/011-quinn-two-columns-to-dictionary.png" width="700" />

Here's how to convert the string that's output via the PySpark DataFrame show() method into a DataFrame.  You may want to do this if your coworker sends you a DataFrame via Slack or you're trying to convert a StackOverflow question into a working code snippet.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/quinn/012-quinn-show-output-to-df.png" width="700" />

