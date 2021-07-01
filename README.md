HappyMonk Assignment

Model:-
Multilayer perceptron(MLP) model is a class of artificial neural network that uses back propagation technique for training. It has three layers of nodes(including one hidden). During training, all the weights and biases are updated after processing single training sample and the method is called stochastic training. The code is run for 600 epochs alongside EarlyStopping method which uses a technique to stop the model training if validation_loss or validation_accuracy starts to increase or decrease respectively and dependent on which method it was applied. The activation function is sigmoid of the form f(x) = 1 / 1 + exp(-x) Its range is between 0 and 1 . 

Plan:-
We will develop a Multilayer perceptron model for the banknote dataset using Tensorflow in Colab. As of now we have the dataset but still don’t know which features would be suitable for the experiment to work out perfectly.
Given the dataset is small with just 1372 rows it is best to use a smaller batch size of 32 or less(i.e. 16). Using the Adam version of stochastic gradient descent is a good idea when getting started as it will automatically adapt the learning rate and works well on most datasets.

Dataset and Implementation:-
1.)The dataset contains 1,372 rows with 5 numeric variables. It is a classification problem with two classes (binary classification) and ultimately 5th numeric variable or class(column name) to be predicted in the form of 0 or 1.

2.)Further on we went ahead to remove the skewness of this dataset which was higher than the demand of range -1 to 1. Brought it in range as if value is supposed to be greater than 1 make it in our possible ranged value which would be 1 or below it.

3.)Further ahead at checking the correlation with our target matrix we found out one of the column has received it’s correlation in between the range of -0.1 to 0.1 as this range provides no ultimate result and sometimes prove to decrease the accuracy of the model we went ahead and removed the particular column and trained and compared with rest of three.

4.)Data Preprocessing:- As the data was bit not in range and had not much but bit of far values. So, it is always better to transform the data into the range so it becomes understandable and proper one. So, we went ahead and used standardscaler whose basic function is to scale the data with respect to mean=0 and variance=1.

5.)Further splitting the data by random shuffling of 80/20 percent of training and testing we applied MLP model. In this case we use one hidden layer with 10 nodes and output layer(chosen arbitrarily). We used relu activation layer and the he_normal weight initialization, as together, they are a good practice.

Final-Output:-

The output of the model is a sigmoid activation for binary classification and we will minimize binary cross-entropy loss. With 274 epochs used by EarlyStopping method we achieved 100% accuracy in the datset.

Confusion-Matrix:- Confusion_matrix uses the actual and predicted output to generate values for false positives, false negatives, true positives and true negatives.
True Negative(TN):- 155
False Positive(FP):- 0
False Negative(FN):- 0
True Positive(TP):- 120

Precision Score:  1.0

Recall:  1.0

F1-Score:  1.0

