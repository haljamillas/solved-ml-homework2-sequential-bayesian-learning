Download Link: https://assignmentchef.com/product/solved-ml-homework2-sequential-bayesian-learning
<br>
<h1>1           Sequential Bayesian Learning</h1>

Conjugate prior assures that the posterior distribution has the same functional form as the prior. The posterior is computed and viewed as the prior for the next parameter updating.

This property plays an important role in sequential Bayesian learning.

<u>Dataset:</u>

The file data.csv contains two sequences <strong>x </strong>= {<em>x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,…,x</em><sub>100</sub>|0 ≤ <em>x<sub>i </sub></em>≤ 2} and <strong>t </strong>= {<em>t</em><sub>1</sub><em>,t</em><sub>2</sub><em>,…,t</em><sub>100</sub>} which represent the input sequence and the corresponding target sequence, respectively.

<u>Basis Function:</u>

Please apply the sigmoid basis functions <em>φ </em>= [<em>φ</em><sub>0</sub><em>,…,φ<sub>M</sub></em><sub>−1</sub>]<sup>&gt; </sup>of the form

In this exercise, please take the following parameter settings for your basis functions: <em>M </em>= 3, <em>s </em>= 0<em>.</em>6 and with <em>j </em>= 0<em>,…,M </em>− 1. Please take the data size to be <em>N </em>= 5<em>,</em>10, 30 and

80 for each of the following questions.

Bayesian Learning:

Please compute the mean vector <strong>m</strong><em><sub>N </sub></em>and the covariance matrix <strong>S</strong><em><sub>N </sub></em>for the posterior distribution <em>p</em>(<strong>w</strong>|<strong>t</strong>) = N(<strong>w</strong>|<strong>m</strong><em><sub>N</sub>,</em><strong>S</strong><em><sub>N</sub></em>) with the given prior). The precision of likelihood function <em>p</em>(<strong>t</strong>|<strong>w</strong><em>,β</em>) or <em>p</em>(<strong>t</strong>|<strong>x</strong><em>,</em><strong>w</strong><em>,β</em>) is chosen to be <em>β </em>= 1.

<strong>Note: </strong>You need to train your model by fitting data sequentially, this means that when you have calculated the result of case <em>N </em>= 5, you can use another 5 data points to calculate the result of case <em>N </em>= 10.

<ol>

 <li><strong>Plot </strong>five curves sampled from the parameter posterior distribution and <em>N </em>data points, e.g. (10%)</li>

 <li><strong>Plot </strong>the predictive distribution of target value <em>t </em>by showing the mean curve, the region of variance with one standard deviation on both sides of the mean curve and <em>N </em>data points, e.g. (10%)</li>

 <li><strong>Plot </strong>the prior distributions by arbitrarily selecting two weights, e.g. (10%)</li>

 <li>Make some discussion on the results of different <em>N </em>in 1, 2 and 3. (10%)</li>

</ol>

<h1>2           Logistic Regression</h1>

You are given the dataset [1] of fashion products (Fashion MNIST.zip). This dataset contains 5 classes. There are 64 different images in each class. In this exercise, you need to implement batch GD (batch gradient descent), SGD (stochastic gradient descent), mini-batch SGD and Newton-Raphson algorithms to construct a multiclass logistic regression model with softmax transformation (<em>p</em>(<em>C<sub>k</sub></em>|<em>φ<sub>n</sub></em>) = exp(<em>a<sub>nk</sub></em>)<em>/</em><sup>P</sup><em><sub>j </sub></em>exp(<em>a<sub>nj</sub></em>)) = <em>y<sub>k</sub></em>(<em>φ<sub>n</sub></em>) , <em>y<sub>nk</sub></em>. The error function is formed by.

<table width="340">

 <tbody>

  <tr>

   <td width="123">Algorithms</td>

   <td width="75">Batch size</td>

   <td width="142">Iterations in one epoch</td>

  </tr>

  <tr>

   <td width="123">batch GD</td>

   <td width="75"><em>N</em></td>

   <td width="142">1</td>

  </tr>

  <tr>

   <td width="123">SGD</td>

   <td width="75">1</td>

   <td width="142"><em>N</em></td>

  </tr>

  <tr>

   <td width="123">mini-batch SGD</td>

   <td width="75"><em>B</em></td>

   <td width="142"><em>N/B</em></td>

  </tr>

  <tr>

   <td width="123">Newton-Raphson</td>

   <td width="75"><em>N</em></td>

   <td width="142">1</td>

  </tr>

 </tbody>

</table>

<em>N </em>= number of training data, <em>B </em>= batch size

<strong>Note: </strong>You need to normalize the data samples before training and randomly select 32 images as test data for each class.

<ol>

 <li>Set the initial weight vector <strong>w</strong><em><sub>k </sub></em>= [<em>w<sub>k</sub></em><sub>1</sub><em>,…,w<sub>kF</sub></em>] to be a zero vector where <em>F </em>is the number of features and <em>k </em>is the number of classes. Implement batch GD, SGD, mini-batch SGD (batch size = 32) and Newton-Raphson algorithms to construct a multiclass logistic regression. (15%)

  <ul>

   <li><strong>Plot </strong>the learning curves of <em>E</em>(<strong>w</strong>) and the accuracy of classification versus the number of epochs until convergence for training data as well as test data, e.g.</li>

   <li><strong>Show </strong>the classification results of training and test data, e.g.</li>

  </ul></li>

 <li>Use principal component analysis (PCA) to reduce the dimension of images to <em>d </em>= 2<em>,</em>5<em>,</em>10.</li>

</ol>

(15%)

<ul>

 <li>Repeat 1 by using PCA to reduce the dimension of images to <em>d</em>.</li>

 <li><strong>Plot </strong><em>d </em>eigenvectors corresponding to top <em>d </em>eigenvalues, e.g.</li>

</ul>

<strong>Left: </strong>Olivetti faces dataset [2]; <strong>Right: </strong>Examples of top 2 eigenvectors

<ol start="3">

 <li>What do the decision regions and data points look like on the vector space? (15%)

  <ul>

   <li><strong>Plot </strong>the decision regions and data points of the images on the span of top 2 eigenvectors by using PCA to reduce the dimension of images to 2.</li>

   <li>Repeat 3(a) by changing the order from <em>M </em>= 1 to <em>M </em>= 2, e.g.</li>

  </ul></li>

 <li>Make some discussion on the results of 1, 2 and 3. (15%)</li>

</ol>