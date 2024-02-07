# Removing-unintended-bias-in-toxic-comment-NLP
Description:
Within the realm of natural language processing, the Conversation AI team encountered a significant challenge when developing toxicity models. They observed that the models tended to inaccurately associate frequently targeted identities with toxicity. For instance, comments containing certain identities like "gay" were often predicted to be toxic, even if the content itself was benign (e.g., "I am a gay woman"). This erroneous association stemmed from imbalances in the training data, which predominantly sourced from environments where certain identities were unfairly depicted in offensive contexts.

This GitHub repository, titled "Removing Unintended Bias in Toxic Comments Based on Natural Language Processing," seeks to rectify this issue by constructing a model capable of identifying toxicity while minimizing unintended biases associated with mentions of identities. By addressing and mitigating these biases, the project aims to foster a more inclusive and equitable online discourse environment, where users are shielded from unwarranted assumptions and stereotypes perpetuated by machine learning algorithms.

## Methodology:
There are mainly three parts involved in development of my project:
a) Data Preparation
b) Model Training
c) Model Testing

### a) Data Preparation
➢ The dataset, that we are working with, is unrefined and skimmed. I started with finding correlation between different columns and performed EDA.
➢ I, then, added self-written functions like get_comment_nature, plot_features_distribution, plot_count and show_wordcloud to better understand and explain the dataset.
➢ Then, I performed NLP tasks like converting text to lower case, removal of punctuations and special characters, removal of stopwords, and performed stemming.
➔ Data Splitting:
I split the data into two dataframes of training and validation using train_test_split.

### b) Model Training
➢ I converted the string data to numeric values using CountVectorizer.
➢ Then I used machine learning model SGDRegressor under Linear Regression models.
➢ Then I performed HyperParameter Tuning using parameters like alpha and penalty, by calculating MeanSquaredError for training and validation dataset and extracted the best model with least MSE.

### c) Model Testing:
➢ I processed the data of test.csv through NLP Tasks and extracted the
required numeric data and passed it to the best_model.
➢ I appended the resulting array to a new csv file called answer.csv.
➢ I also added code to accept live input text comment data and to print live results.
