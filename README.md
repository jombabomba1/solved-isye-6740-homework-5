Download Link: https://assignmentchef.com/product/solved-isye-6740-homework-5
<br>
where <em>α<sub>i </sub></em>≥ 0 are the dual variables. What does this imply in terms of how to relate data to <em>w</em>?

Explain why only the data points on the “margin” will contribute to the sum above,i.e., playing a role in defining <em>w</em>.

Suppose we only have four training examples in two dimensions as shown in Fig. Thepositive samples at <em>x</em><sub>1 </sub>= (0<em>,</em>0), <em>x</em><sub>2 </sub>= (2<em>,</em>2) and negative samples at <em>x</em><sub>3 </sub>= (<em>h,</em>1) and <em>x</em><sub>4 </sub>= (0<em>,</em>3).

For what range of parameter <em>h &gt; </em>0, the training points are still linearly separable? ii. (10 points) Does the orientation of the maximum margin decision boundary change as <em>h </em>changes, when the points are separable?

<ol start="2">

 <li><strong>Multi-class classification for MNIST data set, comparison. </strong></li>

</ol>

This question is to compare different classifiers and their performance for multi-class classifications on the complete MNIST dataset at http://yann.lecun.com/exdb/mnist/. You can find the data

1

file mnist 10digits.mat in the homework folder. The MNIST database of handwritten digits has a training set of 60,000 examples, and a test set of 10,000 examples. We will compare <strong>KNN, logistic regression, SVM, kernel SVM, and neural networks</strong>. We suggest to use Scikit-learn, which is a commonly-used and powerful Python library with various machine learning tools. But you can also use other similar libraries in other programming languages of your choice to perform the tasks. Below are some tips.

<ul>

 <li>We suggest you to “standardize” the features before training the classifiers, by dividing the values of the features by 255 (thus map the range of the features from [0, 255] to [0, 1]).</li>

 <li>You may adjust the number of neighbors <em>K </em>used in KNN to have a reasonable result (you may use cross validation but it is not required; any reasonable tuning to get good result is acceptable).</li>

 <li>You may use a neural networks function neural network with hidden layer sizes = (20, 10). • For kernel SVM, you may use radial basis function kernel, and a heuristic called “median trick”: choose the parameter of the kernel <em>K</em>(<em>x,x</em><sup>0</sup>) = exp{−k<em>x </em>− <em>x</em><sup>0</sup>k<sup>2</sup><em>/</em>(2<em>σ</em><sup>2</sup>)}. Choose the bandwidth</li>

</ul>

as <em>σ </em>= <sup>p</sup><em>M/</em>2 where <em>M </em>= the median of {k<em>x<sup>i </sup></em>− <em>x<sup>j</sup></em>k<sup>2</sup><em>,</em>1 ≤ <em>i,j </em>≤ <em>m</em><sup>0</sup><em>,i </em>6= <em>j</em>} for pairs of training samples. Here you can randomly choose <em>m</em><sup>0 </sup>= 1000 samples from training data to use for the “median trick”<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>.

<ul>

 <li>For KNN and SVM, you can randomly downsample the training data to size <em>m </em>= 5000, to improve computation efficiency.</li>

</ul>

Train the classifiers on training dataset and evaluate on the test dataset.

<ul>

 <li>Report confusion matrix, precision, recall, and F-1 score for each of the classifiers. Forprecision, recall, and F-1 score of each classifier, we will need to report these for each of the digits. So you can create a table for this. For this question, each of the 5 classifier, <strong>KNN, logistic regression, SVM, kernel SVM, and neural networks</strong>,</li>

 <li>Comment on the performance of the classifier and give your explanation why some ofthem perform better than the other<strong>Neural networks. </strong>

  <ul>

   <li>Consider a neural networks for a binary classification using sigmoid function for eachunit. If the network has no hidden layer, explain why the model is equivalent to logistic regression.</li>

   <li>Consider a simple two-layer network in the lecture slides. Given <em>m </em>training data (<em>x<sup>i</sup>,y<sup>i</sup></em>), <em>i </em>= 1<em>,…,m</em>, the cost function used to training the neural networks</li>

  </ul></li>

</ul>

where <em>σ</em>(<em>x</em>) = 1<em>/</em>(1 + <em>e</em><sup>−<em>x</em></sup>) is the sigmoid function, <em>z<sup>i </sup></em>is a two-dimensional vector such that ), and). Show the that the gradient is given by

<em>,</em>

where <em>u<sup>i </sup></em>= <em>w<sup>T</sup>z<sup>i</sup></em>. Also find the gradient of <em>`</em>(<em>w,α,β</em>) with respect to <em>α </em>and <em>β </em>and write down their expression.