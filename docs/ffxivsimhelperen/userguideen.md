---
title: User Guide - Various Scenarios Where FFXIV SimHelper Can Help You
parent: FFXIV Simhelper 
layout: home
nav_order: 2
---

# 0. Brief Introduction of FFXIV SimHelper 

FFXIV SimHelper was originally built as a tool for our Static(One & Done) to quickly find out meta jobs and learn them. I later decided to make it public and fixed the UI to make it more accessible.

Given its history, the tool focuses on the following needs our static had:

* Individual Job Guide: **provite multi-layer data for Players with Entry/Intermediate Understanding of the Job to help them improve quickly.** 

![beginner](../../images/ffxivsimhelperguide1.png)

* Compare Various Party Compositions: **Quickly experiment which jobs in the needed role fit the best for our team.**

![compare](../../images/ffxivsimhelperguide2.png)

* Compare Very Similar Gearsets: in the Gear Farming Stage(Savage week 1-4)/and after Farm 

![gearcompare](../../images/ffxivsimhelperguide3.png)

I'm sure these needs our static had will have a lot in common with the needs of other players in the FFXIV community who enjoy high-level combat content. However, one important thing must be said before we begin our user guide: 

**The tool is focused more on making the beginner/intermediate players better than making the already "advanced" level players "perfect"**
   * After experiencing end game content of various MMORPGS, one thing was clear to me: **the complexity of FFXIV's speedrun-level endgame combat is unmatched, since raidbuffs make the perfect DPS rotation a group effort instead of an individual one.** 
   * To handle such complex DPS rotation, advance Machine Learning/AI technology such as Reinforced Learning must be used, but this is marked as a task for future, since the amount of work it takes to create a Data Pipeline and train AI models is beyond what one individual programmer can do( much help is appreciated!!! ns090200@gmail.com) 
   * Because of this, the tool focuses on making a rotation that is **"good enough" - which make gear comparision results within 0.1%-0.2%p difference trustworthy.** 

This doesn't mean that advanced-level users won't find anything worthy from this tool. The tool will provide you calculations results for curiosities you would have had for FFXIV Combat, giving you various insights of its system.

# User Guide 1. Beginner-level: Learn Your Job Quickly using FFXIV SimHelper(ACT needed)

When you finish leveling job, **you will have a gearset way inferior to the well-known BIS/Optimal Gearsets guide sites like The Balance Provide.**

This huge difference in gear makes it difficult to directly compare your performance with other players. You could do the target dummy trial, but **that also provides you with only the binary pass/fail "result" of your performance, not the "process" on how to improve it.** 

**FFXIV SimHelper can help you in these situations: it will tell you the appropriate DPS for your current gearset, and provide you with various data that will help you achieve that DPS.**

## Target Dummy Simulation

1) Click on "Quick Sim"

![startquicksim](../../images/ffxivsimhelperguide4.png)

2) In-game, open your equipment tab and check your current gearset. (!!! To make your practice as effective as possible, for jobs that have an optimal GCD range such as Monk make sure you set your GCD is inside that range.") 

![equipments](../../images/ffxivsimhelperguide5.png)

3) Input your gearset and other options into the app **and delete all party members(to remove party composition buffs and raidbuff effects)**

![target dummy](../../images/ffxivsimhelperguide6.png)

4) Using ACT, record your target dummy rotation for the length you configured into the App and compare your final DPS with the App's simulation result. **DPS difference of 1-2% shouldn't matter a lot, since FFXIV's combat has a lot of variance due to crit/dh and procs.**

![comparison](../../images/ffxivsimhelperguide7.png)

5) If your DPS isn't close to the simulation result, you can compare the ACT's damage log to the App's damage profile to check if you're missing something big in your damage profile. **Ping and frame rates affect your GCD in the actual game, so missing a few casts of your job's normal GCD combo probably isn't an issue. Check for big differences(missing an important skill cast like Phantom Rush, missing a combo skill 5times, ...)**

![comparison2](../../images/ffxivsimhelperguide8.png)

6) If you want to check if something is wrong in your understanding of the job's rotation, you can use the "Rotation Sample" tab.

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