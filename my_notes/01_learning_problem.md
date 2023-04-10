---
layout: page
mathjax: true
title: The Learning Problem
permalink: /my_notes/01_learning_problem/
---

Table of Contents:

- [Problem Introduction](#problem-introduction)
  - [Formalization](#formalization)
  - [Perceptron Learning Algorithm](#perceptron-learning-algorithm)
  - [References:](#references)

## Problem Introduction

<a name='intro'></a>

Consider the problem of predicting how a movie viewer would rate the various movies out there [[The Netflix Prize]](https://www.thrillist.com/entertainment/nation/the-netflix-prize).

<div class="fig figcenter fighighlight">
  <img src="/images/01_learning_problem/netflix_prize.png" width="60%" height="60%" >
  <div class="figcaption"></div>
</div>

Given we know <u>what movies a viewer like (comedy, action, romance,.. )</u> & <u>what does the movie features (same factors)</u>, we can estimate <u>How much did the viewer rate the movie?</u>

### Formalization

The learning problem can be formalized as:

Given:

- Input \\(x\\) (viewer likings)
- Output \\(y\\) (rating)
- Data: \\((x_1, y_1), (x_2, y_2), (x_3, y_3), …\\)

We want to find the

- Hypothesis: \\(g: X \mapsto Y\\) where \\(g \in H \\)

Assuming

- Target function \\(f: X \mapsto Y\\)

<div class="fig figcenter fighighlight">
  <img src="/images/01_learning_problem/basic_setup.png" width="60%" height="60%">
  <div class="figcaption"></div>
</div>

The <u>hypothesis set </u> and <u>learning algorithm</u> are informally referred to as the <u>learning model</u>.

So, how do we find the hypothesis ? One way is, <u> Say data is linearly separable<u>.

### Perceptron Learning Algorithm

Say we have two classes **Class A** & **Class B**. Then we say

$$ x_i \in A \text{ if } \sum_{i=1}^d w_i x_i > threshold $$

$$ x_i \in B \text{ if } \sum_{i=1}^d w_i x_i < threshold $$

Therefore the linear formular \\( g \in H\\) can be written as, 

$$ h(x) = sign \Biggl(\Biggl( \sum_{i=1}^d w_i x_i \Biggr) - threshold \Biggr) $$

Thus, 
if \\( h(x_i) > 0 \\) then \\( x_i \in A \\) else \\( x_i \in B \\). 

So we have \\(x_i\\), the training data, we need to find optimal \\( w_i\\) & \\(threshold\\) such that we can classify the data as best as we can.

Making some notation changes,

$$ h(x) = sign \Biggl(\Biggl( \sum_{i=1}^d w_i x_i \Biggr) + x_0 w_0 \Biggr) $$

In vector form, the perceptron implements,

$$ h(x) = sign (w^Tx) $$

So, how do we find w ?

### References:
