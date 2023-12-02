# **Supervised learning**
	
Regression

- predict a number
- infinitely
- many possible outputs

Classification
- predict categories
- small number of possible outputs

# **Unsupervised learning**

Clustering
- No giving classic
- Auto group without label

*Data
input -> $x$ not output $y$
Algorithm has to find structure in the data*

- Clustering
	- Group similar data
	- points together
- Anomaly detection
	- Find unusual data point
- Dimensionality reduction
	- Compress data using fewer numbers
	
*$x$ = "input" variable / feature
$y$ = "output" variable / "target" variable
m -> number of training example
$(x,y)$ -> single training example
$(x^{(i)},y^{(i)})=i^{th}$
$(1^{st},2^{nd},3^{rd}\dots)$
not refer to exponent!*

training set=>
learning algorithm=>
$x$ -> $f$ -> $\hat{y}$  '$y$-hat' 'estimate'

So for the model
	$size(x)$ -> $(f)$ -> $price(y)$
	
	$f_{w,b}(x)=wx + b$

# **Cost function**
Model:$f_{w,b}(x)=wx+b$
	$w,b$:parameters
	coefficients/weights
$$
J(w,b)=\frac{1}{2m}\sum_{i=1}^{m}(f_{w,b}(x^{(i)})-y^{(i)})^{2}
$$
*Squared error cost function*
$minimize_{w,b}J(w,b)$
use simplified first
	-> $f_{w}(x)=wx$ $b=0$
$$
J(w)=\frac{1}{2m}\sum_{i=1}^{m}(f_{w}(x^{(i)})-y^{(i)})^{2}
$$
$minimizeJ(w)$

![[IMG_BDD534B8487D-1.jpeg]]

# **Gradient Descent**
$$J(w,b)$ -> $min_{w,b}J(w,b)$$
for it or any function
out line
- start with some $w,b$ to reduce $J(w,b)$
- keep changing $w,b$ to reduce $J(w,b)$
- until we settle at or near a minimum

$$w=w-\alpha\frac{\partial}{\partial w}J(w,b)$$
$$b=b-\alpha\frac{\partial}{\partial b}J(w,b)$$
$\alpha$ -> Learning rate
Simultaneously update $w$ and $b$
*Repeat*
$tmp\_w=w-\alpha\frac{\sigma}{\sigma w}J(w,b)$
$tmp\_b=b-\alpha\frac{\sigma}{\sigma b}J(w,b)$
$w=tmp\_w$
$b=tmp\_b$

$\alpha$' _choosing_

$$\frac{\partial}{\partial w}J(w,b)=\frac{1}{m}\sum_{i=1}^{m}(f_{w,s}(x^{i})-y^{(i)})x^{i}$$
$$
\frac{\partial}{\partial b}J(w,b)=\frac{1}{m}\sum_{i=1}^{m}(f_{w,s}(x^{i})-y^{(i)})
$$

# **Algorithm**

repeat until convergence {
$$
w=w-\alpha\frac{1}{m}\sum_{i=1}^{m}(f_{w,s}(x^{i})-y^{(i)})x^{i}
$$
$$
b=b-\alpha\frac{1}{m}\sum_{i=1}^{m}(f_{w,s}(x^{i})-y^{(i)})
$$
}
*Batch -> using all training set in each step*

**Multiple features(variables)**
- $x_i$ = $j^{th}$_feature_
- $n$ = _number of features_
- $\vec x^{(i)}$= _features of $i^{th}$ training example_
- $x_j^{(i)}$ = _value of feature $j$ in $i^{th}$ training example_

Model
_multiple linear regression_
$$
f_{\vec w,b}(\vec x)=w_1x_1+w_2x_2+w_3x_3+w_4x_4+\dots+w_nx_n+b
$$
$$
	\vec w=\left[\begin{array}{[}w_1&w_2&w_3\dots w_n\end{array}\right]
$$
$$
\vec x=\left[\begin{array}{}x_1&x_2&x_3\dots x_n\end{array}\right]
$$
$$
f_{\vec w,b}(\vec x)=\vec w\cdot\vec x+b
$$

Vectorization
`f=np.dot(w,x) + b`
$\vec w=(w_1,w_2\dots w_n)$ -> _parameters_
$\vec d=(d_1,d_2\dots d_n)$ -> _derivatives_
_compute_ $w_j=w_j-\alpha d_j$ _for_ $j=1\dots n$

|| previous notation | vector notion |
| ---- |----|----|
| Parameters |$w_1,\cdots,w_n$ $\&$ $b$|$\vec w[\begin{array}{}w_1\cdots w_n\end{array}]$ $\&$ $b$|
|Model|$f_{\vec w,b}(\vec x)=w_1x_1+\dots$|$f_{\vec w,b}(\vec x)=\vec w_1+b$|
|Cost function|$J(w_1,\cdots,w_n,b)$|$J(\vec w,b)$|
**Gradient descent**
_repeat_{
$$
w_j=w_j-\alpha\frac{\partial}{\partial w_j}J(w_1,\dots,w_n,b)
$$
$$
b=b-\alpha\frac{\partial}{\partial b}J(w_1,\dots,w_n,b)
$$
}
_repeat_{
$$
w_j=w_j-\alpha\frac{\partial}{\partial w_j}J(\vec w,b)
$$
$$
b=b-\alpha\frac{\partial}{\partial b}J(\vec w,b)
$$
}

$n$ _features_ ($n>2$)
repeat {
$j=1$
$$
w_1=w_1-\alpha\frac{1}{m}\sum_{i=1}^m(f_{\vec w,b}(\vec x^{(i)}-y^{(i)})x_1^{(i)}
$$
$$
\dots
$$
$j=n$
$$
w_n=w_n-\alpha\frac{1}{m}\sum_{i=1}^m(f_{\vec w,b}(\vec x^{(i)}-y^{(i)})x_n^{(i)}
$$
}
_simultaneously update $w_j(for\ j=1,\dots,n)$ and $b$_

# **Feature scaling**
$$
300\le x_1\le2000\quad 0\le x_2\le5
$$
$$
\downarrow
$$
$$
x_{1,scaling}=\frac{x_1}{2000}\quad x_{2,scaling}=\frac{x_2}{5}
$$
$$
0.15\le x_1\le1\quad 0\le x_2\le1
$$
**Mean normalization**
_average_
$$\mu_1\qquad\qquad\mu_2$$
$$x_1=\frac{x_1-\mu_1}{2000-300}\qquad\qquad \cdots$$
$$-0.18\le x_1\le0.82\qquad\qquad \cdots$$
**Z-score normalization**
$$\mu_1\quad\sigma_1(standard\ deviation)$$
$$x_1=\frac{x_1-\mu_1}{\sigma_1}$$
$$-0.67\le x_1\le3.1$$
****
**Checking Gradient Descent for Convergence**
![[IMG_D58E0DBA13FF-1.jpeg]]
Automatic convergence test
- $\varepsilon\ be\ 10^{-3}$
- _If j decreases $dj\le\varepsilon$_
- _->declare converged_
_(difficult to find $\varepsilon$ )_

Alpha -> small number -> J not decrease -> bug

**Try** $$0.001\rightarrow0.003\rightarrow0.01\rightarrow0.03\rightarrow0.1\rightarrow0.3\rightarrow1$$
**Feature engineering**
**Polynomial Regression**
****
# **Classification**
- Sigmoid function
- Logistic function
![[IMG_5C6A14F4806D-1.jpeg]]
$$
g(z)=\frac{1}{1+e^{-z}}
$$
$$z=\vec w\cdot\vec x+b$$
$$0<g(z)=\frac{1}{1+e^{-z}}<1$$
$$f_{\vec w,b}(\vec x)=g(\vec w\cdot\vec x+b)=\frac{1}{1+e^{-(\vec w\cdot\vec x+b)}}$$
$$f_{\vec w,b}(\vec x)=0.7$$
70% chance that $y$ is 1
$P(y=0)+P(y=1)=1$
$$
f_{\vec w,b}(\vec x)\ge0.5
$$
$$
g(z)\ge0.5
$$
$$z\ge0$$
$$
\vec w\cdot\vec x+b\ge0\quad\vec w\cdot\vec x+b\ge0
$$
$$
\hat y=1\qquad\hat y=1
$$
Decision boundary
$$z=\vec w\cdot\vec x+b=0$$
Non-linear decision boundary

 **Cost function**
Squared error cost
$$
J(\vec w,b)=\frac{1}{m}\sum^m_{i=1}(f_{\vec w,b}(\vec x^{(i)}-y^{(i)})^2
$$
![[Pasted image 20231027235219.png]]

**$lossL(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})$**
_Logistic loss function_
$$
L(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})=\left\{\begin{matrix}{}-\log(f_{\vec w,b}(\vec x^{(i)}))&if\ y^{(i)}=1\\-\log(1-f_{\vec w,b}(\vec x^{(i)}))&if\ y^{(i)}=0\end{matrix}\right.
$$
- $lossL(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})\rightarrow1$ then  $loss\rightarrow$ 0
- $lossL(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})\rightarrow0$ then  $loss\rightarrow$ $\infty$
- loss is lowest when $f_{\vec w,b}(\vec x^{(i)})$ predicts close to true label $y^{(i)}$

![[IMG_A43CBC0B2CBE-1.jpeg]]
$y^{(i)}=0$
As $f_{\vec w,b}(\vec x^{(i)})\rightarrow0$ then $loss\rightarrow0$
$$
L(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})=\left\{\begin{matrix}{}-\log(f_{\vec w,b}(\vec x^{(i)}))&if\ y^{(i)}=1\\-\log(1-f_{\vec w,b}(\vec x^{(i)}))&if\ y^{(i)}=0\end{matrix}\right.
$$
![[Pasted image 20231028224424.png]]

**Simplified cost function**
$$
L(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})=-y^{(i)}\log(f_{\vec w,b}(\vec x^{(i)}))-(1-y^{(i)})\log(1-f_{\vec w,b}(\vec x^{(i)}))
$$
$$J(\vec w,b)=\frac{1}{m}\sum^m_{i=1}[L(f_{\vec w,b}(\vec x^{(i)}),y^{(i)})]$$
$$=-\frac{1}{m}\sum^m_{i=1}[-y^{(i)}\log(f_{\vec w,b}(\vec x^{(i)}))-(1-y^{(i)})\log(1-f_{\vec w,b}(\vec x^{(i)}))]$$
_maximum likelihood_

Training logistic regression
![[Pasted image 20231028230127.png]]

**Gradient descent**
![[Pasted image 20231028230313.png]]
_simultaneous updates_
**different**
![[Pasted image 20231028230447.png]]

# **The problem of Overfitting**
**Regression example**
linear regression
- ![[Pasted image 20231028231102.png]]
	- underfit
	- highbias
	- Does not fit the training set well
- ![[Pasted image 20231028231152.png]]
	- Fits training set pretty well
	- generalization
	- just right
- ![[Pasted image 20231028231256.png]]
	- Fits the training set extremely well
	- overfit
	- high variance

**Classification**
- ![[Pasted image 20231028231829.png]]
	- underfit
	- high bias
- ![[Pasted image 20231028231906.png]]
	- just right
- ![[Pasted image 20231028231934.png]]
	- overfit
	- high variances

# **Addressing Overfitting**
- Collect more training examples
	- ![[Pasted image 20231028232126.png]]
- Select features to include/exclude
	- ![[Pasted image 20231028232345.png]]
- Regularization
	- ![[Pasted image 20231028232518.png]]

_Option_
- Collect more data
- Select feature - Feature selection \[course 2\]
- Reduce size of parameters -"Regularization" \[next videos\]

# Regularization
**Intuition**
![[Pasted image 20231028233535.png]]
_make $w_3,w_4$ really small_
![[Pasted image 20231028233748.png]]
$W_1,W_2,W_3,\cdots,W_{100},b$
![[Pasted image 20231028234215.png]]

**Regularization**
![[Pasted image 20231028234617.png]]

![[Pasted image 20231028234717.png]]

**Regularized linear regression**
![[Pasted image 20231028235234.png]]
**Implementing gradient descent**
![[Pasted image 20231028235317.png]]

_Option part_
![[Pasted image 20231029114109.png]]
![[Pasted image 20231029114323.png]]

## Cost function
![[Pasted image 20231029114551.png]]

## Regularized logistic regression
![[Pasted image 20231029114749.png]]
****
# all slides
### **Advanced learning algorithms**
Neural Networks
- inference(prediction)
- training
Practical advice for building machine learning systems
Decision Trees

#### Neural networks
- Origins: Algorithms that try to mimic the brain. 
- Used in the 1980's and early 1990's. 
- Fell out of favor in the late 1990's. 
- Resurgence from around 2005. 
- speech -> images -> text(NLP) -> $\cdots$

**Biological Neuron**
![[Pasted image 20231104105255.png]]
**Simplified mathematical modal of a neuron**
![[Pasted image 20231104105353.png]]
### Why Now?
![[Pasted image 20231104105751.png]]

#### Demand prediction
![[Pasted image 20231104110146.png]]
![[Pasted image 20231104110643.png]]
![[Pasted image 20231104110851.png]]
Multiple hidden layers
![[Pasted image 20231104111415.png]]

#### Face recognition
![[Pasted image 20231104111707.png]]
![[Pasted image 20231104112008.png]]
activations are higher higher level features

#### Neural network layer
![[Pasted image 20231104112705.png]]
![[Pasted image 20231104112959.png]]
![[Pasted image 20231104113049.png]]

#### More complex neural network
![[Pasted image 20231104113814.png]]

#### Handwritten digit recognition
forward propagation

#### TensorFlow implementation
![[Pasted image 20231104114826.png]]
![[Pasted image 20231104115420.png]]
```
x = np.array([[200.0,17.0]])
layer_1 = Dense(units=3, activation='sigmoid')
a1 = layer_1(x)
```

```
layer_2 = Dense(units=1, activation='sigmoid')
a2 = layer_2(a2)
```

**Model for digit classification**
```
x = np.array([[0.0,...245,...240...0]])
layer_1 = Dense(units=25, activation='sigmoid')
a1 = layer_1(x)
```

```
layer_2 = Dense(units=15, activation='sigmoid')
a2 = layer_2(a1)
```

```
layer_3 = Dense(units=1, activation='sigmoid')
a3 = layer_3(a2)
```

#### Data in TensorFlow
**Note about numpy array**
![[Pasted image 20231104120750.png]]

#### Building a neural network architecture
```
layer_1 = Dense(units=3, activation='sigmoid')
layer_2 = Dense(units=2, activation='sigmoid')
model = Sequential([layer_1, layer_2])

x = np.array([[...],
              [...],
              [...],
               ...
              [...]])
y = np.array([])
model.compile(...)
model.fit(x,y)

model.predict(x_new)
```

#### Forward prop in a single layer
![[Pasted image 20231105000542.png]]

#### in Numpy
![[Pasted image 20231105001338.png]]

#### For loops vs. vectorization
![[Pasted image 20231105004814.png]]

#### Matrix multiplication
Dot products
![[Pasted image 20231105111145.png]]

Vector matrix multiplication
![[Pasted image 20231105111356.png]]

matrix matrix multiplication
![[Pasted image 20231105111856.png]]

#### Matrix multiplication rules
![[Pasted image 20231105112638.png]]
#### Matrix multiplication in code
numpy
![[Pasted image 20231105113140.png]]
Dense layer vectorized
![[Pasted image 20231105113458.png]]

#### Train a Neural Network in TensorFlow 
![[Pasted image 20231111113011.png]]

### Training Details
**Model Training Steps**
![[Pasted image 20231111113828.png]]
- Create the model
- ![[Pasted image 20231111114230.png]]
- Loss and cost functions
- ![[Pasted image 20231111114700.png]]
- Gradient descent
- ![[Pasted image 20231111114827.png]]

#### Activation function
Demand Prediction Example
- Sigmoid
- ReLU
- No activation function -> linear
![[Pasted image 20231111125834.png]]

#### **Choosing action**
- Output layer
- ![[Pasted image 20231111130302.png]]
- Hidden layer
- ![[Pasted image 20231111130741.png]]
- Summary
- ![[Pasted image 20231111130934.png]]

Linear example
![[Pasted image 20231111152133.png]]
![[Pasted image 20231111152306.png]]

#### Multiclass
![[Pasted image 20231111152650.png]]
![[Pasted image 20231111152813.png]]
#### Softmax regression
![[Pasted image 20231111154243.png]]
**Cost**
![[Pasted image 20231111160704.png]]

#### Neural Network with Softmax output
![[Pasted image 20231111161644.png]]
![[Pasted image 20231111161920.png]]

#### Numerical Roundoff Errors
##### More numerically accurate implementation of logistic loss:
![[Pasted image 20231111162836.png]]
##### More numerically accurate implementation of softmax:
![[Pasted image 20231111163040.png]]

#### Multi-label Classification
![[Pasted image 20231111163408.png]]
![[Pasted image 20231111163607.png]]
#### Advanced optimization
![[Pasted image 20231112001807.png]] **Adam algorithm Intuition**
![[Pasted image 20231112001954.png]]
MNIST Adam
![[Pasted image 20231112002047.png]]
#### Additional Layer Types
 ![[Pasted image 20231112002322.png]]
 ![[Pasted image 20231112002523.png]]
 ![[Pasted image 20231112002943.png]]

#### Debugging a learning algorithm
 - Get more training example
 - Try smaller sets of features
 - Try getting additional features
 - Try adding polynomial features
 - Try decreasing $\lambda$
 - Try increasing $\lambda$

#### Machine learning diagnostic

### Evaluating your model
![[Pasted image 20231121150857.png]]
Linear regression
![[Pasted image 20231121151218.png]]
![[Pasted image 20231121151241.png]]
It maybe fitting the training set well, but it don't mean that it well fit other well. So when we cut the set into training set and test set, we can view if it can fit new set or not by measure the test error. 

classification problem
![[Pasted image 20231121151745.png]]
![[Pasted image 20231121152013.png]]

#### The bias variance tradeoff
Neural networks and bias variance 
![[Pasted image 20231123205843.png]]

![[Pasted image 20231123210325.png]]

### iterative loop of ML development
- Choose architecture (model, data, etc)
- Train model
- Diagnostics (bias, variance and error analysis)
### Error analysis
- More data features

### Adding data
- Data Augmentation
	- Change the source of your data set 
	- Meaningful change
	- Data  synthesis
		- Generate large number of data set of your application
	- Engineering the data used by your system
		- AI = Code + Data
		- Data-centric approach: focus on data

### Transfer learning
- Only train output layers parameters
- Train all parameters
-  ![[Pasted image 20231126104435.png]]
- Use the pre-train parameters to train your model
- Download neural network network parameters pretrained on a large dataset with same input type (e.g., image, audio, text) as your application (or train your own). 
- Further train (fine tune) the network on your own data. 

#### Full cycle of a machine learning project
- Scope project
	- Define project
- Collect data
	- Define and collect data
- Train model
	- Training, error analysis & iterative improvement
- Deploy in production
	- Deploy, monitor and maintain system

**Deployment**
- Inference server
- Mobile app 
- Software engineering may be needed for:
	- Ensure reliable and efficient predictions
	- Scaling 
	- Logging 
	- System monitoring 
	- Model updates
- MLOps
	- Machine learning operations 

**Fairness, bias, and ethics**
- Bias
	- Some discriminates
	- Blabla
- Adverse use cases

##### skewed dataset
Rare disease classification example
- Train classifier $f_{\vec{w},b}(\vec{x})$ ($y=1$ if disease present, $y=0$ otherwise)
- Find that you've got 1% error on test set (99% correct diagnose)
- Only 0.5% of patients have the disease

Precision/recall
-  $y=1$ in presence of rare class we want to detect
- ![[Pasted image 20231126112406.png]]
- Precision
	- Of all patients where we predicted $y=1$ , what fraction actually have disease?
	- $\frac{True\ positives}{\#precision\ positive}=\frac{True\ positive}{True\ pos+False\ pos}=\frac{15}{15+5}=0.75$
- Recall
	- Of all patients that actually have the rare disease, what fraction did we correctly detect as having it?
	- $\frac{True\ positives}{\#actual\ positive}=\frac{True\ positive}{True\ pos+False\ nag}=\frac{15}{15+10}=0.6$
- Predict 0 all the time which isn't a good model

Trading off prediction and recall
- Raise  threshold
	- Higher prediction, lower recall
- F 1 score
	- $\frac{1}{\frac{1}{2}(\frac{1}{P}+\frac{1}{R})}=2\frac{PR}{P+R}$
	- ![[Pasted image 20231126114739.png]]


## Decision Tree Model
### Cat classification example
- Categorical (discrete values)
### Decision Tree
![[Pasted image 20231202104155.png]]
### Decision Tree Learning
- How to choose what feature to split on at each node?
	- Maximize purty (or minimize impurity)
- When do you stop splitting
	- When a node is 100% one class
	- When splitting a node will result in the tree exceeding a maximum depth
	- When improvements in purity score are below a threshold
	- When number of examples in a node is below a threshold
#### Entropy as a measure of impurity
![[Pasted image 20231202110116.png]]
$H(p_{1})=-p_{1}\log_{2}(p_{1})-(1-p_{1})\log_{2}(1-p_{1})$
#### Choosing a split information Gain
![[Pasted image 20231202111212.png]]
- So that we can choose root node
- $p_{1}^{left}=\frac{4}{5}\quad p_{1}^{right}=\frac{1}{5}$
- $w^{left}= \frac{5}{10}\quad w^{right}=\frac{5}{10}$
- Information gain
	- $=H(p_{1}^{root})-(w^{left}H(p_{1}^{left})+w^{right}H(p_{1}^{right}))$

