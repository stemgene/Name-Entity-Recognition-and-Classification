# Name-Entity-Recognition-and-Classification

# About Dataset
## DATA
Dataset includes:

* 493 clinical documents in plain text format (xxx_nnn.txt)

* csv file of annotations on these documents (clinical_annotation_file.csv)

## DATA FORMAT
Each clinical document file has a naming convention of xxx_nnn.txt, where xxx is the document ID and nnn is the medical category of the text file. Medical categories include neurology, radiology, discharge summary, general medicine and gastroenterology, with about 100 documents per category.
The csv file of annotations contains 15,656 annotations split into two categories:

The csv file of annotations has the following data format:
* File – file name
* Start – the annotation start offset (position by characters from the start of the file)
* End – the annotation end offset
* Text – the annotated text (as it is in the original document, i.e., doc_str[start:end])
* Class – the type of the mention

# Conclusion
We applied different techniques on the data preparation and then features extraction. We used TF-IDF technique to extract the features from the text but the models was not giving good results. We changed the features extraction technique to Sequance extractor using tensorflow and we got the good results. Data preprocessing, data extraction and hyper parameter tuning helped to boost the perofrmance of RNN but Random forest did not performed well. 


Well about the hyper parameters tuning, we don’t need to set different hyper parameters, train the model and show the results. 
To do this what we need to do, we tune the hyper parameters according to problem, we train and test and know how the model giving results in deep learning. And in Random forest model, we can use GRID SEARCH approach that train the model on all the given hyper parameters and select the best parameters to train the final model.

Hyper parameters for RNN,  
We choose the different number of parameters but after tuning, we got best hyper parameters to get the good results. We used Sigmoid activation function as we need only one output. Sigmoid function helps to get one output for binary problem. We used binary cross entropy as our problem is to classify only two classes. RMSPROP optimizer helps to get the good results. We change and test different epochs and batch sizes but 20 epochs and 500 batch size is good to get the good results as well. 


Hyper parameters for RF,  
To get the best parameters of random forest model, we used grid search which take different parameters every time and train the model. Finally grid search train the model on the best parameters. These are the best parameters for RF model:
{'n_estimators': 200,
 'max_features': 'sqrt',
 'max_depth': 8,
 'criterion': 'gini'}

We got good results on the RNN because it remember each and every information of previous times.
