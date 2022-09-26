
# Enron Emails

Create a prediction based on the Enron emails.csv dataset



## Authors

- [@trsonderm](https://www.github.com/trsonderm)


## Lessons Learned

Enron email dataset contains a data wrangling time period to generate a workable predictive dataset.

The data was stripped down into To,From,CC for a numerical dataset of int which where indexes of each variation of the columns. This allows for numeric predictions that multiclass classify. The multiclass is used because the number of cc variables is 32k and to predict over 0,1 requires a multiclass algorithm. 

Keeping to a simple approach the algorithms used were a decision tree and knn. Allowing more time would have presented other opportunities including using NLP against the text message body and other techniques. The more advanced techniques would require greater compute capacity to work through in a reasonable timeframe. 

The prediction success is acceptable with Decision Tree at 76% accuracy for the task and Knn at 74%. The most amount of time was spent on preprocessing the dataset to get it formatted into three numerical columns which categorically converted to index numbers. Once the new file of the simplified and converted dataset was created it was fed to the modelling notebook. 

Data Files:

/data/emails.csv[removed from repo]
/data/clean_emails.csv[preprocessed dataset]
/notebooks/email_preprocessing.ipynb[preprocessing]
   output - clean_emails.csv

/notebooks/emails_model_prediction.ipynb[model testing]

Future work:
Cleanup Email Tags

Algorithms:
Gradient Tree Classification
SVM(Time intensive)

Approaches:
Automodeler
Other predictions: Length of message, Subject and From -> To

Nice to Have:
A graph database loading of the email To, From network would provide alot of insight on how the relationships are defined between people... highlighting more important nodes(people)
