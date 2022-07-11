# WikiDes = Wiki Description
A novel dataset for generating descriptions of Wikidata from Wikipedia paragraphs.

# Dataset 

The data contain over 80k examples in the file **collected_data.json**.  There are 2 phases of training, description generation and candidate ranking. 

## Phrase 1. Description generation 
We consider Wikidata instances as topics of examples. The data distribution is training set ~ 80%, validation set ~ 10%, and test set ~ 10%. We use first 256 tokens in Wikipedia first paragraphs as the documents in the training.
* diff: The data is splitted by different topics. The training set will have different topics from validation and test sets. The distribution of training, validation, and test sets is 65,772/7,820/7,827.
* random: The data is split into random topics. The sets will have random topics. The distribution of training, validation, and test sets is 68,296/8,540/8,542.  Note that we did not filter empty Wikidata instances in this splitting.

## Phrase 2. Candidate ranking
Similar to Phase 1, there are 2 groups of datasets by 2 ways of data splitting, different topic splitting and random topic splitting. The data distribution is training set ~ 75% (6000 examples), validation set ~ 12.5% (1000 examples), and test set ~ 12.5% (1000 examples).

## Examples

Phase 1's examples:
```
{"wikidata_id": "Q55135146", "label": "Xyleborus intrusus", "source": "Xyleborus intrusus is a species of typical bark beetle in the family Curculionidae. It is found in North America.", "target": "species of insect", "baseline_candidates": ["taxon"]}

{"wikidata_id": "Q21000782", "label": "Konstantinos Stivachtis", "source": "Konstantinos Stivachtis (Greek: Κωνσταντίνος Στιβαχτής, born 22 May 1980) is a Greek male volleyball player. He is part of the Greece men's national volleyball team. On club level he plays for Olympiacos.", "target": "Greek volleyball player", "baseline_candidates": ["human"]}
```

Phase 2's examples:
```
{"source": "Knuthenborg Safaripark is a safari park on the island of Lolland in the southeast of Denmark. It is located 7 km (on Rte 289) to the north of Maribo, near Bandholm. It is one of Lolland's major tourist attractions with over 250,000 visitors annually, and is the largest safari park in northern Europe. It is also the largest natural playground for both children and adults in Denmark. Among others, it houses an arboretum, aviaries, a drive-through safari park, a monkey forest (with baboons, tamarins and lemurs) and a tiger enclosure. Knuthenborg covers a total of 660 hectares (1,600 acres), including the 400-hectare (990-acre) Safaripark. The park is viewable on Google Street View.", "candidate": ["park in Lolland, Denmark", "safari park"], "target": "Safari park in Denmark"}

{"source": "March 2015 was the third month of that common year. The month, which began on a Sunday, ended on a Tuesday after 31 days.", "candidate": ["third month of that common year", "calendar month of a given year", "month starting on Sunday", "March"], "target": "month of 2015"}
```

# Publication
In process of writing the report paper...

# Contact
We are from CIC IPN and DeCLaRe Lab (https://declare-lab.net/). If you have any question, contact to: Hoang Thang Ta, tahoangthang@gmail.com
