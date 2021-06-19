
# EM Algorithm — A simple Explanation

Introduction

*“A general technique for finding maximum likelihood estimators in latent variable models is the expectation-maximization (EM) algorithm.”*
> — Pattern Recognition and Machine Learning, 2006.

That's a pretty short definition that I like about EM — Algorithms from the book of Christopher Bishop, so if you understood that definition this post isn’t for you, the purpose of this post is to give a basic and beginner-level conceptual understanding of the Expectation-Maximization algorithm and the concepts that interact with it. By the end of this post, you will find a pretty nice example from a course I got involved a time ago

**Some concepts before getting deeper …**

* Probability Distribution

* Maximum Likelihood Estimation

* Joint Probability Distribution

* Latent Variables

* Likelihood Function

## Some Concepts

**Probability Distribution**

A probability distribution is a function that describes the likelihood of obtaining the possible values that a random variable can assume.

**Maximum Likelihood Estimation**

A maximum likelihood estimation is an approach to density estimation for a dataset by searching across probability distributions and their parameters.

**Latent Variable**

Latent variables are variables that are not directly observed but are rather inferred (through a mathematical model) from other variables.

**Joint Probability Distribution**

First, assume a group of variables and a particular or discrete set of possible values for each variable

The joint probability distribution gives the probability for each variable to fall in any of the defined values for the variable.

**Likelihood Function**

The likelihood function measures how well fit a statistical model for the sample data given.

Data given to the function are values of the unknown parameters.

The data is formed from the joint probability distribution of the sample used as a function of the parameters.

## The Algorithm

1. Given a set of incomplete data, consider a set of starting parameters.

1. **Expectation step (E — step):** Using the observed available data of the dataset, estimate (guess) the values of the missing data.

1. **Maximization step (M — step):** Complete data generated after the expectation (E) step is used in order to update the parameters.

1. Repeat step 2 and step 3 until convergence.

![](https://cdn-images-1.medium.com/max/2000/0*oHhRrftz8qYJHh1G)

The Expectation-Maximization algorithm is to use the available observed data of the dataset to estimate the missing data and then using that data to update the values of the parameters.
> Easy right? Below an explanation a little more detailed of the algorithm

* A set of initial values of the parameters are considered. A set of incomplete observed data is given to the system with the assumption that the observed data comes from a specific model.

* The “Expectation” step: step or *E-step*. In this step, we use the observed data in order to estimate or guess the values of the missing or incomplete data. It is used to update the variables.

* The “Maximization” step: step or *M-step*. In this step, we use the complete data generated in the preceding “Expectation” — step in order to update the values of the parameters. It is basically used to update the hypothesis.

* Converging Review: it is checked whether the values are converging, if yes, then stop otherwise repeat *step-2* and *step-3* until the convergence occurred.

## **Usage of EM algorithm**

* Useful to fill the missing data in a sample.

* Used as the basis of the unsupervised learning of clusters.

* It can be used for the purpose of estimating the parameters of the Hidden Markov Model (HMM) or similar.

* It can be used for discovering the values of latent variables.

## **Advantages of EM algorithm**

* It is always guaranteed that likelihood will increase with each iteration.

* The E-step and M-step are often pretty easy for many problems in terms of implementation.

* Solutions to the M-steps often exist in the closed-form.

## **Disadvantages of EM algorithm**

* It has slow convergence.

* It makes convergence to the local optima only.

## An Application of the EM algorithm: Black Hole Imaging

I found the next slides kind of cool, so I want to share them here because they are related with the topic.

*I got the next slides from a course that I took time ago, it isn’t my own work or has any modification made by me*

![](https://cdn-images-1.medium.com/max/3200/0*GRBblAoWJJhilIfy)

![](https://cdn-images-1.medium.com/max/3200/0*1JSetBUUA_JVGLXh)

![](https://cdn-images-1.medium.com/max/3200/0*KgNI4VVvSlUURY-Z)

![](https://cdn-images-1.medium.com/max/3200/0*Yp9eVosgpvsmpS8E)

![](https://cdn-images-1.medium.com/max/3200/0*pfFNF186__ebE7vd)

![](https://cdn-images-1.medium.com/max/3200/0*jg7VmvBN8FP080Xq)

![](https://cdn-images-1.medium.com/max/3200/0*skgHDkxs0QX_nUfO)
> **Thank you for reading.**
