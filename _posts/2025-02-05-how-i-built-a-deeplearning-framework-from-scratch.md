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

#### In DeepLearning

To have a better understanding of what happens under the hood of a neuron let's proceed step by step.

The same way a neuron in DeepLearning will receive digital inputs (dendrites) from external providers. The provider can be other neurons, or it can be an image pixel for example.

Let's assume a vector of n inputs :
$$
z=\sum_{i=1}^{n} x_i
$$

Each received signal is assigned an importance, called the weight. The bigger is the weight and the bigger its impact will be on the neuron output.
Once the input received, the neuron will add them up, apply an activation function and send its result as an output to the next external receivers (axon).

Let's make a quick example between an input and a neuron:

### A neural network

Now for the purpose of the course, let's assume a neural network is simply a lot of neurons connected together. Like so


