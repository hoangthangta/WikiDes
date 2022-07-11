# WikiDes = Wiki Description
A novel dataset for generating descriptions of Wikidata from Wikipedia paragraphs.

# Dataset 

The data contain over 80k examples in the file "collected_data.json".  There are 2 phases of training, description generation and candidate ranking. 

## Phrase 1. Description generation 
We consider Wikidata instances as topics of examples. The data distribution is training set ~ 80%, validation set ~ 10%, and test set ~ 10%. We use first 256 tokens in Wikipedia first paragraphs as the documents in the training.
* diff: The data is splitted by different topics. The training set will have different topics from validation and test sets. The distribution of training, validation, and test sets is 65,772/7,820/7,827.
* random: The data is split into random topics. The sets will have random topics. The distribution of training, validation, and test sets is 68,296/8,540/8,542.  Note that we did not filter empty Wikidata instances in this splitting.

## Phrase 2. Candidate ranking
Similar to Phase 1, there are 2 groups of datasets by 2 ways of data splitting, different topic splitting and random topic splitting. The data distribution is training set ~ 75% (6000 examples), validation set ~ 12.5% (1000 examples), and test set ~ 12.5% (1000 examples).


# Publication
In process of writing the report paper...

# Contact
We are from CIC IPN and DeCLaRe Lab (https://declare-lab.net/). If you have any question, contact to: Hoang Thang Ta, tahoangthang@gmail.com
