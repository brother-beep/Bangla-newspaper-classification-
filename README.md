## Bangla-newspaper-classification-
Classify the category of the Bangla news either the news is political/sports/economy/Technology  etc. After Balancing the data. 

# Load the data 
I have collected the dataset from kaggle. You can get the dataset from the following link : 
https://www.kaggle.com/datasets/furcifer/bangla-newspaper-dataset 
Since the file size is around 1.03 GB. I have load the dataset into my colab server from kaggle directly using kaggle API. There two files available one is data.json and other is data_v2.json . I have used data_v2.json file . 

# Preprocessing 
1) Removed unused columns :
    There are 10 columns and 408471 rows available. For me the usefull columns are content and category.
2) Drop Null values :
3) 
    No null values present in our dataset.
   
4) Drop duplicated values : 
    1567 duplicate rows available in our dataset.
   
5) Balancing the categorical rows :
    Imbalanced categorical distribution :

     bangladesh       232504
     sports            49012
     international     30856
     entertainment     30466  
     economy           17245
     opinion           15699
     technology        12116
     life-style        10852
     education          9721
     I have used undersampling method to reduce the majority class rows randomly and equalized with minory class labels. Choose sample randomly.

     Balanced categorical Distribution :
   
     bangladesh       9721
     economy          9721
     education        9721
     entertainment    9721
     international    9721
     life-style       9721
     opinion          9721
     sports           9721
     technology       9721
   
   6) Convert categorical label into numeric :
      
      The categories are in textual format. As machine can't understand the textual data we need to convert them into numerical data. There are many 
      encoding methods available. Among them I have used label encoding here available in scikit learn .
      
   7) Convert the textual news into vector :
      
      Again different vectorization method available . I have used Keras Tokenizer which not only convert the text into tokens but also assign each 
      tokens with an integer number. It is called integer Encoding. Using pad sequence to equalize the dimension of the word vectors.

   To be continue.....
