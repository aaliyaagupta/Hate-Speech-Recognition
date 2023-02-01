# Hate-Speech-Recognition
The problem statement is detection of speech that expresses sentiments of hate and promotes bigotry and hatred. I’ve performed this using machine learning in python. 

A project based on NLP, text processing where the model helps recognise texts containing hateful language that may prove to be offensive.
I have used a variety of methods for detection of hate speech into this project, from the sklearn library,decision tree classifiers, count vectorizer, snowball stemmer, regular expressions, nlp etc.


# Motivation

This sort of malpractice can invoke fear and anxiety in a person or a group of people. This is against the human rights, the practice of hate speech whether it is targeted on a specific caste, religion or even gender.  
This detection system can help protect the minorities at some rate on social media platforms. 
it is clear that automated methods for detecting hate-speech are necessary in some circumstances. In such cases it is critical that the methods employed are accurate, effective, and efficient.




#Tools Used


Different libraries of python have been used such as-


	Numpy- It is used for working with the domain of linear algebra and matrices. It is an open source project and you can use it freely and can be used for numerical analysis.It stands for numerical python which makes it clear the usage and everything for performing mathematical functions.

	Pandas- Used for data manipulation and data analysis in particular. It offers data structures and operation for manipulating numerical tables and time series.

	Count Vectorizer- It’s a utility offered by the skicit learn library, used for converting a given text into a vector, based on holding the number of times a word occurs in the given data, text or a paragraph basically for manipulating the frequency of different words in the text. It comes under feature extraction and there are various methods used for feature extraction

	Train_test_split- This also comes under the scikit learn library and is used for splitting the dataset into training and testing data. Separating the dataset into features(X) and labels (Y), The model is trained and fitted afterwards using X.train and Y.train

	Decision trees- It is a sequence of decisions where each path through the tree results into some sort of classification. Data to be classified begins at the root node where it is passed through the various decisions in the tree according to the values of its features.

	Regular expressions for word tokenization and matching of strings

	NLTK- used for dealing with natural language processing and it offers us numerous test data as dataset and different text processing libraries.


For any machine learning model the methodology is usually common which goes something like this-
Importing the dataset and libraries, splitting the dataset into training and testing data, extracting the features from the dataset and then predicting the correct labels for the training data, then using different classification methods for classifying the data into correct classes and there after predicting the accuracy of the model if required.

	Importing the dataset and libraries- After having imported the libraries explained above such as pandas, scikit learn, numpy etc. we will load the dataset into the  pandas data frame. The dataset consists of various tweets from twitter , the social media platform which may or may not contain hate speech. The dataset would look something like this in the raw csv form.
 

As we can see it contains seven columns which are namely count, offensive language, neither, class and then the actual tweet from which we are detecting the hate speech.


	Providing the labels for the features- Next we will provide the labels to the features, which will namely be 0: “hate speech detected” , 1: “offensive language detected”, 2:”no hate or offensive language detected”. After that we will select only the tweet and the label column for the hate speech detection model. 



	Text Preprocessing – It includes various processes through which we can remove unnecessary words or symbols from our text or data, these kind of words aren’t required for prediction and are usually a stoppage.  

 
 
 
 
 
 # Methodology
 
1.	Cleaning the dataset- which will convert the dataset into all lowercase letters and use regular expressions to check whether the text contains useless symbols such as “/,.;]@” and more.

2.	Removing stopwords and punctuation: stopwords are unnecessary words that appear in the data and are to be removed from it. So this is self- explanatory how using some python commands we can remove stopwords and punctuations from the dataset.


 

3.	Splitting the dataset into training and testing data: Making an array of testing and training data and dividing them into labels and features, where labels will be whether the speech is hate speech or not and the training data will be the tweets dataset.   


4. Count Vectorizer & Classification: Using count vectorizer we divide and then fit the testing and training data into the classification model. Here the classification model which ive used is Decision Tree Classifier, It basically contains of three structures – the internal node which consists the features that we ve extracted from the data, branches contain the decision rules through which a tree performs prediction and each leaf node represents the outcome.
The decisions are performed on the basis of features of a dataset. 
The decision tree this gets us all the possible solutions to any decision using its attribute measure methods such as information gain, gini index etc.


5.	Last step would be checking if the input contains hate speech or not, since now we have trained our model using the training data and now we apply it on other testing data. So the machine correctly classifies as the data as “HATE SPEECH DETECTED” OR “HATE SPEECH NOT DETECTED”


# Result
The result will simply give us whether the testing data or the input is classified as “Offensive language detected” or “Not offensive” 

 

The model that I have trained gives a pretty much accurate result and it correctly classifies the dataset whether it is data consisting of hate speech or not, To show the accuracy of the model we can find out the precision, recall and then the f1 score of the data, It will give us the accuracy of the model. 





