# MNIST
Comparing The performance of An SVM Classifier and ANN's on MNIST Hand Digits Dataset

The scope of this proejct is to find how well an SVM Classifier performs compared to Artifical Neural Networks (ANNs). MNIST digits dataset has been used as the data. 
## MNIST Dataset
The MNIST dataset is a database of Hand Written digits.The MNIST database of handwritten digits,which has a training set of 60,000 examples, and a test set of 10,000 examples. Each images is of size 28x28 pixels. So each entry has 784(28x28) features i.e. the 2D images streched to be 1D. It is a subset of a larger set available from NIST. The digits have been size-normalized and centered in a fixed-size image.
![image](https://user-images.githubusercontent.com/80630137/193420339-3e721070-95c3-44a3-9175-3992078762bc.png)

## Description
  I have trained 4 different modelsfpr the comparision of the peroformance. Two of them are base models namely plain SVM classifier, 3 layer Dense ANN with raw data. Since the data is of high dimension, I have used a dimensionality reduction algorithm i.e Principal Component Analysis (PCA) to reduce the raw data's dimensionality to 90% and then fed it to the SVM Classifier. I called this as the PCA+SVM model.
    In order to get better accuracy for ANN's, I have scaled the raw data and then fed it to the 3 layered ANN. This is the 4th model.
#### SVM:
  Support Vector Machine or SVM is one of the most popular Supervised Learning algorithms, which is used for Classification as well as Regression problems. However, primarily, it is used for Classification problems in Machine Learning.The goal of the SVM algorithm is to create the best line or decision boundary that can segregate n-dimensional space into classes so that we can easily put the new data point in the correct category in the future. This best decision boundary is called a hyperplane.SVM chooses the extreme points/vectors that help in creating the hyperplane. These extreme cases are called as support vectors, and hence algorithm is termed as Support Vector Machine.
      ![image](https://user-images.githubusercontent.com/80630137/193420598-4c718711-90af-48e4-bca1-e75fd1cfd9f2.png)
### PCA:
   Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for reducing the dimensionality of a dataset. This is accomplished by linearly transforming the data into a new coordinate system where (most of) the variation in the data can be described with fewer dimensions than the initial data.
### ANNs:
   An Artificial Neural Network in the field of Artificial intelligence where it attempts to mimic the network of neurons makes up a human brain so that computers will have an option to understand things and make decisions in a human-like manner. The artificial neural network is designed by programming computers to behave simply like interconnected brain cells.Artificial Neural Network primarily consists of three layers: Input Layer, Hidden Layer, Output Layer.
      ![image](https://user-images.githubusercontent.com/80630137/193420684-4636f4e8-7a4d-49a5-87d6-cde0e2c88d2b.png)
      
      
## Results 
  Here are the results in a tabular form
 #### Training Results
 
| Model  | Accuracy  | Training Time |
| ------------- | ------------- | ------------- |
| SVM  | 0.9866  | 17 mins 19 secs |
| PCA + SVM  | 0.9951  | 4 mins 17 secs |
| ANNs  | 0.9399  | 55 secs |
| Scaled ANNs  | 0.9922  | 1 min 22 secs |
		
 #### Testing Results
		
| Model  | Accuracy  | Precision | Recall |
| ------------- | ------------- | ------------- |  ------------- |
| SVM  | 0.966  | 0.966 |0.966 |
| PCA + SVM  | 0.9816  | 0.9816 |0.9816 |
| ANNs  | 0.8679  | 0.8690  |0.8679 |
| Scaled ANNs  | 0.978  | 0.978 |	0.978 |

## Conclusion
  It is oberved that with right amount of data PCA+SVM performed equally well in comparision to the 3 layered Dense ANNs. That being said, Neural Networks are the powerful computational objects. With increase in number of hidden layers, ANN's may perform better. Even if the PCA+SVM has the hgihest accuracy, its training time is comparitevely high with respect to the ANNs training time.Further study can be done by comparing other Classifier such as Logistic Regression and Random Forests with more layered ANNs.

### Libraries used
    - Pandas
    - Numpy
    - Matplotlib
    - Seaborn
    - Plotly
    - Sklearn
    - Tensorflow, keras
