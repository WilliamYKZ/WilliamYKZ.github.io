---
layout: post
title: a post with plotly.js
date: 2025-08-10 01:47:00
description: 
tags: formatting charts
categories: Machine Learning
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

In the Machine Learning we typically call float32(FP32) as the full precision, usually is float64 as full precision. 

Basically the we calculate the memory useage by numel time element size. Here let make an example using FP32
```python
x = torch.zeros(4, 8)
assert x.dtype == torch.float32 # Default type
assert x.size() == torch.Size([4, 8])
assert x.numel() == 4 * 8
assert x.element_size() == 4 #Float is 4 bytes
assert get_memory_useage(x) == 4 * 8 * 4
```

The tensor `x = torch.zeros(4, 8)` has 4 * 8 = 32 elements, which is numel, and each elements is of type `float32` which is the element size. 
