---
title: "Rubiks"
Date: 2022-06-07T22:48:18+05:30
Draft: false
layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: This toy which eats countless brains is a marvel of mathematics, engineering and design. A small introduction in to the algorithms required to solve this fantabulous device.
inspiration: Inspired when I realised that a 5x5x5 cube could be broken down to a 3x3x3 cube as a (1+3+1)x(1+3+1)x(1+3+1) cube.
author: Savakar Rohan #if any collaboration
shortDescription: # Description
tags:
  - Ernő Rubik
  - Rubiks Cube
  - Mathematics
  - Group Theory
  - Probabilities
  - Sport
  - Speed cubing
  - God's number
  - Cube
  - Cube Lovers
  -
_links:
  - https://www.jaapsch.net/puzzles/patents/gb1344259.pdf
  - https://en.wikipedia.org/wiki/Rubik%27s_Cube
  - https://cjme.springeropen.com/articles/10.1186/s10033-018-0269-7
  - https://web.mit.edu/sp.268/www/rubik.pdf
  - https://ocw.mit.edu/courses/es-268-the-mathematics-in-toys-and-games-spring-2010/
  - https://diglib.eg.org/bitstream/handle/10.2312/eurova20191119/019-023.pdf?sequence=1&isAllowed=n
  - https://arxiv.org/abs/0803.3435
  - http://www.math.rwth-aachen.de/~Martin.Schoenert/Cube-Lovers/michael_reid__superflip_requires_20_face_turns.html
  - https://www.chrome.com/cubelab#experiment
  - http://kociemba.org/cube.htm
# img01: img/01_Menace/01_tic-tac-toe.png   #front home page card image
# img02:                                    #main card on blog post image
# img03:                                    #Additional just in case.
math: True
---

## Introduction

The Rubik's cube is a 3D - combination puzzle invented in 1974 by a Hungarian sculptor and professor of architecture Ernő Rubik. It was initially called the magic cube but as the toy slowly became an international sensation the business men marketed it as the Rubik's cube, a much more catchy name. The cube comprises of 6 faces of different color where a solved state of the cube occurs when all the faces of the cube has a single color.

## Construction and counting the "Permutations" on a cube

The cube is constructed with 3 different set of pieces. The first piece has a single face and thus a single color on it, called the center piece. The second set of pieces have two faces and thus two colors, called the edge piece. The third set of pieces are made from the corner pieces, which are called the corner pieces. A trivial notice of the rubiks cube or dismantling the cube shows us that the center piece is a never moving piece. That is all the center pieces are in a fixed and solved state, this brings a lot of interesting takes on the solving of the cube as this piece of information could be used as a reference. I would like to point out at this point of time that the centre piece is only present in the odd numbered cubes.

Having learnt that there are three different sets/ groups of pieces which have to be moved, it makes sense to consider that these groups move individually. Though this should be the case (because each group has a different number of colors on it) the mechanism of the cube prevents a single(odd) exchange of pieces within and between the groups.

_Note: I will consider this point in the final section of this calculation._

\begin{equation}
P\_{Center} \cdot P\_{Corner} \cdot P\_{Edge} \cdot P\_{Factor} = \text{Total Permutation of Cube}
\end{equation}

### Center pieces

A simple dismantling of the classic rubiks cube shows us that the center pieces are rigidly connected to each other, though each of the faces of these pieces are permitted to rotate about their connections. Thus there is only a single way in which the centre pieces can be permuted.

{{< postimage "Dismantled.png" "Fig 01:  The centre piece has a fixed relationship with the other pieces." >}}

Although the face of these pieces are permitted to be rotated, these pieces do not move/ change position relative to one another.

\begin{align}
P\_{Center} = 1
\end{align}

### Edge pieces

The edge peice consists of 2 faces each with different colours. These pieces can be located at 12 different locations on the cube. Four locations on each layer of the cube. With 12 locations and 12 pieces the number of ways these pieces may be arranged legally is $12!$. Each piece having two faces can then be placed in 2 ways but because a t least one of the pieces has to be in a fixed orientation we will have $2^{11}$ such arrangements.

_Note: Each of the events mentioned above are separate independent events. That is edge position and edge color are independent of each other. This might not be the case in other games/puzzles_

\begin{align}
P\_{position} \cdot P\_{color} &= P\_{Edge} \\\
P\_{Edge} &= 12! \times 2^{11}
\end{align}

### Corner pieces

The corner peices consist of 3 faces each with different colours. These pieces can be located 8 different locations on the cube. Four each on the Down and Up layers of the cube. Moving forward similarly as the above explanation, we have $8!$ arrangments with the corner pieces and a total of $3^7$ possible orientations for the faces of the cube.

\begin{align}
P\_{position} \cdot P\_{color} &= P\_{Corner} \\\
P\_{Corner} &= 8! \times 3^{7}
\end{align}

### Factor

The mechanism of the cube restricts the only two edges or two corners only swapping. This thus brings out that only even permutations of the groups are allowed thus the factor to be included here is $\frac{1}{2}$.

\begin{align}
P\_{Factor} &= \frac{1}{2}
\end{align}

_Note: At this point I would like to point that a direct swapping between 2 edges or only 2 corners only is not feasible but a swap with an edge and a corner group is feasible._

### The number

Bringing all the numbers together we get:
\begin{align}
P\_{Center} \cdot P\_{Corner}\cdot P\_{Edge}\cdot P\_{Factor} &= \text{Total Permutation of Cube} \\\
1 \times 8! \times 3^{7} \times 12! \times 2^{11} \times \frac{1}{2} &= 43,252,003,274,489,856,000
\end{align}

These are the number of ways that a legal rubiks cube can be present in. That is how a legal cube could be arranged by rotation of its faces by $90^o , 180^o $. A cube could be dismantled and put back together in a haphazard manner, this would mean that the $P\_{Factor}$ term is neglected and thus the "Total Arrangments of a cube" will be two times "Total Permutation of Cube". These cubes may or may not be solvable.

### Visualisation

This section is taken directly from wikipedia and is very well written.

{{<blockquote>}}
To put this into perspective, if one had one standard-sized Rubik's Cube for each permutation, one could cover the Earth's surface 275 times, or stack them in a tower 261 light-years high.
{{</blockquote>}}

Just a massive number I know.

I hope to go through the above mentioned links and even explain how the mechanism of the cube forces even permutations only in a future post.
