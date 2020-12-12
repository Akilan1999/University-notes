## Why is logistic regression a linear classifier ?
- We need calculate probabities and choose the one with a higher probability 
- Uses a sigmoid as the end activation function for a binary classification 


### How does logistic regression work 
Ex: Differentiate between cats and dogs 
   - 2 datasets with different labels 

X = For image recognition:
   - We can take a vector of multi-dimention of matrix of RGB and then we flatten it or convert it into a single dimentinoal array
   - We can consider each of the flatten vectors as coulmns so the array has a vector of coulmns 

X = [[X(1)],[X(2)],X(m-1),X(m)]

The logisitic regression will evaluate the probabilty of being a cat or a dog (values: 0 - 1)

Given X (Conditional Probability):
  - Ŷ = P(y=1|X) where 0 ≤ ŷ ≤ 1
P(y=1|x) tells us what is the probability of y being equal to 1 (a dog) given the input vector of features x


Parameters:
  - X 
  - Y (training labels)
  - Ŷ (Predicted output): Ŷ is a conditional probability

W = weights 
B = bias

W(0)X(0) + W(1)X(1) + ... + W(n)X(n) + B (Matrix multiplication of Weight * X)

T = Transpose 
Z = T(W)*X + B 
(To multiply both matrices we need to transpose W)

- We get a real number
- We use the sigmoid function to get the number between 0 and 1

σ(Z)=1/1+e^−Z
Ŷ = σ(Z)

#### cross entropy loss function 
L(y,^y)=−(ylog(^y)+(1−y)log(1−^y))

#### Linear regression vs linear classification 
(Refer slide 15 for diagram (Gradient regression 2))[https://learn-eu-central-1-prod-fleet01-xythos.content.blackboardcdn.com/5b44cfad90f2e/3789752?X-Blackboard-Expiration=1607796000000&X-Blackboard-Signature=UrqYQxQ7kRNKekh69sbLZNUWgg2qOcH7Tcd9XFergcI%3D&X-Blackboard-Client-Id=305155&response-cache-control=private%2C%20max-age%3D21600&response-content-disposition=inline%3B%20filename%2A%3DUTF-8%27%27Lec%25202%2520GD.pdf&response-content-type=application%2Fpdf&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20201212T120000Z&X-Amz-SignedHeaders=host&X-Amz-Expires=21600&X-Amz-Credential=AKIAZH6WM4PL5M5HI5WH%2F20201212%2Feu-central-1%2Fs3%2Faws4_request&X-Amz-Signature=fd21f7adf4fea7b3455f297597a4ef21cc23bf87acbcdf68f592cb4c95669dd9]


#### Gradient Descent: General Idea
- local search optimization 
- local minimum of a function 
- uses backpropogation 
- Cost Function: Measure how wrong model is 
- Z = T(W)*X + B 
- With cross entropy there is only a single global minima 
   - No matter where we search the algorithum will lead us to a single minima

 ##### Steps gradient decent algorithum 
 - Once we have implemented the algorithm, we can train this network.
 - The initialisation of weights: initial weights are randomly chosen, with typical values between -1.0 and 1.0 or -0.5 and 0.5.
 - To ensure a good performance, we need many training samples as possible, so the network can keep adjusting the weights until it has a high enough accuracy. 
 - When achieved that, we can give it a brand new set of inputs to get the predicted value and see if our model is able to generalise. 

 
 ##### Algorithum 
 repeat until convergence
 {
     minimising the cost by updating w and b
 }

 ##### Formula 
 w1 := w1 − α( ∂J(w,b) / ∂w )

 b := b − α ( ∂J(w,b) / ∂b )

 α Learning rate: controls the size of the step in each iteration
 (0.1 to 0.0001)

 Learning rates determine size of jumps 
 - Too small covergance slow 
 - Too big overshooting 
 - Learning rate can be reduced overtime proportional to the gradient (iteration more accurate when close to minimum)

 ##### Batch Learning
 - Each iteration calculates forward pass and computes error 
 - sum all errors and devides by number of samples in the batch 
 - then calcuates gradients and weights accordingly 
 
 ##### Online learning 
 - calculates forward pass, computes error, gradients and weights per sample 
 - then repeats process until convergence 

 ##### In neural networks, one epoch is a full pass through the dataset



