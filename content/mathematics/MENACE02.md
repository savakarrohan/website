---
title: "MENACE"
Date: 2022-04-20T17:42:09+05:30
Draft: false
# layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: A Mechanical computer to learn the game of tic-tac toe
inspiration: Inspired by Matthew Scroggs Blog
author: Savakar Rohan #if any collaboration
shortDescription: Reward the computer by increasing balls count if favourable, while reprimand it by removing balls if the state is not good.
tags:
  - Mechanical
  - Computer
  - Learning
  - tic-tac-toe
  - noughts&crosses
  - Donald
  - Mitchie
  - noughts&crosses
_links:
  - https://www.mscroggs.co.uk/blog/
  - https://people.csail.mit.edu/brooks/idocs/matchbox.pdf
  - http://cs.williams.edu/~freund/cs136-073/GardnerHexapawn.pdf
# img01: #all images so easier to write ; img/01_Menace/01_tic-tac-toe.png
# img02:
# img03:
---

Lets take a moment to revise everything so far;

- We learnt that we tend to **reward** good behaviour while **reprimanding** unfavourable ones.
- We learnt that states represent the factors which influence a person's decision.
- We learnt that the most recent state effects the players future decisions more than previous states

## The actual computer

Now to the dirty business, how shall we make this computer?
We saw that the states are independent of each other and primarily a decision is based purely out of the most recent state, so it makes sense to have **containers** of all the possible states. How will we make a decision for the next possible state? Let's imagine that each of these **containers** contained the probability of making a future decision. That is they contained information regarding which move to play next in the form of probability. Now how shall we represent this probability, the answer is quite simple, let's pick differently **coloured balls** from a closed bad.

The computer is slowly taking shape, we now have to add the algorithm for rewarding and reprimanding.
The game ends in three scenarios for any player { Win, Loss, Draw}. When we win let's reward the computer by increasing the probability that he wins again. How do we do that you may ask? Well we can do two things, either increase the number of the particular colour balls in the bag or decrease the other colour balls in the bag. Just because it's rewarding let's choose the first option of **increase coloured ball count**. Though I would be very happy to study what happens in the other scenario too. At the same time let's reprimand the computer by **removing balls of the particular colour** whenever it loses. Draw seem to be a slightly more positive reward than a negative one, so lets reward it by increasing the coloured ball count but not by as much if it had won.

The architecture of the computer has been deveolped now what are the equivalent parts?

- The containers are matchboxes.
- The balls are different coloured beads representing each move possible.
- A reward is provided by increasing the number of coloured bead by 3.
  - For example: if in state:01 the red bead is picked and the game is terminated as a win by MENACE we add 3 additional red coloured beads in the respective state:01 box.
- Similarly a reprimand is accomodated by decreasing the number of coloured bead by 1.
  - For example: if in state:01 a green bead is picked and the game terminates as a loss to MENACE we remove the picked green bead from the respective state:01 box.
- A draw is considered by rewarding the coloured bead by 1.
