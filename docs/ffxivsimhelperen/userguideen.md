---
title: User Guide - Various Scenarios Where FFXIV SimHelper Can Help You
parent: FFXIV Simhelper 
layout: home
nav_order: 2
---

# 0. Brief Introduction of FFXIV SimHelper 

FFXIV SimHelper is an application to find out meta jobs and learn them quickly.

We have decided to launch the program so that users can easily adapt to the environment of FFXIV,

showing visualized combat data relayed only on the user's senses 

How?
---

* Individual Job Guide: 

It helps users **to adapt in various jobs.** 

![beginner](../../images/ffxivsimhelperguide1.png)

* Compare Various Party Compositions: 

Quickly figures out which jobs is **the best fit** for our team.

![compare](../../images/ffxivsimhelperguide2.png)

* Compare all Gearsets: 

Even at the same item level, **priorities might change depending on gear combinations.**

Out of numerous mixtures, **Simhelper tells which suits best for the user.** 

![gearcompare](../../images/ffxivsimhelperguide3.png)

## Notice:

Simhelper mainly focuses on **improving the job proficiency of beginner & intermediate users**
   * Because Simhelper aims to make significant comparisons between similar equipment, **it is difficult to consider every variables of each job.**

   * Unlike other RPGs, cycle changes depending on each raid members, which requires an AI technology.

   * Due to practical issues, AI technology issues are left as a future task.


# 1. User Guide 

## Beginner-level: Learn Your Job Quickly using FFXIV SimHelper

As users hit max level, Simhelper provides **the average DPS for their current gearset and gives various data that helps them reach those goals.** 

These features makes it easy to directly compare performances with other players who wear simliar item levels.

## Quick Simulation

1) Click on **Quick Sim**

![startquicksim](../../images/ffxivsimhelperguide4.png)

2) Find out the current gearset you are wearing. 

(**!!!** For jobs that have an optimal GCD range such as Monk, make sure you set your GCD is inside that range to be accurate.") 

![equipments](../../images/ffxivsimhelperguide5.png)

3) Input your gearset and other options into the application **and delete all party members**

**(To remove party composition buffs and raidbuff effects)**

![target dummy](../../images/ffxivsimhelperguide6.png)

4) Compare the actual in-game DPS(using "ACTS") with the simulation results

**(Difference of 1-2% should not matter a lot, due to crit/dh and procs)**

![comparison](../../images/ffxivsimhelperguide7.png)

5) If your DPS isn't close to the simulation result, compare the damage log of the ACT. 

**(Ping and frame rates affect your GCD in the actual game, so check if simhelper is missing an important skill cast such as Phantom Rush, missing combo skills, etc)**

![comparison2](../../images/ffxivsimhelperguide8.png)

6) If you have any confusion about the job rotation, you can refer to the "Rotation Sample".

![comparison3](../../images/ffxivsimhelperguide9.png)


# User Guide 2. Intermediate-level: Analyze Raid Prog/Clears
* In the early weeks of Savage, there's a huge difference in gear progression between players, depending on how lucky you were with your rolls. This makes it hard to compare your logs to other people's logs directly. SimHelper can help you in these situations by showing your expected DPS in your current gearset.

* ex) a 10-minute M2S Clear Log 

![equipments2](../../images/ffxivsimhelperguide10.png)


## Analyze My Fflog Encounter with SimHelper 

1) Click on "Quick Analysis" 

![startquicksim](../../images/ffxivsimhelperguide4.png)

2) Input your gearset, your party composition, and the estimated party ilvl.

![input2](../../images/ffxivsimhelperguide11.png)

3) Compare SimHelper's DPS analysis with your log's DPS 

![input3](../../images/ffxivsimhelperguide13.png)


* !!! The simulation rotation sample doesn't take into account kill time, so it goes with the most general rotation. In the log I cast Raiton 22 times because I knew the fight won't give another burst window and used my last two charges of Raiton as soon as they were ready. SimHelper doesn't know that, so it pools the two Raitons so that it can use it at the 10-minute burst window.

# User Guide 3. Optimize Your Current Gearset 

As mentioned above, in the early weeks of savage there's a huge difference in gear progression between players. 

SimHelper can help find the best setting "for your current gear status" so that you can be as sharp as possible every week.

## Scenario
It's week 2 of Savage, so you collected 900 tomes - **you want to decide whether to buy a tome chest or legs.**

1) Go to "Gear Compare"

![gc](../../images/ffxivsimhelperguide15.png)

2) Input one gearset as the state you will be after you buy the tome chest, and the other as the state you will be after you buy the legs and simulate in any party composition.

![gearcompare](../../images/ffxivsimhelperguide14.png)

3) SimHelper proves buying legs is the better choice, which was the safer bet since our chest was an ornate one with 5 54-materia slots.

![gearcompare](../../images/ffxivsimhelperguide16.png)

4) So you buy the legs. Now you wonder what materia you should meld to get the best output. Go to "Stat Weights" and simulate your gearset without melding the legs. 

![statcompare](../../images/ffxivsimhelperguide17.png)

5) Stat Weights Result says Critical Strike is the best option. Meld both slot with Critical Strike. (the 0.89 value of Critical Strike means **your RDPS is expected to increase by 0.89 for every Critical Strike stat point you obtain.**)

![statcompare2](../../images/ffxivsimhelperguide18.png)

* !!! **It is recommended leave only a few slots open when running Stat Weights, since substat's efficiency changes depending on how much of that stat you have already.**


# User Guide 4. Find the Best Composition for Parsing
We all know buff jobs like DNC and NIN's performance rely heavily on party composition. FFXIV SimHelper can help you visualize exactly how much the difference is. 

1) Use "Best Partner" to find jobs that contribute the most to your buffs. 

![bestpartner](../../images/ffxivsimhelperguide19.png)

---

![synergy](../../images/ffxivsimhelperguide20.png)

2) Best Partner gives you relative values because of calculation limits. You can figure out exactly how much the difference is between different compositions using Quick Sim. 

* When we simulate in Quick Sim with High/Low scoring party comps, we can see **NIN's RDPS is 1.5% higher when in the higher party comp.**

![ffxiv](../../images/ffxivsimhelperguide21.png)



# User Guide 5. Other Uses - Solve Curiosities Using SimHelper 

There's many more uses for FFXIV SimHelper other than the general use cases mentioned above.

## How Much DPS Increase do Pots Give You?

* You can test by running one sim with "use pots" off and the other one on. - **For Ninja, we can see that using pots give you a 1.7%-2% damage increase.**

![nin](../../images/ffxivsimhelperguide22.png)

## How Much DPS Increase does Food Give You? 

* Simulate with "food" input empty. **You can see that food is a 1% damage increase for a Ninja.** Thus we can also conclude that pots give more damage increase than food.

![nin](../../images/ffxivsimhelperguide23.png)

Just like these examples, you can test with the SimHelper to collect data about things that you've been curious about!