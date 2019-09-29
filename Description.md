#Methodology

## *Introduction*

**Data Processing**

Firstly, the data was parsed from a .csv file.

Then the data was transformed by resetting the time values every time the pilot ID changed.

Nan values were replaced with previous values.

**Methods**

PCA:
Dimensionality reduction.

Linear Regression:
The flight data per pilot was fed into the linear regression model in order to attempt in order to dimensionally reduce each pilot's data into significantly fewer variables obtained from the similarity criteria 

RandomForest:
This method was used to predict a label when passing the ten flight parameters into the algorithm.

Gaussian Analysis:
Was implemented in order to further analyze the dataset.

Neural Network:
An idea was proposed to pass the output of the PCA or linear regression (similarity criteria) into a neural network to obtain a label value.