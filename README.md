# Text-Conversion-without-packages
Required to write Python code to preprocess a set of unit information and convert them into numerical representations 
(which are suitable for input into recommender-systems/ information-retrieval algorithms).

The data-set contains 400 unit information crawled from Monash University.
It contains a table in which each row contains
information about a unit which is unit code, synopsis, and requirements. Code is to extract
and transform the information for each unit into a vector space model considering the following
rules:
Generating sparse representations for the unit information
i.e. build sparse representations for the unit information, which includes
word tokenization, vocabulary generation, and the generation of sparse representations.

The following tasks have been performed 
1. The word tokenization using the regular expression, "\w+(?:[-']\w+)?"
2. The context-independent and context-dependent (with the threshold set to %95) stop
words have been removed from the vocab. 
3. Tokens have been stemmed using the Porter stemmer.
4. Rare tokens (with the threshold set to %5) have been removed from the vocab.
5. Tokens have been normalized to lowercase except the capital tokens appeared in the
middle of a sentence/line.
6. Tokens with the length less than 3 have been removed from the vocab.
7. First 200 meaningful bigrams (i.e., collocations) have been included in the vocab using
PMI measure.
