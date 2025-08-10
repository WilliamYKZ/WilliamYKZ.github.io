---
layout: post
title: a post with plotly.js
date: 2025-08-10 01:47:00
description: 
tags: formatting charts
categories: sample-posts
chart:
  plotly: true
---


## Memory Accounting

### Tensor 
Which is the basic building block for storing everything: parameters, gradients, optimizer state, data, activations. 

There are multi ways to create tensor for example 
```python
x = torch.tensor([1., 2, 3], [4, 5, 6])
x = torch.zeros(4, 8)
```
All for those tensore are stored as floating point numbers.  

In the Machine Learning we typically call float32 as the full precision, usually is float64 as full precision. 