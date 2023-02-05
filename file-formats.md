# File Formats

## CSV files

When reading #csv files, you have two bad options to figure out the schema. Manually specifying the schema is error prone (human error) and tedious for wide tables. Schema inference by query engines is error prone if subsets of data are used (could be wrong) and slow if the entire dataset is used.

Delta Lake stores the schema in the transaction log, so it can be fetched quickly and accurately.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/file-formats/002-csv-schema-inference-sucks.png" width="700" />

## Compaction

Too many small files cause queries to run slower than they should. You can easily bin pack small Parquet files into right-sized files with Delta Lake, so your queries run faster.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/file-formats/001-bin-pack-parquet.png" width="700" />

