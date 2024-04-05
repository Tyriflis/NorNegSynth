# NorNegSynth


NorNegSynth is a synthetic dataset, made by manually adding negating expression the the existing Norwegian NoReC fine dataset (Øvrelid et al.).

The main findings are presented in the paper _A Diagnostic Dataset for Sentiment and Negation Modeling for Norwegian_ (Mæhlum et al, 2023). This work in this paper is based on the Master thesis published the same year: _Exploring the Effect of Negation on Sentiment in Norwegian_ (Mæhlum, 2023).

In this repository you will find the dataset, which can be used to evaluate models for Norwegian sentiment.

The core objective of the dataset is this: To be able to compare how negation is handled in models for SA, by having several minimal pairs, i.e. pairs of sentences where the only difference is the added or removed negation expression.

## Core Limitations

Not all negations are represented equally, and care should be made when drawing conclusions from the less frequent examples.

Beware that types of negation can vary with domains, and thus the scores from this dataset cannot necessarily be used to say something about how well a model would do for negation in for example the medical domain.



## Code and Data

nornegsynth.json is the file containing the parallell data.

The format is similar to that of NoReC fine, but the IDs are updated to reflect the pairs.

There is an additional META label which conains the attribute Artificial, which can be False or True. This refers to whether the pair is originally in NoReC fine, or if it is a new addition.

Letters are used to indicate newly added pairs. The original sentences have no additional letter, while negated sentences (or sentenced with negation removed) have a letter appended to their ID, as in the sentences below, where there is one original sentence, and two new additions. 

```
"sent_id": "201344-02-01",
"text": "Garmin Fenix Chronos er meget god tur- og treningskamerat , og mye flottere enn vanlige smartklokker .",

"sent_id": "201344-02-01-a"
"text": "Garmin Fenix Chronos er ikke meget god tur- og treningskamerat , og mye flottere enn vanlige smartklokker .",

"sent_id": "201344-02-01-b",
"text": "Garmin Fenix Chronos er ikke meget god tur- og treningskamerat , men mye flottere enn vanlige smartklokker .",
```

In these examples, the sentence with the added letter "-a" has an "ikke" (not) added, and the sentence with "-b" added has an additional change in having "og" being changed to "men" to better reflect the changes in polarity.

## Urls

Paper: 
[https://aclanthology.org/2023.resourceful-1.11.pdf](https://aclanthology.org/2023.resourceful-1.11/)

NoReC fine:
https://aclanthology.org/2020.lrec-1.618/

Thesis:
https://www.duo.uio.no/handle/10852/107605

## Acknowledgement and distribution
If you use this dataset, please cite the RESOURCEFUL paper.

Petter Mæhlum, Erik Velldal, and Lilja Øvrelid. 2023. A Diagnostic Dataset for Sentiment and Negation Modeling for Norwegian. In Proceedings of the Second Workshop on Resources and Representations for Under-Resourced Languages and Domains (RESOURCEFUL-2023), pages 77–85, Tórshavn, the Faroe Islands. Association for Computational Linguistics.

(See more citation options on the paper website)
