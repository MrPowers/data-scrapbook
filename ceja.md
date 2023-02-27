# ceja

## Phonetic algorithms

### NYSIIS

The New York State Identification and Intelligence System (NYSIIS) phonetic algorithm is similar to the soundex algorithm (which is built-in to Spark), but 2.7% more accurate.  It can be used to determine if two words sound the same.  For example, "there" and "their" have the same NYSIIS encoding.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/ceja/001-ceja-nysiis.png" width="700" />

### Metaphone

The metaphone phonetic algorithm is an improvement to soundex and codifies words based on their English pronunciation.  You can use PySpark and ceja to run the metaphone algorithm on large datasets with parallel processing.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/ceja/002-ceja-metaphone.png" width="700" />

### Match rating codex

TODO

## Stemming algorithms

### Porter stem

The Porter stem algorithm is used to remove common English word endings and get the "stem" of a word.  For example, the stem of "washed" and "washing" is "wash".  Let's see how ceja allows you to run the Porter stem algorithm on a large dataset in parallel with PySpark.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/ceja/003-porter-stem.png" width="700" />

## Similarity algorithms

### Damerau Levenshtein Distance

The Levenshtein distance measure the differences between two strings.  "The Damerau–Levenshtein distance differs from the classical Levenshtein distance by including transpositions among its allowable operations in addition to the three classical single-character edit operations".  PySpark has a built-in Levenshtein function.  You can access the Damerau Levenshtein algorithm with the ceja library.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/ceja/004-damerau-levenshtein.png" width="700" />

### Hamming distance



### Jaro similarity



### Jaro Winkler similarity




### Match rating comparison



## Scaling jellyfish with PySpark

A lot of Python libraries can be scaled to run on large datasets with PySpark.  Take the jellyfish library for approximate and phonetic matching of strings as an example.  jellyfish defines algorithms like how to compute the Hamming Distance between two strings.  PySpark makes it easy to run the jellyfish Hamming Distance algorithm on a big dataset in parallel.

<img src="https://github.com/MrPowers/data-scrapbook/blob/main/images/ceja/001-ceja-nysiis.png" width="700" />

