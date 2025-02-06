---
layout: post
title: "How I built an entire DeepLearning framework from scratch"
date: 2025-02-05
categories: blog
---

# How I built an entire DeepLearning framework from scratch

## Introduction

The best way to finally understand a concept is to built it with your own hand. As I wanted to clearly understand the machine, I took of my time to build an entire homemade DeepLearning framework.

## Prerequisite

Being familiar with matrix calculations, object oriented programming and a programming language is a plus.
If not you may not be able to fully understand the following concepts.

## Objectives

Todays objectives:
- Understand the underlying concepts behind the neural network keyword
- Build an entire DeepLearning framework from scratch
- Train fully-connected models
- And finally, infer from data

## Uderstand the untold secrets behind overmystified neural network

### Let's understand how does a neuron work

#### Biological neuron

A biological neuron is composed of dendrites, a cell body and an axon. It receives many electrical signal from the dendrites. The neuron will sum the electrical signals and if the result exceed its activation threshold, then it will generate an electrical signal on its axon.

![A Classic Biological Neuron](/boost-your-code/assets/a_classic_biological_neuron.png)

To be able to learn, a neuron can adjust the importance of each dendrite.

#### In DeepLearning

To have a better understanding of what happens under the hood of a neuron let's proceed step by step.

The same way a neuron in DeepLearning will receive digital inputs (dendrites) from external providers. The provider can be other neurons, or it can be an image pixel for example.

Let's assume a vector of $n$ inputs like so: $\mathbf{x} = (x_1, x_2, \dots, x_n)$, with $x_i$ the scalar at the $i$ position.

Then, the computed output $z$ of the neuron would be equal to:

$$
z = x_1 + x_2 + \dots + x_n \iff z = \sum_{i=1}^{n} x_i
$$

But with this formula, we receive an input but there is no parameter to adjust that will allow our neuron to adapt to its environment.

Each received signal is assigned an importance, called the weight. The bigger is the weight and the bigger its impact will be on the neuron output.
Once the input received, the neuron will add them up, apply an activation function and send its result as an output to the next external receivers (axon).

Let's add another vector of $n$ weight like so: $w = (w_1, w_2, \dots, w_n)$, with $w_i$ the weight applied to the $i$ of the $n$ inputs.

Now the computed output $z$ of our neuron would be equal to:

$$
z = w_1*x_1 + w_2*x_2 + \dots + w_n*w_n + b \iff z = (\sum_{i=1}^{n} w_i*x_i) + b
$$

Yes, now our neuron looks like a linear function. If we leave it like this, a neural network would be simply a linear combination of the inputs.

The activation function introduce non-linearity in the model. It will allow our model to learn more complex relation in the provided inputs.

As I told you just before, a biological neuron sends its signal via its axon only if its threshold has been exceeded. The activation function allows us to 
### A neural network

Now for the purpose of the course, let's assume a neural network is simply a lot of neurons connected together.

