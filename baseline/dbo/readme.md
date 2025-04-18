# Baseline system - Attacks on the Basic Democratic Order

A **gradient-boosting classifier** was trained as the baseline system. The system is based on two features: sentence embeddings created with SentenceBert (Reimers & Gurevych, 2019) and the polarity of the tweets, which was determined using a lexicon-based approach with the TextBlob programme (Loria, 2025). 

The Jupyter notebook `dbo_baseline.ipynb` contains the code for training the model and for making predictions on unseen data.

## Results 

The system achieved the following metrics on the test data, with the Macro-F1 metric being decisive for the ranking on the leaderboard:

| Category      |   P  |   R  |  F1  |
| ------------- | ---- | ---- |  -:  |
| agitation     | 0.07 | 0.01 | 0.02 |
| criticism     | 0.59 | 0.29 | 0.39 |
| nothing       | 0.87 | 0.97 | 0.92 |
| subversive    | 0.00 | 0.00 | 0.00 |
| **Mac. avg.** | **0.38** | **0.32** | **0.33** |
| **Weight. avg.** | 0.80 | 0.85 | 0.82 |

</div>

## References

- Loria, S. (2025). Sloria/TextBlob (Version 0.7.0) [Python]. https://github.com/sloria/TextBlob (Original work published 2013)
- Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence embeddings using siamese BERT-networks. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), 3982–3992. https://doi.org/10.18653/v1/D19-1410
