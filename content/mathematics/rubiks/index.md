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
_links:
  - https://www.jaapsch.net/puzzles/patents/gb1344259.pdf
  - https://en.wikipedia.org/wiki/Rubik%27s_Cube
  - https://cjme.springeropen.com/articles/10.1186/s10033-018-0269-7
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
P\_{position} \cdot P\_{color} = P\_{Edge}
P\_{Edge} = 12! \times 2^{11}
\end{align}
