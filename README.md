# WOLVES: Word List Vector for Sentiment

The official implementation of paper "[The Effects of Sentiment Evolution in Financial Texts: A Word Embedding Approach](https://onlinelibrary.wiley.com/doi/full/10.1111/poms.13959)". 

![Gitea Stars](https://img.shields.io/gitea/stars/:user/:repo)


![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/navendu-pottekkat/awesome-readme?include_prereleases)
[![Stargazers][stars-shield]][stars-url]
![GitHub last commit](https://img.shields.io/badge/last_commit-Feb_2024-yellow)
![GitHub issues](https://img.shields.io/github/issues-raw/navendu-pottekkat/awesome-readme)
![GitHub pull requests](https://img.shields.io/github/issues-pr/navendu-pottekkat/awesome-readme)
![GitHub](https://img.shields.io/github/license/navendu-pottekkat/awesome-readme)



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



