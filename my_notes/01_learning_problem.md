---
layout: page
mathjax: true
title: The Learning Problem
permalink: /my_notes/01_learning_problem/
---

Table of Contents:

- [Problem Introduction](#problem-introduction)
  - [Formalization](#formalization)
  - [References:](#references)

## Problem Introduction

<a name='intro'></a>

Consider the problem of predicting how a movie viewer would rate the various movies out there [[The Netflix Prize]](https://www.thrillist.com/entertainment/nation/the-netflix-prize).

<p align="center">
  <img src="images/01_learning_problem/netflix_prize.png" width="60%" height="60%" >
</p>

Given we know <u>what movies a viewer like (comedy, action, romance,.. )</u> & <u>what does the movie features (same factors)</u>, we can estimate <u>How much did the viewer rate the movie?</u>

### Formalization

The learning problem can be formalized as:

- Input $x$ (viewer likings)
- Output $y$ (rating)
- Target function $f: X \mapsto Y$
- Data: $(x_1, y_1), (x_2, y_2), (x_3, y_3), …$
- Hypothesis: $g: X \mapsto Y$

<p align="center">
  <img src="images/01_learning_problem/basic_setup.png" width="60%" height="60%" >
</p>

The hypothesis set and learning algorithm are referred to informally as the learning model.

### References:
