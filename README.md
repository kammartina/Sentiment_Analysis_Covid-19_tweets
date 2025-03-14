# Sentiment_Analysis_Covid-19_tweets
**Fine-tuning DistilBERT and BERTweet for sentiment analysis task on a dataset with COVID-19 tweets in English** as a final assignment of the introductory class of Computational Linguistics in WS 2024 at the University of Vienna.
<br><br>
This project explores the application of transformer-based models for **sentiment analysis on English-language COVID-19-related tweets** (see the link below). The primary goal was to fine-tune two pre-trained models from Hugging Face — **DistilBERT** (distilbert-base-uncased; see the link below) and **BERTweet** (vinai/bertweet-base; see the link below) — to classify tweets into **three sentiment categories: negative, neutral, and positive**.
<br>
The dataset used is a publicly available **COVID-19 Twitter dataset** from Kaggle, specifically the subset from **August–September 2020**, comprising over **320,000 labeled tweets**. To ensure efficiency and reduce resource consumption, the task utilized only two key columns: "clean_tweet" (renamed to "text") and "sentiment" (renamed to "labels").
<br>
Each model was fine-tuned on a reduced dataset of **2,000 samples**, split into training (80%), validation (10%), and test (10%) sets. After preprocessing and tokenization, both models were trained and evaluated using standard metrics such as **accuracy, precision, recall, and macro F1-score**.
<br><br>

**Highlights:**
<br>
- **Model Accuracy:** DistilBERT – 93%, BERTweet – 92%
- **Data Format:** Converted from Pandas DataFrame to Hugging Face DatasetDict
- **Hyperparameters:** Optimized manually with additional experimentation using **Optuna**
- **Training Environment:** Fine-tuning performed in Google Colab Pro with GPU acceleration
- **Error Analysis:** Confusion matrices and embedding visualizations were used for detailed performance insights
- **Visualization Tools:** Embedding layers analyzed using TensorFlow Projector
<br><br>

Both models demonstrated strong classification performance, with DistilBERT slightly outperforming BERTweet in overall accuracy and sentiment separation. The project also provided insights into the challenges of sentiment classification, especially for ambiguous or mixed-sentiment tweets.
<br><br>
**--> For more details about dataset preprocessing, model architecture, hyperparameter tuning, evaluation results, and visualizations, please refer to the full project report included in this repository.**
<br><br>

**Dataset:** https://www.kaggle.com/datasets/arunavakrchakraborty/covid19-twitter-dataset?select=Covid-19+Twitter+Dataset+%28Aug-Sep+2020%29.csv
<br>
**DistilBERT**: https://huggingface.co/distilbert/distilbert-base-uncased
<br>
**BERTweet**: https://huggingface.co/vinai/bertweet-base
