#Multi-Class Classifier
Implements Subtask C from the 2017 POLEVAL Shared Task: http://2017.poleval.pl/index.php/tasks/ 

1. baseline.ipynb 
    - Runs a Naive Bayes and Decision Tree algorithm on a bag of words representation and provides F1, precision, and recall metrics. 
    - bag of words representation: the tokens (orth) are set in a context window of 7 tokens, with the 4th column containing the target word. START and STOP tokens are added to indicate the start/end of the file, and all tokens are set to lowercase. 
    - input files: "train.xml", "validate.xml", "test-full-1.xml"
    - output files: "train_baseline.csv", "validate_baseline.csv", "test_baseline.csv" (writes dataframes to csv for easier loading)
    - NOTE: I have included the code that preprocesses the data from xml to dataframe, however it takes quite long to run so I do not recommend running that segment of code and instead directly loading the csv files


2. improved.ipynb 
    - Runs a Naive Bayes and Decision Tree algorithm on a bag of words representation and provides F1, precision, and recall metrics. 
    - Runs and reports performance for feature engineering portion of assignment. 
    - bag of words representation: the tokens (orth) are set in a context window of 7 tokens, with the 4th column containing the target word. <s> and </s> sentence markers are added to separate sentences (chunks), and tokens retain their uppercase/lowercase form. 
    - input files: "train.xml", "validate.xml", "test-full-1.xml"
    - output files: "train_improved.csv", "validate_improved.csv", "test_improved.csv" (writes dataframes to csv for easier loading)
    - NOTE: I have included the code that preprocesses the data from xml to dataframe, however it takes quite long to run so I do not recommend running that segment of code and instead directly loading the csv files
    

3. extra_credit_1.ipynb
    - Runs a Naive Bayes and Decision Tree algorithm using the improved system with the specified tests & reports performance metrics:
                - predictor: orth      label = full ctag
                - predictor: lemma     label = part of speech tag
                - predictor: lemma     label = full ctag 
    - input files: "train.xml", "validate.xml", "test-full-1.xml"
    - output files: a train, validate, and test csv file for each test 
    - NOTE: I have included the code that preprocesses the data from xml to dataframe, however it takes quite long to run so I do not recommend running that segment of code and instead directly loading the csv files
