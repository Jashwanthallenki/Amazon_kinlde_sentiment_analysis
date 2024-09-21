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


Basic code for Preprocessing and cleaning of the dataset

  import re
  import nltk
  from nltk.corpus import stopwords
  from nltk.stem import WordNetLemmatizer
  
  nltk.download('wordnet')
  nltk.download('omw-1.4')
  nltk.download('stopwords')
  def cleanData(txt):
  cleanTxt = re.sub(r'http\S+\s',' ',txt)
  
  cleanTxt = re.sub(r'@\S+',' ',cleanTxt)
  
  cleanTxt = re.sub(r'#\S+',' ',cleanTxt)
  
  cleanTxt = re.sub(r'[^A-Za-z0-9\s]',' ',cleanTxt)
  
  cleanTxt = cleanTxt.split()
  
  cleanTxt = [word for word in cleanTxt if word.lower() not in stopwords.words('english')]
  
  
  lemma = WordNetLemmatizer()
  
  cleanTxt = [lemma.lemmatize(word.lower(),pos='v') for word in cleanTxt]
  
  cleanTxt = ' '.join(cleanTxt)
  
  return cleanTxt
  
