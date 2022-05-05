MENACE Data
===========

This folder contains all the data from when we took MENACE to Manchester Science Festival.

Stand-up Maths videos here:
https://youtu.be/R9c-_neaxeU
https://youtu.be/KcmjOtkULi4

In the CSV files, the moves/positions are given using the following numbers for the positions:

0|1|2
-+-+-
3|4|5
-+-+-
6|7|8

Each file starts with either `sat` (Saturday) or `sun` (Sunday). For each day, the following files are included:

DAY.png - A plot of the number of beads in the first box over time
DAY-same-axes.png - The same plot with the same axis scales on both days.
DAY-games.csv - The results of the games that day.
DAY-ending-bead-numbers.csv - The number of beads of each colour in the boxes at the end of each day.

DAY-games.csv
-------------
In this file contains the first two moves of each game (numbered using the key above) and the winner (Human, Draw, or MENACE).

DAY-ending-bead-numbers.csv
---------------------------
This file contains the numbers of beads in the boxes at the end of the day. The data is explained most easily with an example. For example, take the row:

(Move,0,1,2,3,4,5,6,7,8)
1,0,0,10,0,o,0,x,48,6

This box is on move 1, so is on the machine's second move (the moves are numbered 0 to 3).

Arranging the other numbers in this row like the key above gives:

0 0  10
0 o  0
x 48 6

This means that the box had

. . .
. o .
x . .

drawn on it and had

0 0  10
0 .  0
. 48 6

beads for the positions left at the end.
