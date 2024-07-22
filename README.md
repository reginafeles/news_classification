### News Classification

# Objective: 
given a title and description we have to determine whether it belongs to one of four possible categories of news articles.
# Dataset: 
https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset

# Embeddings:
1. Word2Vec
2. GloVe
3. FastText

# Models:
1. CNN
2. RNN (LSTM)
3. BiLSTM
4. CNN-GRU
5. CNN-BiLSTM


## I. In this project work we trained 15 models:

CNN with Word2Vec Embedding layer
CNN with Glove Embedding layer
CNN with FastText Embedding layer
LSTM with Word2Vec Embedding layer
LSTM with Glove Embedding layer
LSTM with FastText Embedding layer
BiLSTM with Word2Vec Embedding layer
BiLSTM with Glove Embedding layer
BiLSTM with Glove Embedding layer
CNN-GRU with Word2Vec Embedding layer
CNN-GRU with Glove Embedding layer
CNN-GRU with Glove Embedding layer
CNN-BiLSTM with Word2Vec Embedding layer
CNN-BiLSTM with Glove Embedding layer
CNN-BiLSTM with Glove Embedding layer

## II. Models Evaluation

Overall, all models exhibit some degree of overfitting
Some possible solutions were applied to tackle this problem, including regularization, BatchNormalization, Dropouts; however, they didn't improve the models' performance
In accordance with the f1-score metric, the models best predict the “Sports” class, “World” is in second place, “Technology” is in third place, and “Business” is in fourth place. Initially we thought that this was due to the length of the text (texts about sports are longer and contain more features). However, EDA showed that the average length of texts about sports is shorter. We can conclude that our models also work well on short texts.
Overall performance of models is in the table below

[](https://github.com/reginafeles/news_classsification/accuracy.png)

Models with FastText show slightly better performance than models with Word2Vec or Glove Embeddings. This confirms similar conclusion ("FastText <...> generally outperforms other combinations") obtained by the authors of the article (Wang et al., 2021). In addition, our findings show that models with Glove are slightly better than with Word2Vec Embedding.

Our jointed models (CNN-GRU, CNN-BiLSTM) show slightly better results. Although the difference in the accuracy metric is not great, it still exists. Thus, the conclusion made in the article (Wang et al., 2016; Murfi et al., 2022) was also confirmed.

#References:
https://aclanthology.org/C16-1229.pdf
https://arxiv.org/ftp/arxiv/papers/2211/2211.05273.pdf
https://dl.acm.org/doi/pdf/10.1145/3443279.3443304
