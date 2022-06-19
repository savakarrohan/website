---
title: "Basics of optimization"
Date: 2022-06-18T07:40:50+05:30
Draft: false
layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: A fixed amount of resources always causes us to act in a specific manner. Is it possible to quantify what would make us the most efficient user of our resources? How do we go about writing the problem in mathematical terms? Do these problems always fall under a certain group?
inspiration: Inspired by the MATLAB logo being a peak which I could slice off with a plane
author: Savakar Rohan #if any collaboration
shortDescription: A fixed amount of resources always causes us to act in a specific manner. Is it possible to quantify which manner would make us the most efficient user of our resources? How do we go about writing the problem in mathematical terms? Do these problems always fall under a certain group?
tags:
  - Optimization
  - Convexity
  - Affine
  - Affine states
  - General optimization
  - Non linear optimization
  - Convex optimization
  - Steven Boyd
  - Vandenberghe
  - cvxopt
_links:
  - https://web.stanford.edu/~boyd/cvxbook/
  - https://cvxopt.org/
  - http://www.seas.ucla.edu/~vandenbe/publications/mlbook.pdf
# img01: img/01_Menace/01_tic-tac-toe.png   #front home page card image
# img02:                                    #main card on blog post image
# img03:                                    #Additional just in case.
math: True
---

Optimization is a problem important in everyones lives, we all have fixed amount of resources and intend to do the best we can with this available resource. These resources could be in the form of money, valuable resources like wood, material for projects and most importantly time (A very important asset I have only just realised). These resources are limited and we wish to use them appropiately to gain the most "utility".

## What is it (mathematical explanation)

I would love to extract this excerpt from the book cvxbook available at a link mentioned on the right, a compilation by Steven Boyd and Lieven Vandenberghe, which is curated from lecture slides for an appropiate course. This being a website project for me to better understand and write for academic and teaching purposes I would love to write in my own words.

The optimization problem is posed as finiding that value for a vector $\boldsymbol{x} \in \boldsymbol{R}^n$ such that a function $f_0: \boldsymbol{R}^n \rightarrow \boldsymbol{R}$ evaluated at $\boldsymbol{x}$ attains the least value, after giving further rules that $f_i: \boldsymbol{R}^n \rightarrow \boldsymbol{R}$ evaluated at $\boldsymbol{x}$ is less than a noted value $ b_i \in \boldsymbol{R}$. Another point to be included is that $\boldsymbol{x} \in \boldsymbol{S}$ where $\boldsymbol{S}$ is a set defined on $\boldsymbol{R}^n$. Gathering the above passage in to a simpler math notation we have the following.

\begin{align}
&\text{minimize} & &f_0(x) & \\\
&\text{subject to} & &f_i(x) \leq b_i, & i = 1,...,m.
\end{align}

The above problem is the general optimization problem where $\boldsymbol{x} = (x_1, ..., x_n)$ is the _optimization variable_ with $f_0$ being the _objective function_ and $f_i$ being the _constraint functions_. The vector $\boldsymbol{x^*}$ is _optimal_ when it satisties all the conditions as well as attaining the minimum value for the objective function.

Here the _objective function_ is thought of as the cost of choosing the variable $\boldsymbol{x}$ while it maintains strict rules for the variable $\boldsymbol{x}$ defined under the _constraint functions_. This problem could be linear or nonlinear depending on the objective function, having said this I would like take this moment to point that although many of problems have different methods of solving depending on linearity of the problem defined. Optimization problems are typically differentiated by the convexity of the problem, which we will define in a sooner post.

## Applications

Again I would like to attempt to explain this in my own words;

Energy is a physical quantity which every system tends to minimize whenever it attains its equilibrium position. The objective function is exactly the same, its a representation of the requirement that the energy of the system is minimized. Though I haven't explicity stated it, we believe that the entire system is defined by and only the variable $\boldsymbol{x}$. There are no other possible values to explain the state mentioned above, this is a limitation to the solution of the problem defined above but its important to notice when the set is well defined the _optimal solution_ can consider the whole system. The _constraint functions_ represents other design/requirments that the optimal solution to satisfy, this could be explained as safety factor considerations in mechanical engineering, while it could be a limit on bank money for a financial problem.

Some extracts from the Boyd book are attached below;

{{< blockquote >}}
In portfolio optimization, for example, we seek the best way to invest some
capital in a set of n assets. The variable x i represents the investment in the ith
asset, so the vector x ∈ R n describes the overall portfolio allocation across the set of
assets. The constraints might represent a limit on the budget (i.e., a limit on the
total amount to be invested), the requirement that investments are nonnegative
(assuming short positions are not allowed), and a minimum acceptable value of
expected return for the whole portfolio. The objective or cost function might be
a measure of the overall risk or variance of the portfolio return. In this case,
the optimization problem (1.1) corresponds to choosing a portfolio allocation that
minimizes risk, among all possible allocations that meet the firm requirements.
{{< /blockquote>}}

{{< blockquote >}}
Another example is device sizing in electronic design, which is the task of choos-
ing the width and length of each device in an electronic circuit. Here the variables
represent the widths and lengths of the devices. The constraints represent a va-
riety of engineering requirements, such as limits on the device sizes imposed by
the manufacturing process, timing requirements that ensure that the circuit can
operate reliably at a specified speed, and a limit on the total area of the circuit. A
common objective in a device sizing problem is the total power consumed by the
circuit. The optimization problem (1.1) is to find the device sizes that satisfy the
design requirements (on manufacturability, timing, and area) and are most power
efficient.
{{< /blockquote>}}

{{<blockquote>}}
An amazing variety of practical problems involving decision making (or system
design, analysis, and operation) can be cast in the form of a mathematical opti-
mization problem, or some variation such as a multicriterion optimization problem.
Indeed, mathematical optimization has become an important tool in many areas.
It is widely used in engineering, in electronic design automation, automatic con-
trol systems, and optimal design problems arising in civil, chemical, mechanical,
and aerospace engineering. Optimization is used for problems arising in network
design and operation, finance, supply chain management, scheduling, and many
other areas. The list of applications is still steadily expanding.
{{</blockquote>}}

## Future positions

In future posts I will attempt to provide justice to the class of problems known as Convex optimization problems, using methods such as interior point methods. Interior points methods appear to solve practical problems and are very reliable. I will attempt to provide heuristic for the the general non-convex problems while explaining similar heuristics for local optimization and bounds for global optimization. During the entirety of this blog posts I will be using the python library called cvxopt created and maintained by Martin Andersen (martin.skovgaard.andersen@gmail.com), Joachim Dahl (dahl.joachim@gmail.com), and Lieven Vandenberghe (vandenbe@ee.ucla.edu).
