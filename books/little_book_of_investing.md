---
layout: page
mathjax: true
title: Little Book of Investing
permalink: /books/little_book_of_investing/
---

Table of Contents:

- [Chapter 1: Introduction](#chapter-1-introduction)
  - [Defintions](#defintions)
  - [Perceptron Learning Algorithm](#perceptron-learning-algorithm)
  - [References:](#references)

## Chapter 1: Introduction

Notes:

1. The index fund eliminates the risks of individual stocks, market sectors, and manager selection. Only stock market risk remains.
2. Before the deduction of the costs of investing, beating the stock market is a zero-sum game, examples options, futures, derivatives, etc because the contracts are agreements between two parties, and, if one person loses, then the other party gains. In economics, trade and exchange are thought to be examples of a positive sum game. 
3. Long term investing is positive-sum game, because the entire company's output gets better. However, short-term speculative trading is zero-sum game.
4. As Warren Buffett recently wrote, “When trillions of dollars are managed by Wall Streeters charging high fees, it will usually be the managers who reap outsize profits, not the clients.”
5. Mutual fund investors are confident that they can easily select superior fund managers. They are wrong.

### Defintions

1. Traditional Index Funds(TIFs): Holding a percentage of all shares in the market.
2. Standard & Poor's 500 Index Fund: Holding small percentage in Fortune 500 companies.
3. Game Theory:
   1. Zero-Sum Game: a situation, often cited in game theory, in which one person’s gain is equivalent to another’s loss, so the net change in wealth or benefit is zero.
   2. A positive sum game is where the net result is greater than zero, even though there may be some winners and losers.

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
