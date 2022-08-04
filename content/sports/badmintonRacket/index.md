---
title: "Badminton Rackets' peculiar design"
Date: 2022-06-21T14:31:07+05:30
Draft: false
layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: Badminton is the fastest racket sport in the world, what are the recent design innovations which allow players to find that extra 0.01 milliseconds improvement in their performance.
inspiration: Weight saving on the connector between the handle and shaft of the latest Astrox series by Yonex.
author: Savakar Rohan #if any collaboration
shortDescription: Sports provide a fertile ground for innovation, the rules bring out creativity amongst enthusiasts to find that one factor to influence their victory. In the world of badminton, this discussion hopes to give ideas to qualify factors such as stiffness for the design and development of high performance rackets.
tags:
  - sports
  - Badminton
  - Racket
  - Carbon fibers
  - Design
  - Technical sports
  - Squash
  - materials
_links:
  - https://in.victorsport.com/badmintonaz/3632/Racket-basic-introduction-Part-2-shaftcap-grip-end-cap
  - https://in.victorsport.com/badmintonaz/3614/Racket-design-thinking-starts-from-How-the-game-is-played
  - https://odr.chalmers.se/handle/20.500.12380/250350
img01: #all images so easier to write ; img/01_Menace/01_tic-tac-toe.png
img02:
img03:
math: True
---

The world of sports is amazing, everyone is on a level playing field following the same set of rules and a participant or team attempts to do their best. In my personal opinion it's the perfect substitution to war. Much like how countries spend billions in their respective armed forces and technologies, sportspeople too spend their time finding that advantage over their opponent. I believe this is the primary reason why technology develops first in the armed forces and then quickly follows in to the world of sports.

Sporting equipment have slowly improved over the decades. The major step being the various lightweight materials namely carbon-fibre being manufacturable (_Note: Carbon fibre was first produced way back in the 19th century when Thomas Edison attempted to used signed and burnt strips of cotton as a material for the light bulb. The difficulty was in using the material to its full extent in mechanical designs._).

As the goal was to decrease the weight of the racket the important question being asked was where can we reduce it without affecting the performance. These questions were typically answered by experienced athletes who couldn't quantify the effects satisfactorily enough back to the engineers. This ineffienct form of communication caused most of the problems during the design process.

In this post I hope to review the design recommendation for the badminton racket and comment on the ideology behind these designs. Just as every other design the first question to answer is what are the possible loads on a badminton racket.

## What are the loads?

The game of badminton can be broken down in to 3 classes of shots;

- Power (Smash,Drive, Clear, Lift)
- Control (Defense, Push, Cross court, Drop(Backcourt))
- Slow (Drop)

Now the above categorization is slighlty ambiguous as the speed of the shuttle at which the game is played determines this categorization. I would like to point out that this grouping is generally agreed amongst the advanced players. The categorization also shows that the most important groups are the Control and the Power group.

### Power Group

The main goal of this shot is to transfer as much speed as possible to the shuttle in the shortes time possible. This is just a fancy way to say that we should maximise the force on the shuttle.

Now this is ideal to an engineer, we can now think of the badminton racket as a spring(Ideally this is a dynamic analysis). The equation of the force exerted by a spring of stiffness $(K)$ and displacement $(x)$ is given by:
\begin{equation}
\bar{F} = - K \bar{x}
\end{equation}
_Where the minus sign is incorporated to account for direction of deflection_
From the above equation there are two ways to increase the force on the shuttle. We could increase the initial displacement, or we could increase the stiffness of the badminton racket.

{{< postimage "spring.png" "Fig:01 Spring representation of racket" >}}

#### Case 01: Increase stiffness

Assuming that the power transferred by the player through the racket can be infinitely large, it's clear from the equation that an increase in the racket stiffness will in general increase the power (and thus the force) transferred on to the shuttle. Now in composites we can do this in a manner of ways, we could arange the plies in the composite in such a manner so as to increase the stiffness of the racket along the shaft. We could shorten the racket so as to increase the stiffness of the shaft. We could change the geometry of the head so as to increase the stiffness. Categorizing below are the above mentioned methods

**How to increase stiffness of racket?**

- Shorter racket
- Change direction of polymer plies
- Geometry modification, (I Beam)

#### Case 02: Increase displacement

These are where the nuances come in to play, the system events described above classify in to a dynamic system, where a player rotates(moves) the badminton racket and thus the racket has an inertial force being applied on it. At the same time the shuttle initially applies a load on the racket in a short span of time, the direction of this force quicly reverses direction to then be applied on the shuttle itself. Let's stop right there, now concentrating on the player applying a load on the racket by rotating it know it experiences a load. This load(rotational inertial) causes the racket to bend, and thus deflecting the tip of the racket head. Thus the higher the load(Effort/Power) applied by the player the greater the deflection and thus greater the force transferred to the shuttle.

Now now, theres another way to increase the deflection, intuitively its obvious that reducing the overall stiffness of the racket will increase the deflection. This is clearly countering the first case of increasing the stiffness. For beginners who can't transfer the load on to the racket, a lesser stiff racket is better as this will increase the power transferred during a smash shot. For advanced players though, who can efficiently transfer the load on the racket it's better to use a stiffer racket as excess deflection will hinder the control of the racket.

## Other Design considerations

I gave barely enough justice for the physics during a shot above(_I would like to reiterate that the situation is a dynamic situation and Inertial factors play a much more important role_). These might be valid for power but what about control and aerodynamic drag? In this section I hope to bring light to some design considerations which have been implemented for the same situations.

### Control Group

Control can be easily assesed as the amount a racket twists about it's shaft. Remember this is twist and that is related to the torsional stiffness which is related to the angle of deviation and not the normal stiffness (?). During a shot if the racket deflects by a greater angle the shuttle will not move as intended by the player. Therefore it's important that the torsional stiffness is maximised. These can be achieved by the orientation of the plies that the composites are placed in the shaft. Another technique of varying stiffness is during manufacturing of the shaft, the fibers could be rolled or could be coiled. The diagrams shown below represent these techniques during manufacturing.

{{< postimage "Rolled.png" "Fig 02: Rolled Type" >}}
{{< postimage "Coiled.png" "Fig 03: Coiled Type" >}}
{{< postimage "Table.png" "Table 01: Comparision" >}}

### Aerodynamic resistance

Aerodynamic resistance is an important characteristic of the racket, it is important that this resistance should be minimal. A smaller resistance would allow the racket to quickly slice through the air. A faster racket movement speed will be crucial during defensive shots. Defensive shots are almost always played with the backhand especially at the professional level. Thus it makes sense to have a different profile for one side of the racket. This is what people at Yonex have figured out as shown in the image below.

{{< postimage "RacketProfile.png" "Fig 04: Racket profile including the aerodynamic and strength part" >}}

### Weight savings

I recently noticed something quite special from the rackets, the shaft connector between the shaft and handle has been slightly modified. More material has been removed then a typical connector. Below is an image of the same.

{{< postimage "WeightSaving.png" "Fig 05: Weight savings of rackets" >}}
