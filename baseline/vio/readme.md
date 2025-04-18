# Baseline system - Violence 

The **Large Language Model Qwen2.5**, with 32 billion parameters, was used as the baseline for violence detection (Yang et al., 2024). The LLM was tasked with binary classification of tweets in a few-shot scenario. The LLM was assigned the role of a filter system specialised in detecting harmful content on social media via a system prompt. It was also provided with a definition of ‘call to definition’ that was essentially the same as the one given to the annotators. The examples required for in-context learning are the same as those available on the website and presented to the annotators. The script is intended for LLMs running locally with Ollama. 

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

- Yang, A., Yang, B., Zhang, B., Hui, B., Zheng, B., Yu, B., Li, C., Liu, D., Huang, F., Wei, H., Lin, H., Yang, J., Tu, J., Zhang, J., Yang, J., Yang, J., Zhou, J., Lin, J., Dang, K., … Qiu, Z. (2024, September). Qwen2.5 Technical Report. https://qwenlm.github.io/blog/qwen2.5/
