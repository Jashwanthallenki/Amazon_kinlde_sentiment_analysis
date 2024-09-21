# Amazon_kinlde_sentiment_analysis
In this NLP project we will be performing the following steps


-> preprocessing and cleaning the data

-> Train Test Split

-> Applying BOW,TF-IDF,Word2Vec

-> Ml algorithms

for converting a dataset to w2v
1. Data cleaning
2. Train W2V model from gensim library
3. Before training in W2V, the training data should tokenized
4. We should convert each data to list of words
5. These W2V provides embeddings for each indiviual words but for   ML models it requires numerical features for entire sentence
6. So we should create a function to convert sentences to vectors
7. words = [word for word in doc if word in model.wv]
8. Then the vector is of size 100 we should be avg
9. Training the model
10. Prediction of the model
11. For better prediction score we should perform data preprocessing and cleaning

