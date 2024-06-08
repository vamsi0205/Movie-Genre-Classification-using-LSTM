# Movie-Genre-Classification-using-LSTM

# Overview

This project aims to classify movie genres based on their plot summaries using a Long Short-Term Memory (LSTM) neural network. The dataset comprises movie titles, genres, and plot summaries from IMDb. The model leverages text preprocessing techniques and LSTM to predict the genre of a movie based on its plot summary.

# Dataset

The dataset consists of a text file with each line containing:

Movie title
Genre
Plot summary

The format for each line in the dataset is:

<id> ::: <title> ::: <genre> ::: <plot_summary>

# Example

1 ::: Oscar et la dame rose (2009) ::: drama ::: Listening in to a conversation between his doctor and parents, 10-year-old Oscar learns what nobody has the courage to tell him. He only has a few weeks to live. Furious, he refuses to speak to anyone except straight-talking Rose, the lady in pink he meets on the hospital stairs. As Christmas approaches, Rose uses her fantastical experiences as a professional wrestler, her imagination, wit and charm to allow Oscar to live life and love to the full, in the company of his friends Pop Corn, Einstein, Bacon and childhood sweetheart Peggy Blue.

# Requirements

* Python 3.x
* pandas
* numpy
* re
* nltk
* scikit-learn
* tensorflow

You can install the necessary libraries using:

pip install -r requirements.txt

# Code Explanation

# Preprocessing

Text Preprocessing: Convert to lowercase, remove punctuation and numbers, remove extra spaces.

Stopword Removal: Remove common English stopwords using NLTK.

Tokenization and Padding:
Convert text to sequences using Keras Tokenizer.

Pad sequences to ensure uniform input length.

# Model Architecture

Embedding Layer: Converts words into dense vectors of fixed size.

LSTM Layer: Captures temporal dependencies in the text.

Dense Layer: Outputs probabilities for each genre.

# Training and Evaluation

Training: The model is trained using categorical cross-entropy loss and Adam optimizer.

Evaluation: The model's performance is evaluated on the test set, and a classification report is generated.

# Saving the Model

The trained model is saved to movie_genre_classification_model.keras.
