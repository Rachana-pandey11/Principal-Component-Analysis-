# Principal-Component-Analysis

Dataset Used:


Breast CancerWisconsin (Diagnostic) Data Set
Predict whether the cancer is benign or malignant
Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass.
They describe characteristics of the cell nuclei present in the image.


Attribute Information:


1) ID number


2) Diagnosis (M = malignant, B = benign)


3)Ten real-valued features are computed for each cell nucleus:


a) radius (mean of distances from center to points on the perimeter)

b) texture (standard deviation of gray-scale values)

c) perimeter

d) area

e) smoothness (local variation in radius lengths)

f) compactness (perimeter^2 / area - 1.0)

g) concavity (severity of concave portions of the contour)

h) concave points (number of concave portions of the contour)

i) symmetry

j) fractal dimension ("coastline approximation" - 1)


The mean, standard error and "worst" or largest (mean of the three largest values) of these features
were computed for each image, resulting in 30 features.

For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius. All feature
values are recoded with four significant digits.


• Missing attribute values: none
• Class distribution: 357 benign, 212 malignant

Algorithm:


Principal Component Analysis is an unsupervised learning algorithm that is used for the
dimensionality reduction in machine learning. It is a statistical process that converts the
observations of correlated features into a set of linearly uncorrelated features with the help
of orthogonal transformation. These new transformed features are called the Principal
Components. It is one of the popular tools that is used for exploratory data analysis and
predictive modeling. It is a technique to draw strong patterns from the given dataset by
reducing the variances.
PCA generally tries to find the lower-dimensional surface to project the high-dimensional
data.

Steps :

Step 1: Getting the dataset
Firstly, we need to take the input dataset and divide it into two subparts X and Y, where X is
the training set, and Y is the validation set.


Step 2: Representing data into a structure

Now we will represent our dataset into a structure. Such as we will represent the two-
dimensional matrix of independent variable X. Here each row corresponds to the data items,
and the column corresponds to the Features. The number of columns is the dimensions of
the dataset.


Step 3: Standardizing the data
In this step, we will standardize our dataset. Such as in a particular column, the features
with high variance are more important compared to the features with lower variance.
If the importance of features is independent of the variance of the feature, then we will
divide each data item in a column with the standard deviation of the column. Here we will
name the matrix as Z.


Step 4: Calculating the Covariance of Z
To calculate the covariance of Z, we will take the matrix Z, and will transpose it. After
transpose, we will multiply it by Z. The output matrix will be the Covariance matrix of Z.


Step 5: Calculating the Eigen Values and Eigen Vectors
Now we need to calculate the eigenvalues and eigenvectors for the resultant covariance
matrix Z. Eigenvectors or the covariance matrix are the directions of the axes with high
information. And the coefficients of these eigenvectors are defined as the eigenvalues.


Step 6: Sorting the Eigen Vectors
In this step, we will take all the eigenvalues and will sort them in decreasing order, which
means from largest to smallest. And simultaneously sort the eigenvectors accordingly in
matrix P of eigenvalues. The resultant matrix will be named as P*.


Step 7: Calculating the new features Or Principal Components
Here we will calculate the new features. To do this, we will multiply the P* matrix to the Z.
In the resultant matrix Z*, each observation is the linear combination of original features.
Each column of the Z* matrix is independent of each other.


Step 8: Remove less or unimportant features from the new dataset.
The new feature set has occurred, so we will decide here what to keep and what to remove.
It means, we will only keep the relevant or important features in the new dataset, and
unimportant features will be removed out.
