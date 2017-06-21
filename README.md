## About

The file sw1k.csv contains most frequent 1,000 words and phrases occurred in more than 1.53 million news articles from 200+ sources collected over the span of a 2.5 years. 

Similarily sw10k.csv and sw100k.csv contain 10,000 and 100,000 terms respectively.

## Structure of the files

Each CSV file contains 5 columns:


*term*: the actual word or phrase


*frequency*: how many times a term has occured in all the documents


*presence*: in how many documents the term has occurred, note that frequence >= presence


*doc_size_sum*: sum of the size of the documents in which the term has occurred, 

> doc_size(d) = number of characters present in the doc d including whitespace


type: type of the term, N: Noun, NP: Noun Phrase, PN: Proper Noun, G: Other

*types PERSON, PLACE, ORGANIZATION are self explanatory*

Libs Sanford CoreNLP and OpenNLP were used to split the docs in sentences, NER and POS tagging


## Notes
1. The dataset is not manually processed, so you might see some unusual terms such as some common emails, news site names, editor/author names etc. These can be easily filtered by keeping the words with higher ***frequency/presence*** ratio. 

2. The dataset includes all type of frequent terms like proper nouns, places, orgs etc. One can filter these using the *type* column. 
