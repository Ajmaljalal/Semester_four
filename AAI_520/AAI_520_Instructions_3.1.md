# Sentiment Analysis with BERT on IMDb Movie Reviews

## Instructions
In this task, use the IMDb movie review dataset and the BERT model from the Transformers library to build a sentiment analysis model that predicts whether a movie review is positive or negative.

## Required Dataset
Use the "IMDB Dataset of 50K Movie Reviews" Dataset is in the same dir called IMDB-Dataset.csv. This is a dataset for binary sentiment classification. It provides a set of 25,000 highly polar movie reviews for training and 25,000 for testing. The dataset contains movie reviews labeled as "positive" or "negative."

## Required Details
1. Text Preprocessing:
  - Tokenize the movie reviews using the BERT tokenizer.
  - Convert the tokenized reviews into input features suitable for BERT.
2. Model Training:
  - Load the pre-trained BERT model for sequence classification from the Transformers library.
  - Fine-tune the BERT model on the preprocessed IMDb dataset for sentiment analysis.
  - Implement training loops and loss calculation.
3. Evaluation:
  - Split the dataset into training and testing sets.
  - Evaluate the trained model on the testing set using accuracy, precision, recall, and F1-score metrics.
4. Predictions:
  - Use the trained model to predict sentiments for a set of sample movie reviews.

## Required Deliverable
Prepare and format the notebook with code (cells) and explaination (markdown) outputs that include the following: 
- Data loading and preprocessing. 
- Text tokenization and conversion to BERT input features.
- Model definition, training, and evaluation.
- Sample movie review predictions and explanations.

## Implementation guides:
- Follow the above instructions and write the approperiate description and python code cells to implement the task. 
- Make sure to only and only do the tasks as mentioned exactactly in the instructions above and here. 
- Do not do any extra steps, code, do not write any code that is not relavent or not needed
- Use "we" instead of "I" or third person. Also use "ing" forms like building a plan instead of Build a plan for example
- Keep the cells short, do not print any unecessary lines. Also do one thing per cell
- Make sure our training is not printing th epoch process, we can just do a one print statement at the end indicating training complete. 