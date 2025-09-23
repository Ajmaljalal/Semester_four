# NLP Preprocessing: News Classification

## Instructions
For this task, you will use the indicated dataset and implement the tasks described below in your Jupyter Notebook or Python script. You will submit your notebook or script as a PDF (preferred) or HTML document. 

## Required Dataset
sklearn.datasets.fetch_20newsgroups

5 categories: Business, Entertainment, Politics, Sport, Tech
~2,225 news articles

## Required Details
Part 1: Data Exploration 
- Load the dataset and show basic statistics
- Visualize article distribution by category
- Display sample articles from each category
Part 2: Text Preprocessing 
- Create and compare 2 preprocessing pipelines:
- Basic: tokenization + lowercasing + stop word removal
- Advanced: Basic + stemming + lemmatization + POS filtering. Compare vocabulary size and processing time for both approaches.
Part 3: Text Vectorization 
- Implement and compare:
- Bag of Words (CountVectorizer)
- TF-IDF (TfidfVectorizer)
- Word2Vec (both CBoW and Skip-gram, average word vectors for documents). Create - visualizations comparing the methods.
Part 4: Classification 
- For each vectorization method, train:
  - Logistic Regression
  - Simple LSTM
  - Report accuracy, precision, recall, and F1-score for each combination.

  ## Code Instructions:
- Follow the above instructiion and write the approperiate description and python code cells to implement the task. 
- Make sure to only and only do the tasks as mentioned exactactly in the instructions. 
- Do not do any extra things, do not write any code that is not relavent or not needed
- Use "we" instead of "I" or third person. Also use "ing" forms like building a plan instead of Build a plan for example
- Keep the cells short, do not print any unecessary lines. Also do one thing per cell
- Make sure our training is not printing th epoch process, we can just do a one print statement at the end indicating training complete. 
