---
title: "Demystifying Neural Networks"
seoTitle: "Neural Networks for Beginners Step-by-Step"
datePublished: Sat Oct 28 2023 09:10:03 GMT+0000 (Coordinated Universal Time)
cuid: clo9tn3cc000d09l73jmtgwai
slug: demystifying-neural-networks
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698482997344/f70c1831-f5da-4688-92c0-06131075387a.png
tags: machine-learning, guide, beginners, neural-networks

---

Wait, what? Teeny tiny neurons wire together to create one of the most remarkable aspects of Machine Learning?

*Hell, yeah!*

But how exactly? Aha, that's exactly what you are gonna find out in this article!

### 📦 Basic Terminology

Neurons - A function that takes in a value, modifies it and holds it.

Connection - Link between 2 neurons.

Hyperparameters - The model adjusts its parameters in the learning process. So, the parameters you can specify are called hyperparameters.

Input Layer - The initial layer of *neurons* that takes in the external input.

Output Layer - The final layer of *neurons* that spits out the *hopefully* desired output.

Hidden Layer/s - Layers of *neurons* inside a neural network that derive different values from the inputs to activate the output layer.

### ❔ What is a Neural Network?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698480760495/0044804c-a9bd-4f09-b04d-cb3d72715266.jpeg?height=512 align="center")

Think of a Neural Network (NN) as layers of neurons with each neuron connected to another neuron (in a different layer) through *connections*.

Imagine we are building a neural network to help a farmer sort their fruits into three categories: Apples, Bananas, and Oranges based on their weight (grams), colour (red, yellow, orange, green), texture (smooth or rough) and size (small, medium or large).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698442446031/5d3fd252-b306-4fb7-9758-08e1c6130b9f.png align="center")

> When every neuron is connected in this manner, we call it a Dense Network. There are different types of neural networks. We'll delve into them in later articles.

Input data is fed forward through the network using these connections to activate neurons in the output layer.

The hidden layers between the input and output layers are what determine the final activations.

In the lingo, the hidden layers are collectively called a **black box**. Yet, as a smart beginner, you don't have to think about them that way. That's because we'll break down the process step by step!

### ⚙️ How does an NN work?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698480826102/3aaf1e39-7066-4b0f-bd57-9bbe9ee6d4bb.jpeg?height=512 align="center")

When you input data into a neural network, they are stored in the neurons in the input layer.

**How a Neuron gets Activated**

Every *connection* is associated with a specific weight (w). So, to activate one neuron in the next layer, we take the weighted sum of the previous layer.

Let's take a look at the first two layers of our neural network and calculate the weighted sum of a neuron in the first hidden layer;

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698444075870/d03a5616-2ce3-4a07-a588-1e5b3726920d.png?height=512 align="center")

In this case, the weighted sum is,

*a = activation of the previous neurons (i.e. the values they hold)*

$$\text{Weighted Sum} = (a_1\times w_1) + (a_2\times w_2) + (a_3\times w_3) + (a_4\times w_4)$$

Then, we add a constant at the end called the bias before passing down the weighted sum to the next neuron.

$$\text{Value Passed to the Next Neuron}= \text{Weighted Sum} \pm b$$

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Don't forget: Every connection has a unique weight. So, even though the activations in one layer are constant, neurons in the next layer are activated differently.</div>
</div>

In fact, we can just use the `weighted sum + bias` without any modifications. That's called a linear combination (just like x=y in a graph).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698398226957/9d51de2d-0906-4635-ac32-e172b5316aa4.png?height=512 align="center")

Yet, this isn't helpful when it comes to finding complex patterns in data.

So, we pass the `weighted sum + bias` to an activation function. The value it returns is the activation of the neuron. That way, we can find a fancy non-linear model to fit the data.

There's a variety of activation functions, each suited for their purpose:

| Activation Function | Process | Pros | Cons |
| --- | --- | --- | --- |
| ReLU - Rectified Linear Unit | `if input < 0: return 0 else: return input` | Cost-effective & efficient | Leaves behind important data in converting negatives to 0s. |
| Sigmoid | Squishes the input into the range 0-1 | Easy to compute | Introduces the [vanishing gradient problem](https://www.engati.com/glossary/vanishing-gradient-problem#:~:text=Vanishing%20gradient%20problem%20is%20a%20phenomenon%20that%20occurs%20during%20the%20training%20of%20deep%20neural%20networks%2C%20where%20the%20gradients%20that%20are%20used%20to%20update%20the%20network%20become%20extremely%20small%20or%20%22vanish%22%20as%20they%20are%20backpropogated%20from%20the%20output%20layers%20to%20the%20earlier%20layers.). |
| Binary Step Function | `if input < 0: return 0 else: return 1` | Yay, just 0 and 1 to deal with! | Activation information is lost :( |

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">There are modified versions of ReLU like Parametric ReLU and Leaky ReLU to address the issue with classic ReLU.</div>
</div>

*Don't forget! Your purpose defines the activation function.*

Plus, there is a special activation function that is only used in the output layer. It's called ***softmax***.

It takes in all the raw values passed down to the output layer and calculates an activation for each neuron.

*let O = list of raw values passed down to the output neurons.*  
*let i = the raw value passed down to the current neuron.*

$$P_i = \frac{e^{i}}{\sum^{len(O)}_{j=0} e^{O[j]}}$$

For example, if the raw values passed down to all output neurons were \[34, 32, 25\];

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698449726935/d5ecc34b-b626-460a-a8b8-be8bfbe7092e.png?height=512 align="center")

The final activation of the Apple neuron would be,

$$P_{32} = \frac{e^{32}}{e^{34}+ e^{32} + e^{25}} = 0.12$$

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">We raise the values to the power of e (Euler's number) to pronounce the differences.</div>
</div>

**Giving the NN Feedback**

At first, all the weights and biases are selected randomly. So, our NN sucks at making predictions. We need a way to give it feedback and alter its direction towards success.

To achieve that, we use loss functions:

| Loss Function | Process | Pros | Cons |
| --- | --- | --- | --- |
| Mean Squared Error | Means of the squared difference between predicted and actual values. | Smooth optimization | Sensitive to outliers, may not be robust. |
| Cross-Entropy Loss | Quantifies the dissimilarity between predicted and true class probabilities. | Effective for classification tasks. | Sensitive to class imbalance. |
| Mean Absolute Error | The mean absolute difference between predicted and actual values. | Less sensitive to outliers. | Slower convergence. |

**Ultimate Neural Network**

Let's assume we input data that suits an apple. The whole process would be,

*Loss = Squared Error*

*Activation Function of Both Hidden Layers = ReLU (Rectified Linear Unit)*

*Output Layer Activation Function = Softmax*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698449772045/06eebba7-1352-4da2-b3c7-54574a38e3b8.png align="center")

You see, because we haven't trained the network, it predicts the data represents an orange when the correct answer is an apple. So, let's train it!

### 🧑‍🏫 Training an NN

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698480880038/4e0cda5c-5d70-4067-8a24-17b1e788d5b4.jpeg?height=512 align="center")

During the training process, the neural network constantly tries to minimise the loss function for each prediction.

To do so, it uses a fancy algorithm called ***Backpropagation*** along with some cool ***Optimization Functions***.

**Backpropagation**

During this process, we are calculating how big/small the changes in the output-layer-activations should be to result in the desired outputs.

Using these proportional changes for every neuron, we calculate the proportional changes that should have happened in the activations of the previous layer.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">This way, the whole process is repeated for every previous neuron because every activation is dependent on them. That's why we call it <em>backpropagation</em>.</div>
</div>

To minimise complexity, we will focus on how the proportional changes for one neuron activation are propagated backwards from the output layer to the second hidden layer.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698449776770/a5a3f72f-9ef3-4b1e-a9ae-83b01b76e725.png?height=512 align="center")

*Proportional changes are illustrated through the thickness and length of arrows in the image.*

To achieve those required changes, we adjust the weights and biases which affect them the most. This is where optimization functions kick in.

**Optimization Functions**

These are fancy functions to find the optimal values for different weights and biases in the network.

> These are based on some wonderful mathematical operations. Especially, Calculus (e.g. the chain rule).
> 
> We will take a look at the Maths in a future article.

For now, you just have to know some basic optimization functions like,

| Optimization Function | Process | Pros | Cons |
| --- | --- | --- | --- |
| Gradient Descent | Iteratively updates weights & biases by moving in the direction of the steepest decrease in the loss function. | Simple  
Widely applicable | High computation power  
Can get stuck in local minima |
| Stochastic Gradient Descent (SGD) | A variant of gradient descent that randomly samples a subset of data for each iteration. | Faster computation | Can be noisy (i.e. random)  
May require fine-tuning of the learning rate. |
| Adam (Adaptive Moment Estimation) | An adaptive learning rate optimization algorithm that combines aspects of RMSprop and Momentum. | Fast computation | Sensitive to the choice of hyperparameters. |
| RMSprop (Root Mean Square Propagation) | Maintains an adaptive learning rate for each parameter based on the magnitude of recent gradients. | Effective for non-stationary objectives. | Requires careful tuning of hyperparameters. |

### 👋 Conclusion

With this knowledge, you can fluently use a library like Tensorflow Keras and create fantastic neural networks.

With user-friendly and high-level APIs like Tensorflow and PyTorch, you can crack 98% of machine learning without being Math Savvy. That's the reality.

So, don't be afraid! Over time, you'll start to realise what is going on under the hood, intuitively.

Keep in mind that a neural network is like a team of Pokemon. You have to choose your players (i.e. different functions, number of layers/neurons in each layer) to win the battle. So, developing an NN is an art instead of *heavy* math :)

🍀 ***Good luck with developing stunning NNs... You've got this!***