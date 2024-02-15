# WOLVES: Word List Vector for Sentiment

The **WOLVES** (Word List Vector for Sentiment) algorithm is an innovative sentiment analysis algorithm that combines manually defined lists of sentiment words with word embedding techniques to quantify the change in text sentiment over time.WOLVES dynamically updates the sentiment word list based on changing semantics and sentiment intensity, thus solving the problem of static sentiment analysis models. WOLVES can dynamically update the sentiment lexicon according to changing semantics and sentiment intensity, thus solving the limitations of static sentiment analysis models. In addition, WOLVES can help extract valuable business intelligence from financial texts, which provides powerful support for business decision-making.  
The official implementation of paper "[The Effects of Sentiment Evolution in Financial Texts: A Word Embedding Approach](https://onlinelibrary.wiley.com/doi/full/10.1111/poms.13959)". 



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
### Key Functions
```python
def sentiment_word_intensity(model, pos_list, neg_list, similarity='cos')
```

```python
def get_year_bias_data_dict(model_dict, test_pos_words, test_neg_words, pos_benchmark_dict, neg_benchmark_dict, similarity='cos', year_cols=None)
```



### Application
```bash
python main.py
```



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



