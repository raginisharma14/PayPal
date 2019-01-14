Description of data - deu.txt is the dataset with english phrases in column1 and german phrases in column2
deu.txt contains 152,820 pairs of English to German phases
the data in deu.txt has the following characteristics
1.There is punctuation.
2.The text contains uppercase and lowercase.
3.There are special characters in the German.
4.There are duplicate phrases in English with different translations in German.
5.The file is ordered by sentence length with very long sentences toward the end of the file.

Description of preprocess.py
preprocess.py will clean the raw data present in deu.txt and saves the cleaned data in english-german.pkl. engligh-german.pkl contain 1,52,820 sentences.
preprocess.py clean the raw data in deu.txt by removing the special characters, removing the punctuations, convert all the chracters to lowercase, removing the numbers from the sentences.

cleaned data looks like below
[hi] => [hallo]
[hi] => [gru gott]
[run] => [lauf]
[wow] => [potzdonner]
[wow] => [donnerwetter]
[fire] => [feuer]
[help] => [hilfe]
[help] => [zu hulf]
[stop] => [stopp]
[wait] => [warte]
...

The clean data contains a little over 150,000 phrase pairs and some of the pairs toward the end of the file are very long.

we will not be using the entire dataset as we are doing thid for the demo, I reduced the dataset to the first 10,000 examples;
these will be the shortest phrases in the dataset.

Further, we will then take the first 9,000 of those as examples for training and the remaining 1,000 examples to test the fit model.

Description of splittext.py
splittext.py takes the first 10,000 examples out of 1,52,820 examples and saves it in the english-german-both.pkl.
also, shuffles the first 10,000 examples and saves 9,000 into english-german-train.pkl and the rest 10,000 in english-german-test.pkl

Description of trainmodel.py
The input to the model is a matrix of [mxn] where m indicates number of sentences which= 9,000 and n indicates the  maximum length of the sentence (maximum number of words in the largest sentence)



Execution Steps 
	1. run preprocess.py
	2. splittext.py
	3. trainmodel.py
	4. test.py

