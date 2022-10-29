# Support-Vector-Machines

Support vector machines (SVMs) are a set of supervised learning methods used for classification, regression and outliers detection.

The goal of the SVM algorithm is to create the best line or decision boundary that can segregate n-dimensional space into classes so that we can easily put the new data point in the correct category in the future. This best decision boundary is called a hyperplane.

SVM chooses the extreme points/vectors that help in creating the hyperplane. These extreme cases are called as support vectors, and hence algorithm is termed as Support Vector Machine. Consider the below diagram in which there are two different categories that are classified using a decision boundary or hyperplane:

![image](https://user-images.githubusercontent.com/109084435/198834388-8ff422b8-3f51-4ceb-bdc3-c3c097667221.png)

SVM algorithm can be used for Face detection, image classification, text categorization, etc.

## Types of SVM

### SVM can be of two types:

#### Linear SVM:

Linear SVM is used for linearly separable data, which means if a dataset can be classified into two classes by using a single straight line, then such data is termed as linearly separable data, and classifier is used called as Linear SVM classifier.

#### Non-linear SVM:

Non-Linear SVM is used for non-linearly separated data, which means if a dataset cannot be classified by using a straight line, then such data is termed as non-linear data and classifier used is called as Non-linear SVM classifier.

## Hyperplane and Support Vectors in the SVM algorithm:

### Hyperplane: 

There can be multiple lines/decision boundaries to segregate the classes in n-dimensional space, but we need to find out the best decision boundary that helps to classify the data points. This best boundary is known as the hyperplane of SVM.

The dimensions of the hyperplane depend on the features present in the dataset, which means if there are 2 features (as shown in image), then hyperplane will be a straight line. And if there are 3 features, then hyperplane will be a 2-dimension plane.

We always create a hyperplane that has a maximum margin, which means the maximum distance between the data points.

### Support Vectors:

The data points or vectors that are the closest to the hyperplane and which affect the position of the hyperplane are termed as Support Vector. Since these vectors support the hyperplane, hence called a Support vector.

## How does SVM works?

### Linear SVM:

The working of the SVM algorithm can be understood by using an example. Suppose we have a dataset that has two tags (green and blue), and the dataset has two features x1 and x2. We want a classifier that can classify the pair(x1, x2) of coordinates in either green or blue. Consider the below image:

![image](https://user-images.githubusercontent.com/109084435/198834634-a6cdefcf-cd44-46b3-bef0-c5b39bdfa816.png)

So as it is 2-d space so by just using a straight line, we can easily separate these two classes. But there can be multiple lines that can separate these classes. Consider the below image

![image](https://user-images.githubusercontent.com/109084435/198834655-9f2f2ae9-fe24-480a-a673-9f36cbed3d22.png)

Hence, the SVM algorithm helps to find the best line or decision boundary; this best boundary or region is called as a hyperplane. SVM algorithm finds the closest point of the lines from both the classes. These points are called support vectors. The distance between the vectors and the hyperplane is called as margin. And the goal of SVM is to maximize this margin. The hyperplane with maximum margin is called the optimal hyperplane.

![image](https://user-images.githubusercontent.com/109084435/198834683-fa0e8a82-8887-40d5-a45f-f7206e25e9a2.png)

### Non-Linear SVM:

If data is linearly arranged, then we can separate it by using a straight line, but for non-linear data, we cannot draw a single straight line. Consider the below image:

![image](https://user-images.githubusercontent.com/109084435/198834714-7ef4ea7d-505f-40b3-bb82-70d9c030dc1d.png)

So to separate these data points, we need to add one more dimension. For linear data, we have used two dimensions x and y, so for non-linear data, we will add a third dimension z. It can be calculated as:

### z=x2 +y2

By adding the third dimension, the sample space will become as below image:

![image](https://user-images.githubusercontent.com/109084435/198834758-e1bc825c-8da9-4798-89fb-dd9be9129a85.png)

So now, SVM will divide the datasets into classes in the following way. Consider the below image:

![image](https://user-images.githubusercontent.com/109084435/198834796-5aea6734-284d-4c28-bcde-7c3756d58ab2.png)

Since we are in 3-d Space, hence it is looking like a plane parallel to the x-axis. If we convert it in 2d space with z=1, then it will become as:

![image](https://user-images.githubusercontent.com/109084435/198834816-f8c5cd00-f6a8-4243-8db3-202d5da45d92.png)

In this case, the new variable y is created as a function of distance from the origin. A non-linear function that creates a new variable is referred to as kernel.

### SVM Kernel:

The SVM kernel is a function that takes low dimensional input space and transforms it into higher-dimensional space, ie it converts non separable problem to separable problem. It is mostly useful in non-linear separation problems. Simply put the kernel, it does some extremely complex data transformations then finds out the process to separate the data based on the labels or outputs defined.

#### Advantages of SVM

-Effective in high dimensional spaces.

-Still effective in cases where number of dimensions is greater than the number of samples.

-Uses a subset of training points in the decision function (called support vectors), so it is also memory efficient.

-Versatile: different Kernel functions can be specified for the decision function. Common kernels are provided, but it is also possible to specify custom kernels.

#### Disadvantages of SVM:

-If the number of features is much greater than the number of samples, avoid over-fitting in choosing Kernel functions and regularization term is crucial.

-SVMs do not directly provide probability estimates, these are calculated using an expensive five-fold cross-validation (see Scores and probabilities, below).
