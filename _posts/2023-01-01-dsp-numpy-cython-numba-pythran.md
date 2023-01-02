---
layout: post
title: "DSP performance comparison Numpy vs. Cython vs Numba vs Pythran vs Julia"
author: Jochen Schroder
date: 2020-11-17
categories: ml/ai/nlp
tags: best-practice
---

[https://jochenschroeder.com/blog/articles/DSP_with_Python2/](https://jochenschroeder.com/blog/articles/DSP_with_Python2/)

> In my previous post I talked about how we can significantly speed up python code using cython. However, to get the ultimate performance, we need to add significant amounts of boilerplate and the resulting code looks hardly like python any longer. 
>
> I therefore tested two other popular packages for speeding up numerical python code. Numba and Pythran both achieve impressive speed-ups without much more than adding some comments and decorators. In particular Pythran could get about 140 times improvement over numpy by only adding the pythran export comments, which have the advantage that the code remains valid python when one does not want to compile the code.
>
> If we further rewrite the code in particular using explicit loops, results in pythran and numba achieving the same performance as cython (pythran even outperforming it by some margin). In the case of pythran this does take away the advantage of being able to run the code without compilation, as it becomes very slow due to the explicit loops.

> **[Numpy](https://numpy.org/)** The Numpy module provides an array class together with a lot of numerical functions. It is at the core of almost every numerical and scientific package for Python. Here it is going to be our baseline performance.
>
> **[Cython](https://cython.org/)** Cython is a superset of the Python language which can be compiled to C-code. Ideally, if one eliminates most accesses to Python objects it can achieve almost the same speed as C. However, the more you optimize Cython the more it will look like C and less like Python. We showed in our previous post that it achieves an almost 200-fold performance increase on my system over the numpy version.
>
> **[Numba](http://numba.pydata.org/)** Numba is a JIT compiler for a subset of Python and numpy which allows you to compile your code with very minimal changes. In theory it can achieve performance on par with Fortran or C. It can automatically optimize for SIMD instructions and adapts to your system. While numba also allows you to compile for GPUs I have not included that here.
>
> **[Pythran](https://github.com/serge-sans-paille/pythran)** Pythran is a bit the new kid on the block. It’s an ahead of time compiler for numerical and scientific python that can take advantage of SIMD instructions and OpenMP directives to speed up your code. It allows compiling to C++ and doesn’t need a python interpreter so can be used for prototyping code for e.g. embedded devices. Note that recently it has become possible to use Pythran to compile numpy code within Cython.
