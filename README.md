# WOLVES: Word List Vector for Sentiment

The **WOLVES** (Word List Vector for Sentiment) algorithm is an innovative sentiment analysis algorithm that combines manually defined lists of sentiment words with word embedding techniques to quantify the change in text sentiment over time.WOLVES dynamically updates the sentiment word list based on changing semantics and sentiment intensity, thus solving the problem of static sentiment analysis models. WOLVES can dynamically update the sentiment lexicon according to changing semantics and sentiment intensity, thus solving the limitations of static sentiment analysis models. In addition, WOLVES can help extract valuable business intelligence from financial texts, which provides powerful support for business decision-making.  
</br>
The official implementation of paper "[The Effects of Sentiment Evolution in Financial Texts: A Word Embedding Approach](https://onlinelibrary.wiley.com/doi/full/10.1111/poms.13959)". 


## Dataset Information

| Dataset                               | description                              |
|---------------------------------------|------------------------------------------|
| LM_positive                           |Positive words in the Loughran and McDonald dictionary|
| LM_negative                           |Negative words in the Loughran and McDonald dictionary|
| H4_positive                           |Positive words in the H4 dictionary|
| H4_negative                           |Negative words in the H4 dictionary|
| LoughranMcDonald_MasterDictionary_2020.csv |Loughran-McDonald Dictionary|
| mda_tf.csv                           |Sentiment words data in the Form 10Ks|
| index.csv                            |Index and year information for Form 10-Ks|





## Installation
### Clone the repository to your local machine:
```bash
git clone https://github.com/Mingze0111/MM_Test.git
```
### Dependencies
To install the required dependencies, please run the following command:
```bash
pip install -r requirements.txt
```

## Usage
### Key Functions:

```python

def get_year_bias_data_dict(model_dict, test_pos_words, test_neg_words, pos_benchmark_dict, neg_benchmark_dict,
                            similarity='cos', year_cols=None):
    """
    Calculate bias data and cluster data for a given word embedding model across different years.

    Parameters:
    - model_dict (dict): A dictionary containing word embedding models for different years.
    - test_pos_words (list): List of positive test words.
    - test_neg_words (list): List of negative test words.
    - pos_benchmark_dict (dict): A dictionary containing positive benchmark words for each year.
    - neg_benchmark_dict (dict): A dictionary containing negative benchmark words for each year.
    - similarity (str, optional): Similarity measure to be used ('cos' for cosine similarity or 'euc' for Euclidean distance). Defaults to 'cos'.
    - year_cols (list, optional): List of years to consider. Defaults to None.

    Returns:
    - mc_pos_cluster_data_pd (DataFrame): DataFrame containing cluster data for positive test words.
    - mc_neg_cluster_data_pd (DataFrame): DataFrame containing cluster data for negative test words.
    - mc_pos_bias_data_pd (DataFrame): DataFrame containing bias metrics for positive test words.
    - mc_neg_bias_data_pd (DataFrame): DataFrame containing bias metrics for negative test words.
    - average_distance_dict (dict): Dictionary containing average distances between positive and negative reference vectors for each year.
    """
```

The `get_year_bias_data_dict` function is designed to calculate bias metrics and cluster data for a given word embedding model across different years. This function leverages word embeddings to quantify semantic relationships between words and provides insights into how word meanings evolve over time.  
The function returns the results as DataFrames and dictionaries for further analysis and visualization.  
#### Example Usage:  
```python
pos_cluster_data, neg_cluster_data, pos_bias_data, neg_bias_data, avg_distances = get_year_bias_data_dict(model_dict, test_pos_words, test_neg_words, pos_benchmark_dict, neg_benchmark_dict, similarity='cos')
```


</br>


```python
def sentiment_word_intensity(model, pos_list, neg_list, similarity='cos'):
    """
    Calculate the sentiment intensity of positive and negative words based on their embeddings in a word embedding model.

    Parameters:
    - model (Word2Vec): Word embedding model.
    - pos_list (list): List of positive words.
    - neg_list (list): List of negative words.
    - similarity (str, optional): Similarity measure to be used ('cos' for cosine similarity or 'euc' for Euclidean distance). Defaults to 'cos'.

    Returns:
    - pos_intensity (Series): Series containing sentiment intensity scores for positive words.
    - neg_intensity (Series): Series containing sentiment intensity scores for negative words.
    """
```

The `sentiment_word_intensity` function calculates the sentiment intensity of positive and negative words based on their embeddings in the word embedding model. By comparing the distances between word embeddings and centroids of positive and negative word clusters, this function provides insights into the strength of sentiment conveyed by each word.

#### Example Usage:  
```python
pos_intensity, neg_intensity = sentiment_word_intensity(model, positive_words, negative_words, similarity='cos')
```


### Application
```bash
python main.py
```




## Citation
```
@article{-,  
    author = {Jiexin Zheng, Ka Chung Ng, Rong Zheng and Kar Yan Tam},  
    title = {The Effects of Sentiment Evolution in Financial Texts: A Word Embedding Approach},  
    journal = {-},  
    volume = {n/a},  
    number = {n/a},  
    pages = {},  
    keywords = {word embedding, word list, sentiment evolution, textual analysis, strategic communication},  
    doi = {-},  
    url = {-},  
    eprint = {-},  
}
```

## Contact
```
jzhengas@connect.ust.hk  
kc-boris.ng@polyu.edu.hk  
rzheng@ust.hk  
kytam@ust.hk  
```

## License

[MIT](https://choosealicense.com/licenses/mit/)



