**Problem Statement**

1.  Create a augumentation functions using Google translate to convert the sentences also include "random_swap" function, as well as "random_delete".

2.  Use "Back Translate", "random_swap" and "random_delete" to augment the data you are training on.

3.  This task uses standfordtreebank sentiment analysis dataset. we will be using  "datasetSentences.txt" and "sentiment_labels.txt" files. This dataset contains just over 10,000 pieces of Stanford data from HTML files of Rotten Tomatoes. The sentiments are rated between 1 and 25, where one is the most negative and 25 is the most positive.

4.  Train our model and achieve 45%+ validation/text accuracy. 
5.  Training logs showing final validation accuracy, outcomes for 25 example inputs from the test/validation data and also find 10 false positives. 

**Data Augmentation** 
Please refer the below notebook for data augumentation.
https://github.com/srirampattabiraman/Extensive-NLP-and-Deep-Learning/blob/main/session_5/Standford_Data_Augumentation.ipynb

This uses

**Back Translation**

**Description**

"The Rock is destined to be the 21st Century 's new `` Conan '' and that he 's going to make a splash even greater than Arnold Schwarzenegger , Jean-Claud Van Damme or Steven Segal ."


**Translated Description**

"The Rock is destined to be the new `` Conan '' of the 21st century and that it will cause an even greater sensation than Arnold Schwarzenegger, Jean-Claud Van Damme or Steven Segal."


**Random Swap**

**Random Deletion**

"Rock is 21st '' that going to make a even than Arnold Steven ."


Post perfoming data augumentation the resultant data has been saved as csv file with name "transformed_data.csv"

https://github.com/srirampattabiraman/Extensive-NLP-and-Deep-Learning/blob/main/session_5/transformed_data.csv


Have Tried running a model in below notebook for 60 epochs with belwo hyper parameters 

https://github.com/srirampattabiraman/Extensive-NLP-and-Deep-Learning/blob/main/session_5/Sentiment_Analysis_using_Augumentated_data.ipynb

EMBEDDING_DIM = 512
HIDDEN_DIM = 512

N_LAYERS = 5
DROPOUT = 0.2

Providing the screenshot of accuracy of initial few epochs while it is running

![image](https://user-images.githubusercontent.com/55537646/121591130-c1a8de80-ca56-11eb-9a96-c2c244ec6851.png)

