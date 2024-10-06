
# Multiclass Twitter Sentiment Analysis using NLP tools and Deep Learning

This project implements a deep learning model to classify the sentiments of tweets related to the COVID-19 pandemic into 5 categories. The model is built, drawing inspiration from architectures like Bidirectional LSTM and includes word embeddings from GloVe. The aim is to create a robust sentiment analysis model that accurately classifies sentiments across various tweets.



## Dataset

The dataset used for training the model is sourced from [Pandemic Tweet Challenge](https://www.kaggle.com/competitions/pandemic-tweet-challenge/overview). It contains 5 unique sentiment categories: Extremely Negative, Negative, Neutral, Positive, and Extremely Positive.


### Dataset Format

- The dataset is stored in a CSV format with two important columns:
  - `OriginalTweet`: The original text of the tweet.
  - `Sentiment`: The sentiment label associated with each tweet.
  - Other columns that are not required for the task are dropped.


### Preprocessing

- Tweets are cleaned to remove irrelevant elements:
  - URLs, mentions, and special characters are removed.
  - Contractions are expanded.
  - Text is lowercased.
- Tokenization is applied to convert tweets into sequences of words.
- Padding ensures all sequences are of equal length.
- Word Embeddings: GloVe embeddings (`glove.6B.100d`) are used to map words to vectors.


## Model Architecture

The model consists of multiple layers including:

- Embedding Layer: Initialized with GloVe embeddings to represent words as vectors.
- Bidirectional LSTM Layers: Used to capture long-term dependencies in the text from both directions.
- Dropout and Batch Normalization: Regularization techniques to prevent overfitting.
- Fully Connected Layers: To combine the learned features before final classification.

Key highlights of the architecture:

![Architecture](https://github.com/user-attachments/assets/811fdab6-6e62-4b4d-9638-28b6b0929f2c)


## Results

### Model Performance

The final performance of the trained model on the test dataset:

- **Training Accuracy**: Approximately 85% - 86%
- **Validation Accuracy**: Approximately 79.35% - 81.60%
- **Test Accuracy**: Approximately 80.25% - 80.79%


### Evaluation Metrics

- **Confusion Matrix**: A confusion matrix is used to visualize the true and predicted labels of the model across all sports categories.

    ![download](https://github.com/user-attachments/assets/88d98640-04fd-417d-b56e-32fe9f89beee)

- **Classification Report**: A classification report is used to analyze the precision, recall and f1-score of the model across all sports categories.
    ```bash
                        precision    recall  f1-score   support

  Extremely Negative       0.77      0.87      0.82       548
  Extremely Positive       0.78      0.88      0.83       663
              Negative       0.77      0.76      0.76       991
               Neutral       0.91      0.85      0.88       772
              Positive       0.80      0.75      0.77      1142

              accuracy                           0.81      4116
             macro avg       0.81      0.82      0.81      4116
          weighted avg       0.81      0.81      0.81      4116
    ```


## Improvements
Future work may involve:

- Experimenting with transformer-based models like BERT to improve sentiment classification accuracy.
- Implementing data augmentation techniques for tweets, such as back-translation and synonym replacement.
- Further hyperparameter tuning to optimize model performance.



## Badges

Open access to anyone!

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)



## Contribute

Contributions are always welcome!




## 🚀 About Me

This is Udoy Saha. I am a tech enthusiast and problem solver.

[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://udoysaha.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/udoysaha103/)


## Feedback

If you have any feedback, please reach out to me at udoysaha103@gmail.com.

