# WikiDes = Wiki Description
A novel dataset for generating descriptions of Wikidata from Wikipedia paragraphs.

# Dataset 

The data contain over 80k examples in the file collected_data.json.  There are 2 phases of training, description generation and candidate ranking. 

## Phrase 1. Description generation 
We consider Wikidata instances as topics of examples. The data distribution is training set ~ 80%, validation set ~ 10%, and test set ~ 10%.
* diff: The data is splitted by different topics. The training set will have different topics from validation and test sets.
* random: The data is splitred by random topics. The sets will have random topics.

## Phrase 2. Candidate ranking
Similar to Phase 1, there are 2 groups of datasets by 2 ways of data splitting, different topic splitting and random topic splitting. The data distribution is training set ~ 75%, validation set ~ 12.5%, and test set ~ 12.5%.


# Contact
We are from CIC IPN and DeCLaRe Lab (https://declare-lab.net/). If you have any question, contact to: Hoang Thang Ta, tahoangthang@gmail.com
