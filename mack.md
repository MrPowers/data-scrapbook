# Mack

## Deduplicate

Mack makes it easy to handle duplicate records in a Delta Table.

Let's imagine you have an event source that produces faulty events. Those events have a unique primary key, but you know that they are duplicate records on a semantic level. The following example shows how to use the `drop_duplicates_pkey` method to efficiently remove the records.

TODO: Ask Robert if image can be used

Mack makes it easy to append data to #deltalake tables without any duplicates. This saves you from having to deduplicate later. Big shout out to Souvik Pratiher for adding this feature.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/mack/008-powers-mack-append-without-duplicates.png" width="700" />

## Table metadata

It's easy to calculate the size of your Delta Lake table with the Mack helper methods. Thanks for adding this method Robert Kossendey.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/mack/013-powers-calculate-delta-table-size.png" width="700" />

## SCD

The mack library lets you perform Type 2 SCD upserts to #deltalake tables with a single line of code. Just run pip install mack and you can enjoy Delta Lake helper methods that make common data processing tasks easy.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/mack/012-powers-type-2-scd.png" width="700" />
