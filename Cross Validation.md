Cross validation is used to select the number of hyper parameters of a model. 
It can also be used to select the number of clusters required in K means clustering

The MSE of the validation dataset is used to find the optimal number of parameters for the model

Cross validation is done by splitting the dataset into training and testing data, and comparing the MSE on the testing data. if the MSE increases when the degree of the polynomial is increased, overfitting is occuring

### Cross Validation on smaller datasets
In case there is not enough data to split into training and validation sets, we can use the following methods:
- **Random Sampling**: Validation of models is done by repeatedly drawing random samples from training set and using it as validation set
- **Leave One Out Cross Validation**: Build the model using (n-1) samples and validate using the remaining sample (expensive to implement as it needs $n$ fitting iterations, and may overfit)![[Pasted image 20240921011739.png]]
- **K-Fold Cross Validation**: Training data is split into $k$ disjoint samples of equal size
- **Bootstrap**
