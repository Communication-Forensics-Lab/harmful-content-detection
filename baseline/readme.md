# Baseline systems

[//]: # ( A **Large Language Model** that performed the classification in a zero-shot setting was used as the baseline system for all subtasks. Qwen2.5 with a size of 32 B was selected as the model. In the results presented below, the Macro-F1 measure is the main evaluation measure. This is also used for the ranking in the leaderboard. In addition, we also report precision, recall and F1 measures for the individual classes.)

## Call to Action

A **gradient-boosting classifier** was trained as the baseline system, using sentence embeddings extracted from SentenceBert and the polarity of the tweet as features. Polarity was determined using a lexicon-based approach with the TextBlob programme. Undersampling was applied to address the high imbalance of the training dataset. 

| Category      | P  |  R | F1 |
| ------------- | -- | -- | -: |
| true          | -- | -- | -- |
| false         | -- | -- | -- |
| **Mac. avg.** | -- | -- | -- |

## Detection of attacks on the basic democratic order

## Violence Detection

The Large Language Model Qwen2.5, with 32 billion parameters, was used as the baseline for violence detection. The LLM was tasked with binary classification of tweets in a few-shot scenario. The LLM was assigned the role of a filter system specialised in detecting harmful content on social media via a system prompt. It was also provided with a definition of ‘call to definition’ that was essentially the same as the one given to the annotators. The examples required for in-context learning are the same as those available on the website and presented to the annotators. The script is intended for LLMs running locally with Ollama. 
