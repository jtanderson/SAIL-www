---
title: "Week 1"
date: 2021-01-27T15:06:43-05:00
draft: true
---

Welcome to the Salisbury AI Lab(SAIL)!

My name is Blaine Mason, and I have been apart of the SAIL group for around a year now.  I am a student at Salisbury University majoring in Computer Science, Math, and Data Science.  Currently, I am interested in going to graduate school and later on become a professor.  Enough about me, let's dive into what I have and will be working on this semester.

---

# The Floating Body

Recently, the head of our group Dr. Anderson published a paper titled [Efficiency of the floating body as a robust measure of dispersion](http://faculty.salisbury.edu/~jtanderson/files/floatingbody.pdf).  Most of this paper is beyond my knowledge, but with the help of Dr. Anderson, I have been able to gain a general understanding of the material.  This week's post will be my attempt to explain the material needed to understand the floating body.

## Convexity

In plain English, a convex set is a set such that for any line defined by two points in the set, there is no point on the line that exists outside the set.  A great example of a convex set is the set defining a square.  There exists a form of a convex set referred to as the polar of the set.  Mathematically, we define the polar as:

$$K^{\circ} := \\{x: \langle x, k \rangle \leq 1  \forall k \in K\\}.$$

At the moment, I do not have a clear way of explaining this.

## Quantiles

The quantile of a level \\(q \in (0,1)\\) of a set of real numbers is the least value that is above a \\(q\\) fraction of the set. For example, the quantile of level \\(.50\\) is also known as the median since it would contain only \\(50\\)% of the data.  Our goal is to generalize this idea of quantiles to multivariate-data, and one way of doing this is to take advantage of the distributions quantile function.  For now, we can understand the quantile function as the inverse of the CDF.  Later, when defining the floating body, we will include a direction \\(\theta\\). The definition of a quantile in regards to a random variable is:

**Definition 1:** The \\(q\\)-quantile of a random variable \\(X\\) at level \\(q \in (0,1)\\) is given by: 

$$\mathcal{Q}_q(X) := \inf\\{t: P(X \leq t) \geq q\\} .$$

## The Support and Radial Function

The support function aims to find the supporting hyperplane in some direction given by the vector \\(u\\).  This is done using the inner product between \\(u\\) and \\(x\\).  If we find the \\(x\\) that maximizes the inner product, we know a supporting hyperplane is orthogonal to \\(x\\).  Formally, we define the support function as:

**Definition 2:** Let \\(K \subseteq \mathbb{R}^n\\) be a convex set.  The support function of a given vector \\(x\\) is: 

$$h_K(x) := \sup\\{\langle x, k \rangle: k \in K\\} .$$

The radial function is defined as:

**Definition 3:** Let \\(K \subseteq \mathbb{R}^n\\) be a convex set.  The radial function of a given vector \\(x\\) is: 

$$\rho_K(x) := \sup\\{a > 0: ax \in K\\} .$$

The radial is essentially a function that returns the largest scalar \\(a\\) such that the vector \\(x\\) does not exceed the boundary of K.  A unique relationship exists where the support function of K is the reciprocal of the radial function of \\(K^{\circ}\\),  \\(h_{K} = \frac{1}{\rho_{K^{\circ}}}\\).

---

Thank you for reading!

Next week, we will define the floating body and discuss the process of establishing membership in \\(K\\) and \\(K^{\circ}\\) efficiently.








