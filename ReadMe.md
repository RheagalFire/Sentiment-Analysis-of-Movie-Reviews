## Sentiment Analysis of Movie Reviews

This [notebook](https://github.com/RheagalFire/Sentiment-Analysis-of-Movie-Reviews/blob/master/Sentiment%20Analysis%20.ipynb) is a demonstration to implent various classifiers to classify the sentiment of a review as **negative** or **posative**.

### Tooling

- Python
    - Sklearn
    - NLTK
### Concepts

- Classification Algorithms Used
    - Naive Bayes Algorithm 
    - Multinomial Naive Bayes
    - Logistic Regression
    - Bernoulli Naive Bayes Classifier
    - Linear SVC classifier
    - Custom made Vote classifier

### Techniques in Handling Data 

1. The given two **txt** files has to be manually handle to classify them as posative or negative according to the label of filename. 
2. While reading the file words that are adjectives are only appended to the our `all_words` list. This operation is achieved by using `pos_tag` attribute of NLTK.
    Example- 
    ```
    from nltk.tokenize import PunktSentenceTokenizer
    example_text="I love my country , I am grateful for all the things it has given me"
    sample_text='I love biscuits. I am grateful to shops.'
    custom_token=PunktSentenceTokenizer(example_text)
    tokkend=custom_token.tokenize(sample_text)
    for i in tokkend:
        words=word_tokenize(i)
        tagged=nltk.pos_tag(words)
        print(tagged) 
    ```
![output](https://github.com/RheagalFire/Images/blob/main/Capture.JPG)

3. Creating featuresets that is of **tuple** datatype. Most common words are selected that are cross-refrenced against occuring words in document to create a boolean feature like below.

![output 2](https://github.com/RheagalFire/Images/blob/main/Capture2.JPG)

### Classification Results 

![Results](https://github.com/RheagalFire/Images/blob/main/Capture3.JPG)



