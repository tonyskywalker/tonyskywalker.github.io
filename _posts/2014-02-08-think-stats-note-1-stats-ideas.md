---
layout: default
title: think-stats-note-1: statistical thinking
---

think-stats-note-1: statistical thinking
========================================

Why we learn probability and statistics with a computational approach using python?
-----------------------------------------------------------------------------------
Here are some answers from the author:

* Students write programs as a way of developing and testing their understanding.
For example, they write functions to compute a least squares fit, residuals,
and the coefficient of determination. Writing and testing this code requires them 
to understand the concepts and implicitly corrects misunderstandings.

* Students run experiments to test statistical behavior. For example, they explore 
the Central Limit Theorem (CLT) by generating samples from several distributions. 
When they see that the sum of values from a Pareto distribution doesn’t converge to
normal, they remember the assumptions the CLT is based on.

* Some ideas that are hard to grasp mathematically are easy to understand by simulation. 
For example, we approximate p-values by running Monte Carlo simulations, which reinforces 
the meaning of thep-value.

* Using discrete distributions and computation makes it possible to present topics 
like Bayesian estimation that are not usually covered in an introductory class. 
For example, one exercise asks students to compute the posterior distribution 
for the “German tank problem,” which is difficult analytically but surprisingly 
easy computationally.

* Because students work in a general-purpose programming language (Python), 
they are able to import data from almost any source. They are not limited to data 
that has been cleaned and formatted for a particular statistics tool.


