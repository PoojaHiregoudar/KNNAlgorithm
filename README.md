## KNN Algorithm 

Designed KNN algorthim from scratch to classify Abalone age without using the existing libraries.

### Dataset: The dataset of the project was obtained from the Department of Primary Industry and
Fisheries, Tasmania, Australia, in the form of comma separated values. Which consists of 8
parameters and a corresponding no. of rings for each data point.
Furthermore, the data description provided states the following classes and the class boundaries
which are based on the number of rings of an abalone shell:
• Rings 0-8: Young
• Rings 9-12: Intermediate
• Rings >12: Old

The data processing involved structuring the csv file into a dataset with feature labels and then
using the threshold above to include another column in the dataset which contained the class labels
for the datapoints. The class labels re encoded as 0, 1, 2 with respect to increasing age of the
abalone, as this would ease the coding procedure. Then the dataset was divided into two parts. The
first part contained 3000 points which would be used to train the model and the second part of the
dataset would be left with 1177 points which would be the validation set of our model.

The data processing involved structuring the csv file into a dataset with feature labels and then
using the threshold above to include another column in the dataset which contained the class labels
for the datapoints. The class labels were encoded as 0, 1, 2 with respect to increasing age of the
abalone, as this would ease the coding procedure. Then the dataset was divided into two parts. The
first part contained 3000 points which would be used to train the model and the second part of the
dataset would be left with 1177 points which would be the validation set of our model.
To implement the K-Nearest Neighbors method, the first step was to define the function of the
Euclidean distances. This function would find the Euclidean distance of a data point which would
be an input from the user and find its Euclidean distance from the training dataset.

This distance would be stored in a 3000x2 dimension matrix whose columns would be the
Euclidean distance of the point from input datapoint to the ith datapoint and the class of the ith
datapoint. The next step of the algorithm would be to sort this matrix in the ascending order of
distances and then extract the top “K” number of data points, I can call this K number of points
a K-set for ease of understanding. From this K-set, I found out the number of datapoints from each
class in the set and the class which has the majority would be considered as the class to which our
input data point belongs. 

For one value of K,
It can be said that the errors that it generates is the number of classes it predicted incorrectly from
our validation set. Then the errors were found for a range of K values and plot it on a graph
with the lateral axis representing the values of K and the longitudinal axis representing the
number of errors it generated. The minima of this graph would be the optimal value of K with
the least number of errors. For this algorithm, the dataset which was tested was the validation set
of our main dataset consisting of 1177 datapoints. While the value of K ranged from 1 to 300.

### Visulaization: From the visualization plots of our dataset, causes that can lead to the
inaccuracy in our classification models cab be defined. Below is a list of different plots which can be interpreted
to show how the features of the intermediate class overlap the features of old class.

### Results: From the results that was obtained, it can be told that the dataset has unequal number of data points
for each class which is a major reason for the varying inaccuracies in the classification model. The
other major barrier is inseparable and overlapping data. In other words most of the old abalones
and intermediate abalones exist in the similar region of the feature space so the classifier would
most likely assign our input point the class of the dominant class, which in our case is the
intermediate class.
Ultimately, it can be concluded that, this is a fairly accurate model to predict age group of Young and
Intermediate aged abalones, however, performs poorly for classifying the age group of Old aged
abalones. The solution for this could be to record a new feature in the dataset which makes the
Old aged abalones stand out from other classes. Another solution would be to collect a well
separable data for the old age abalones in the same features.
