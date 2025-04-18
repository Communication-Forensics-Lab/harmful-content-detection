# Baseline system - Violence 

The **Large Language Model Qwen2.5**, with 32 billion parameters, was used as the baseline for violence detection. The LLM was tasked with binary classification of tweets in a few-shot scenario. The LLM was assigned the role of a filter system specialised in detecting harmful content on social media via a system prompt. It was also provided with a definition of ‘call to definition’ that was essentially the same as the one given to the annotators. The examples required for in-context learning are the same as those available on the website and presented to the annotators. The script is intended for LLMs running locally with Ollama. 

A **gradient-boosting classifier** was trained as the baseline system, utilising sentence embeddings extracted from SentenceBert (Reimers & Gurevych, 2019) and the tweet's polarity as features. Polarity was determined using a lexicon-based approach with the TextBlob programme (Loria, 2025). Undersampling was applied to address the high imbalance of the training dataset. 

The notebook `vio_baseline.Rmd` contains the code for training the model and for making predictions on unseen data.

## Results 

The system achieved the following metrics on the test data, with the Macro-F1 metric being decisive for the ranking on the leaderboard. 

<div align="center">

[//]: # (| Category      |   P  |   R  |  F1  |
| ------------- | ---- | ---- |  -:  |
| true          | 0.23 | 0.78 | 0.36 |
| false         | 0.97 | 0.72 | 0.83 |
| **Mac. avg.** | 0.60 | 0.75 | 0.59 |
| **Weight. avg.** | 0.90 | 0.73 | 0.78 |)

</div>

## References

- Loria, S. (2025). Sloria/TextBlob (Version 0.7.0) [Python]. https://github.com/sloria/TextBlob (Original work published 2013)
- Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence embeddings using siamese BERT-networks. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), 3982–3992. https://doi.org/10.18653/v1/D19-1410
