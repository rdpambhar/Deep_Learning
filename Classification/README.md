### Assignment

This specific dataset seperates flowers into 3 different classes of species.

Setosa,
Versicolor,
Virginica,

The information about each flower is the following.

sepal length,
sepal width,
petal length,
petal width,


Building model

And now we are ready to choose a model. For classification tasks there are variety of different estimators/models that we can pick from. Some options are listed below.

DNNClassifier (Deep Neural Network)
LinearClassifier
We can choose either model but the DNN seems to be the best choice. This is because we may not be able to find a linear coorespondence in our data.

What we've just done is created a deep neural network that has two hidden layers. These layers have 30 and 10 neurons respectively. This is the number of neurons the TensorFlow official tutorial uses so we'll stick with it. However, it is worth mentioning that the number of hidden neurons is an arbitrary number and many experiments and tests are usually done to determine the best choice for these values. Try playing around with the number of hidden neurons and see if your results change.

The only thing to explain here is the steps argument. This simply tells the classifier to run for 5000 steps. Try modifiying this and seeing if your results change. Keep in mind that more is not always better.
