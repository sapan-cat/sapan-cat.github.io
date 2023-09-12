---
layout: page
mathjax: true
title: CAT Planning
permalink: /work/cat_planning/
---

Table of Contents:
- [ToDos](#todos)
- [Section Meeting](#section-meeting)
  - [People](#people)
- [Planning Team Sync (Bi-Weekly)](#planning-team-sync-bi-weekly)
  - [August 31, 2023](#august-31-2023)
  - [August 17, 2023](#august-17-2023)
    - [Payam's Presentation](#payams-presentation)
    - [Questions on CfH, CfU Planning](#questions-on-cfh-cfu-planning)
- [](#)

## ToDos
!!! danger **High**
    1. [ ] Task 1

!!! warning **Medium**
    1. [ ] Task 1

!!! todo **Low**
    1. [ ] Task 1

!!! done **Completed**
    1. [ ] Task 1


## Section Meeting

### People
1. Incubator/Simulation Team
   1. Aram Ebtekar, Incubator team: simulation
   2. Colin Chen, Incubator team: simulation
   3. Jason Chiu,
   4. Nasa Rouf, Team Lead
   5. Venkata Dandibhotla, Incubation team: supporting applications using simulation
   6. Sanket Bachuwar, Incubator team: simulation
2. 1A Planning, Navigation
   1. Steve Daniluk: Team lead
   2. Payam Ghassemi: manuever manager, ML Project
   3. Spencer Davis: Perception, Controls, CfH program AHS, bringing legacy CAT Autonomy to 1aPlanning   
   4. Sapan Agrawal: Sanford Test Track Project, Trajectory Evaluation Suite 
   5. Sarthake Choudhar: Trajectory Evaluation Suite
3. 1A Planning, Terrain Planning
   1. Jeff Berry: Team Lead
   2. Kianoosh Naveh (2019), Terrain Planning: Hex, Wheel Loaders, Decision Making
   3. Samuels Bettens
4. Andrew Sucato, AIS group: 1A Interfaces 
5. Benjamin Hodel, Implement planning lead: buckets, blades, grippers, excavators, digcycle planner, application messages
6. Justin Peters
7. Ben Floyd
8. Louis Roy
9. Jeremy Vogel, Manager

## Planning Team Sync (Bi-Weekly)

### August 31, 2023

1. [Reusable Element 2023Q3 Road Show](https://caterpillar.sharepoint.com/:p:/r/teams/CatDevelopmentGroup2/_layouts/15/Doc.aspx?sourcedoc=%7B47A7E5BB-A6C7-4047-808E-FD524B964E0E%7D&file=devops-618105%20RE%20WS%202023Q3%20Road%20Show.pptx&action=edit&mobileredirect=true) -  Nicolas Vandapel

2. [Using V Models for Testing](https://insights.sei.cmu.edu/blog/using-v-models-for-testing/)

### August 17, 2023
#### Payam's Presentation
1. [Presentation](https://caterpillar.sharepoint.com/:p:/r/teams/1APlanning251Group/_layouts/15/Doc.aspx?sourcedoc=%7BA3BD6B1D-A71F-4654-B393-41F41E6074B4%7D&file=ml-terrain-manipulation-model.pptx&action=edit&mobileredirect=true)
2. [Technical Doc](https://dev.azure.com/CatDevelopment/1A%20Planning/_git/wl-dig-sim?path=/docs/ml_based_terrain_sim_approx_model.md&version=GBpayam/wl-ml&_a=preview)
3. Changing terrain using various machines with increasing complexity
4. Wheelloader: Where is the next location to dig ? DigCycle Planner  
5. Terrain Manipulation Model: Predicts how the terrain changes after digging given initial terrian, machine pose, etc
6. Terrain height is modelled as image
7. Use image to image models for solving the problem
8. (Q) How are the other inputs fed to the network other than the input terrain image ?
9. Autodig: moves straight in +X
10. (Q) How are labels generated ? 
11. (Q14) How do you quantitavily find if data is valid or invalid ? 
12. (Q) What are the training/testing accuracy ?
13. Any Bias-Variance tradeoff done to check if the model is overfitting to the training dataset ? 
14. Looks to me that the labels are generated for multiple digs cycles. And these machine poses are not fed into the model.
15. I didn't understand this part -> How does the model learn 

#### Questions on CfH, CfU Planning
1. Describing & documenting the navigation side.
2. What's the navigation architecture solution looks like ?
3. {A} Kontz & Phillip: Present AHS Planning Architecture
4. What is the vision for 1APlanning team 5 years later ?
5. What's the state of CfH, CfU Planning ? 
6. How can we align 1APlanning goals with current & future states of CfH/CfU ?
7. Payam link for AHS presentation videos.


## 

1. Ros node 
   1. that accepts the commands to send implement joint commands
   2. Given
      1. Angle of attack
      2. Goal position
   3. Find the path to move the robot to the 
   4. Obs Detection only -> Stop if obstacle in path
   5. Spline based path planning 
      1. Can be imposed curvaturing
      2. Bezier Curve
      3. Curvature limit
      4. limitation: cannot handle obstacle
   6. Lattice Planner  
