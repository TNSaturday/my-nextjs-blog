---
title: 'Machine Learning Basic Terminology'
date: '2022-01-07'
---

## Machine Learning
With normal code, a human writes the code directly, and a computer reads and interprets that code, or some 
derivative of it. Now we’re in a world where a human doesn’t write the algorithm, so what actually happens? 
Where does the algorithm come from? It’s simply one extra step. A human writes the algorithm’s trainer. 
Assisted by a framework, or even from scratch, a human outlines in code the parameters of the problem,
the desired structure, and the location of the data to learn from. Now the machine
runs this program-training program, which continuously writes an ever-improving
algorithm as the solution to that problem. At some point, you stop this program and
take the latest algorithm result out and use it.

The algorithm is much smaller than the data that was used to create it. Gigabytes of
movies and images can be used to train a machine learning solution for weeks, all just
to create a few megabytes of data to solve a very specific problem. The resulting algorithm is essentially a collection 
of numbers that balance the outlined structure identified by the human programmer. The collection of numbers and their 
associated neural graph is often called a model.

## Types of Machine Learning
1. Supervised.
2. Unsupervised.
3. Semi-supervised.
4. Reinforcement.

## Model
When you create a neural network in TensorFlow.js, it’s a code representation of the
desired neural network. The framework generates a graph with intelligently selected
randomized values for each neuron. The model’s file size is generally fixed at this
point, but the contents will evolve. When a prediction is made by shoving data
through an untrained network of random values, we get an answer that is generally as
far away from the right answer as pure random chance. Our model hasn’t trained on
any data, so it’s terrible at its job. So as a developer, our code that we write is complete,
but the untrained result is poor.

Once training iterations have occurred for some significant amount of time, the neural network weights are evaluated 
and then adjusted. The speed, often called the **learning rate**, affects the resulting solution. After taking thousands 
of these small steps at the learning rate, we start to see a machine that improves, and we are engineering a
model with the probability of success far beyond the original machine. We have left
randomness and converged on numbers that make the neural network work! Those
numbers assigned to the neurons in a given structure are the trained model.

## Training
Training is the process of attempting to improve a machine learning algorithm by
having it review data and improve its mathematical structure to make better predic‐
tions in the future.

TensorFlow.js provides several methods to train and monitor training models, both
on a machine and in a client browser.

## Training set
Sometimes called the training data, this is the data you’re going to show your algorithm 
for it to learn from. You might think, “Isn’t that all the data we have?” The answer is “no.”

Generally, most ML models can learn from examples they’ve seen before, but teach‐
ing the test doesn’t assure that our model can extrapolate to recognize data it has
never seen before. It’s important that the data that we use to train the AI be kept sepa‐
rate for accountability and verification.

## Test set
To test that our model can perform against data it has never seen before, we have to
keep some data aside to test and never let our model train or learn from it. This is
generally called the test set or test data. This set helps us test if we’ve made something
that will generalize to new problems in the real world. The test set is generally significantly 
smaller than the training set.

## Validation sets
This term is important to know even if you aren’t at the level where you need it. As
you’ll hear often, training can sometimes take hours, days, or even weeks. It’s a bit
alarming to kick off a long-running process just to come back and find out you’ve
structured something wrong and you have to start all over again! While we probably
won’t run into any of those mega-training needs in this book, those situations could
use a group of data for quicker tests. When this is separate from your training data,
it’s a “holdout method” for validation. Essentially, it’s a practice where a small set of
training data is set aside to make validation tests before letting your model train on
an expensive infrastructure or for an elongated time. This tuning and testing for validation 
is your validation set.

## Tensors
Tensors are the optimized data structure that allows for GPU and Web Assembly acceleration for
immense AI/ML calculation sets. Tensors are the numerical holders of data.

## Normalization
Normalization is the action of scaling input values to a simpler domain. When every‐
thing becomes numbers, the difference in sparsity and magnitude of numbers can
cause unforeseen issues.

For example, while the size of a house and the number of bathrooms in a house both
affect the price, they are generally measured in different units with vastly different
numbers. Not everything is measured in the same metric scale, and while AI can
adapt to measure these fluctuations in patterns, one common trick is to simply scale
data to the same small domain. This lets models train faster and find patterns more
easily.

## Data augmentation
In photo editing software, we can take images and manipulate them to look like the
same thing in a completely different setting. This method effectively makes an
entirely new photo. Perhaps you want your logo on the side of a building or embossed
on a business card. If we were trying to detect your logo, the original photo and some
edited versions would be helpful in our machine learning training data.
Oftentimes, we can create new data from our original data that fits the goal of our
model. For example, if our model is going to be trained to detect faces, a photo of a
person and a mirrored photo of a person are both valid and significantly different
photos!

## Features and featurization
We mentioned featurizing earlier when we talked about the way eyes send what’s
most important to the brain. We do the same thing with ML. If we were trying to
make an AI that guesses how much a house is worth, we then have to identify what
inputs are useful and what inputs are noise.
There’s no shortage of data on a house, from the number of bricks to the crown mold‐
ing. If you watch a lot of home improvement TV, you know it’s smart to identify a
house’s size, age, number of bathrooms, date the kitchen was last updated, and neigh‐
borhood. These are often key features in identifying a house’s price, and you’ll care
more about feeding a model that information than something trivial. Featurization is
the selection of these features from all the possible data that could be selected as
inputs.