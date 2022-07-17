---
title: "Hiking Equipment"
Date: 2022-07-05T23:02:08+05:30
Draft: false
layout: #select between art, contact, engineering, mathematics, optimization, sports
attention: Hiking equipment have to be durable, light weight and most importantly safe for the treachorous terrain and weather that nature has to offer us at the foot of  mountains. I do my best to explain calculations and design considerations in preparing tent stakes.
inspiration: #Inspiration
author: Savakar Rohan #if any collaboration
shortDescription: Hiking equipment have to be durable, light weight and most importantly safe for the treachorous terrain and weather that nature has to offer us at the foot of  mountains. I do my best to explain calculations and design considerations in preparing tent stakes.
tags:
  - Sports
  - Hiking
  - Draw out
  - Force
  - Screw
  - Tent
  - Stakes
_links:
  - https://www.engineeringtoolbox.com/wood-screws-allowable-withdrawal-load-d_1815.html
  - http://www.thetentlab.com/stakesncords/stakesandcords.html
  - https://www.outdoorgearlab.com/topics/camping-and-hiking/best-tent-stakes
img01: #all images so easier to write ; img/01_Menace/01_tic-tac-toe.png
img02:
img03:
math: True
---

# Trekking equipment

It's a cold monsoon afternoon, you are up in the mountains, and you have carried your backpack and equipment for well over 6 hours and you are planning to set camp at this flat spot you found beside the stream. You slowly unpack the bag and notice your equipment, you check if they are suitable for this location, and you ponder over how did you manage to carry so much that morning. Then you slowly notice the tiny designs which seem so important, from the numerous straps on a backpack to that groove on your shoes to strap your spikes and even how compact you can pack your tent.

I recently went on a trek to the Himalayas and had goosebumps all over me as I took in the marvelous views on my way to the Beas Kund, a lake near the seven sisters' peak where Veda Vyasa is said to have written the epic poem Mahabharath. On my way to the peak, I was continuously astonished by the simple and innovative methods to carry equipment. They folded into position as though they were puzzles to be solved. As they took shape it was artistic like Origami, taking shape from a nearly flat surface.

I found myself interested in how these pieces of equipment were made, from the shoes which didn't transfer shock from jumping on to jagged rocks to the tent pipes folding neatly when packing but not buckling during gusty winds to even the various types of stakes I found. In this post, I wish to do justice by commenting on the various design consideration to partake in when designing these stakes.

## Step 1: Loading

The first critical step in any design process is answering the question of how this piece will be used. In our mechanical sense, this would mean what are the possible loading conditions of this piece. The various types of loading can be broken down into Tensile, Compressive, Shear, or Bending. These are usually broken down further into the various components represented by $ F_i $ and $ M_i $. Now for a tent, there are a few loads that the tent experience, these being lift loads (Wind swooshes below the tent surface and the pressure differences pushes the tent upwards) and shear loads as the gusty wind blows across the face of the tent (The typical formula $ F = \frac{1}{2} \rho v^2 L_d A\_{Projected} $ quantifies and explains the nature of this load).

## Step 2: Design (Topology)

There are many design methodologies for creating any device but I would like to decide the general shape of the stake. Now clearly, the amount of surface the part is exposed to in the surface would be proportional to the pull-out force of the stake. Thus clearly, the length of the stake and the number of fins will affect its quality. At the same time, the increase in the number of fins will make it difficult to penetrate the surface. What about the surface? Could something be accommodated for surfaces like sand and snow? At the same time could cost-cutting measures be accommodated for manufacturing?

For surfaces like sand whose physics is determined by multi-granular physics (A story for a different post). From experience we know it behaves very much like a fluid and I would like to point to a design that takes advantage of this property.

The holes in the main structure allow the grains to form a rope between the two ends and prevent the stake from being pulled out.

The larger surface area of the screw types allows for a greater pull-out force in surfaces such as snow.

## Step 3: Deciding on shape (Dimension) and material

There's a very interesting case in structural mechanics that says in beam bending the stress is proportional to the geometry of the material and not dependent on the material itself $ \(\frac{M_bc}{I}\) $. This is a very important point in itself. In this discussion, I will look into two cases of failure, and decide the appropriate dimensions for two types of stakes, the rod-type and the one with 3 fins.

In hindsight, for the below calculations, I will require material properties and will take appropriate values for Aluminium and Titanium which I will specify later.

## Design considerations

{{< postimage "ColouredImage.png" "Fig 01: stakes" >}}

### Case 01: Pry out force

Either of the stakes should not pry out during usage in the rocky soil medium by lift loads caused by wind.
Lift load:

- The number of stakes for a tent: 8
- Pry out formula (Empirical): $ 1.6x10^4 (S.G) D L $
- The specific gravity of soil: 2.75
- D, Dimension characteristic of cross section: $ 4\* Area / Perimeter $
- Wind lift load: 800 N (_Calculated from the formula explained in the paragraph above._)

Assumptions:

- Only 75% of the entire length of stake is in medium,
- The angle of stake doesn't affect pry out,
- Failure of the ground material such as coning out is not considered.
- All stakes are sufficiently separated.

Thus the load on each stake will be $ 100N $. For a rod of 5mm diameter we get that the minimum length should be $ 26.7cm $ Similarly calculating for the 3 fin stake we get that the minimum length of the stake should be $16.6cm $. **Though the masses are comparable of both the designs, its important to note that the fin shape will be shorter which will definetly help in packaging the equipment.** This is clear from the formula but a quantification makes this discussion more valid. Handling a 30cm stake would be much more difficult as compared to handling a short 15cm stake. I imagine the scenario as follows, its much easier to keep a 15cm scale in a pencil box whereas the 30cm scale which I kept in my backpack always broke (Fractured).

{{< postimage "AllStakesIso.png" "Fig 02: CAD modeled stakes" >}}

### Case 02: Column buckling during impact load

This case is considered to prevent the equipment from being damaged during usage. An impact load from a hammer should not cause significant column buckling deflection. We shall quantify which material would be a better choice.

- Max Deflection: 3mm
- Hammer mass: 1kg
- Impact height: 150mm

Using the Buckling formula (shown below) we can estimate the buckling load required for the two materials. This load is for when one end is fixed while the other end is free.

\begin{equation}
P\_{critical,buckling}= \frac{\pi^2 E I}{(2L)^2}
\end{equation}

Applying the above formulae we see that the critical load for Titanium $(2069N)$ is twice more than that for Aluminium $(1252N)$.

As the loading is an impact load from the hammer it is important to find the value of this load also. This relation is calculated from equating the energy imparted by the hammer to the workdone by material when deformed. The relation is shown below for completion where the symbols have appropriate meanings. upon calculating for the two materials the impact force is $250 \pm 30 N$.

\begin{equation}
F\_{impact} = W\left( 1 + \sqrt{1 + \frac{2 h A E}{W L}} \right)
\end{equation}

As is clear the impact load is an order less than that for buckling failure. Thus the device will not fail on impact, but we also notice that the failure criteria for titanium is 8 times the impact load therefore will be less likely to bend significantly. (Evident from comparing stiffness also). Thus the choice of titanium is better when we want long lasting equipment. Further buisness constraints such as manufacturing cost makes this material less viable.

The above discussion might seem redundant, as via intuition we know that as area increases so does the pry out force. We also very well know that titanium is stiffer and thus is the material of choice. The scope of this discussion was to quantify the values and provide some basic calculations which might be applied when designing such equipment and I hope it provides an insight.
