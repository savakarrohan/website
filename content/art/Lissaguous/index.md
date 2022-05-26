---
title: "Lissaguous curves"
Date: 2022-05-19T18:21:51+05:30
Draft: false
layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: Infinity logos of META Facebook, how do they come about?
inspiration: Facebook, Australian Broadcasting Corporation,
author: Savakar Rohan #if any collaboration
shortDescription: A recent increase in infinity symbols in logos
tags:
  - logo
  - art
  - lissaguous
  - curves
  - Bowditch
  - Chebyshev polynomial
  - Parametric
_links:
  - https://en.wikipedia.org/wiki/Lissajous_curve
  - https://codepen.io/kotwgarnku/full/dMqKZG
  - http://jsxgraph.uni-bayreuth.de/wiki/index.php/Lissajous_curves
  - https://mathcurve.com/courbes2d.gb/lissajous/lissajous.shtml
img01:
img02:
img03:
math: True
---

The recent naming ceremony of Facebook caught my eye, I noticed the symbolic play going on about the company but I seemed to be more intrigued by the new symbol of META. It looked different, peacefull, everending and capable of much much more. This reminded me of the paintings being made by the garage artists, hanging a paint bucket and pushing it on to a blank canvas. I was perplexed when I finally found an article for parametric curves and dwelled in to the beatifull mathematics behind art.

## Introduction

Curves are seen in a lot of applications from art, to engineering, to science. These curves also appear to be solutions to many solutions in the engineering field. It is well known that an arch which is a parabola which is a member of the family of conic sections. There are various ways to draw curves, we could draw using a parametric equation, a function could be written. At the same time we could use define the curve under different coordinate systems. It might be easier to draw a different curve on different systems.

A lissaguous curve can be constructed with a parametric curve $(t)$ and 4 variables $( A, B, a, b, c, d )$

$$
	\begin{array}{ccc|}
		  x &= &A sin(at + \delta) \\\
		  y &= &B sin(bt)
	\end{array}
	\quad 0 \leq\delta \leq \frac{\pi}{2}
$$

Let's have a look at what each of the variables would mean.

- $A$ : Amplitude in x direction.
- $B$ : Amplitude in y direction.
  - The closer the two above values to each other the more the plot is square, as the values are further apart the plot is more rectangular.
- $a,b$ : Frequency in x,y direction respectively.
  - This represents the frequency of the waves in x,y direction respectively. as the ratio increases the number of waves in the x,y direction respectively differ.
- $\delta$ : Phase difference.
  - This explains the different starting locations of the respective starting locations of the x, y points.
  - This would mean that we could move the curve around by varying the $\delta$ variable.

## Visualisation

Now what are the best ways to visualise these equations. As you can see the equations are in the x, y axes,
