# Delta Lake

## Installation

You can enjoy Delta Lake with PySpark or without a Spark dependency too.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/007-powers-install-delta-lake.png" width="700" />

You can install Delta Lake and PySpark with conda as follows.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/017-install-delta-spark-conda.png" width="700" />

## Basic features

You can easily time travel to read different versions of your Delta table with #deltalake. This example shows a Delta table with three versions. The latest version is read by default, but you can also easily time-travel back to version 1 of the Delta table.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/011-powers-time-travel.png" width="700" />

You can easily append a #pandas DataFrame to an existing Delta table with #deltalake.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/002-powers-append-pandas.png" width="700" />

It's so easy to convert from #parquet to #deltalake - just one line of code.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/003-powers-convert-parquet-to-delta.png" width="700" />

There are a variety of ways to create #deltalake tables. You can create a Delta table by writing out a DataFrame with the Delta format, you can create an empty Delta table with #sql, or you can convert an existing Parquet table to the Delta format. Very easy to jump in and start using Delta Lake.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/015-powers-three-ways-to-create-delta-tables.png" width="700" />

You can add constraints to your #deltalake that prevent certain values from getting appended. You can add NOT NULL constraints that prohibit null values and custom constraints with boolean checks. Constraints are a great way to keep your Delta tables clean.


<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/005-powers-delta-constraints.png" width="700" />

Lots of folks are under the misguided impression that switching to Delta Lake is a big change. For many organizations, it's trivially easy. You can oftentimes just change a few lines of code to switch from #parquet to #deltalake.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/001-powers-adopt-delta.png" width="700" />

Delta Lake prevents you from appending data with mismatched schema by default. If your Delta table has c1, c2, and c3 columns, you can't append a DataFrame with c1, c2, and c5 columns. You need to specifically enable schema evolution if that's what you want. Schema enforcement is the default.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/010-powers-schema-enforcement.png" width="700" />

Delta Lake is a protocol that can be implemented in any programming language. There is currently an implementation in Scala and another implementation in Rust. Each implementation can expose different language bindings (e.g. the Rust implementation exposes #rust & #python user APIs).

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/009-powers-protocol-langauge-agnostic.png" width="700" />

You can create #deltalake tables that are simply persisted in storage (non-registered) or Delta table that also have a corresponding entry in the Hive metastore (managed tables).

Managed tables are great if you'd like to easily query the data with SQL syntax. Non-registered tables are better if you're just using the DataFrame API and don't want to depend on #hive. See these #pyspark examples.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/016-powers-managed-non-registered-delta-tables.png" width="700" />

## Merge

You can use a #deltalake merge to append to a Delta table without adding any duplicates. This is important if you want to maintain the uniqueness of a column in your Delta table.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/014-powers-delta-merge-append-without-duplicates.png" width="700" />

## Delete

Deleting rows from a Parquet data lake is complicated, dangerous, and requires table downtime. Deleting rows from a Delta Lake is safe, fast, and easy.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/delta-lake/004-powers-deleting-rows-delta.png" width="700" />

## Connectors

reading Delta Lake tables with Polars

You can easily read a #deltalake table into a #polars DataFrame. The following image shows how to read version 0 of a Delta table with three versions into a Polars DataFrame. Reading different versions is easy. Thanks for getting this added Chitral Verma and Ritchie Vink.

TODO: Find image :|

## Other



