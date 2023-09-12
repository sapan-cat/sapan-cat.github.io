---
layout: page
mathjax: true
title: CAT Navigation
permalink: /work/cat_navigation/
---

Table of Contents:
- [ToDos](#todos)
- [Planning Stand-ups](#planning-stand-ups)
  - [Sept 11, 2023](#sept-11-2023)
  - [Sept 05, 2023](#sept-05-2023)
- [Planning Knowledge Sharing (Weekly)](#planning-knowledge-sharing-weekly)
  - [Sept 05, 2023](#sept-05-2023-1)
  - [August 15, 2023](#august-15-2023)
- [Aug 30, 2023 Meeting with Sagar](#aug-30-2023-meeting-with-sagar)

## ToDos
!!! danger **High**
    1. [Sept 05, 2023: Check the operator manual for the features](#sept-05-2023)
    2. [Sept 11, 2023: Complete the definitions for the metric calculations](#sept-11-2023)
    3. [Sept 11, 2023: Write unit test for the compute methods](#sept-11-2023)

!!! warning **Medium**
    1. [Sept 11, 2023: Based on the inputs & uses cases find the flow of information](#sept-11-2023)

!!! todo **Low**
    1. [Sept 11, 2023: Write the input parser](#sept-11-2023)
    2. [Sept 11, 2023: Test against the bag file](#sept-11-2023)

!!! done **Completed**
    1. [Sept 11, 2023: Metric Calculator code clean-up](#sept-05-2023)
    2. [Sept 08, 2023: Rebase sanford_tt_dev with mbot](#sept-05-2023)
    3. [Sept 08, 2023: Define the inputs/outputs to the input parser module in Trajectory Evaluator](#sept-05-2023)
    4. [Sept 07 2023: Merge v3.2.0 navigation release into mbot](#sept-05-2023)
    5. [Sept 06, 2023: Define the inputs to the metric calculator](#sept-05-2023)
    6. [Sept 05, 2023: Metric Container code clean-ups, PR ready](#sept-05-2023)

## Planning Stand-ups

### Sept 11, 2023
!!! todo Trajectory Evaluation
    1. Based on the inputs & uses cases find the flow of information
    2. Complete the definitions for the metric calculations
    3. Write unit test for the compute methods
    4. Write the input parser
    5. Test against the bag file 

### Sept 05, 2023
!!! todo Trajectory Evaluation
    1. Define the inputs to the metric calculator
    2. Define the inputs/outputs to the input parser module in Trajectory Evaluator
    3. Metric Container code clean-ups, PR ready
    4. Metric Calculator code clean-up

!!! todo Sanford Test Track
    1. Merge v3.2.0 navigation release into mbot
    2. Rebase sanford_tt_dev with mbot
    3. Check the operator manual for the features

## Planning Knowledge Sharing (Weekly)

### Sept 05, 2023
1. Dam project: Semi-autonomous loading & dumping
   1. Early next year
2. TrajEval
   1. In backwards,
   2. Target Date: End of Nov for UfH
   3. Get list of questions 
   4. Nov - Metrics computation 

### August 15, 2023
1. [AHS 101](https://caterpillar.sharepoint.com/:w:/r/teams/1APlanning251Group/Shared%20Documents/Navigation/Knowledge%20Center/AHS%20101.docx?d=w656c29c64f9047d19dd3c3b3b8793d39&csf=1&web=1&e=OEN4Tv)
2. UQ Planner
   1. [Receding Horizon Control Framework - Kianoosh's PhD Thesis](https://caterpillar.sharepoint.com/:b:/r/teams/1APlanning251Group/Shared%20Documents/Navigation/Knowledge%20Center/Kianoosh_PhD_Thesis.pdf?csf=1&web=1&e=no3w5B) 
   2. Tree Search Vs Graph Search

## Aug 30, 2023 Meeting with Sagar
1. [AIS LOG Analysis Tools]()
2. OCS - Operator Control Station Visualizer 
3. LogProcessor - Analysis tool for hlogs
   1. need to define what to read
4. Amendments 
   1. We can amend computed_trajectory 
5. Log Processor can handle multiple logs
6. Reproducing an issue
   1. Scenerio Generation ? 
7. Determinism
   1. Create a state of a task (node) and save it in log
   2. check point in log
   3. At task level, not differentiated in hlogs
8. Synthetic Bookmarks
   1. Run Task with log data and ammend new data in the same log
9. Apply Patch -> modify existing channel (topic)
10. Challenges
    1.  Channels 
    2.  Amend the log from the diterministic Task
11. ROS -> AIS channel conversion available
12. Task
    1.  Read Odom message from hlog
    2.  Path that robot was trying to follow
    3.  Cross Track - tracks the error from the centerline
    4.  Slope, bank, traction, parameters, compute time
13. Vehicle Observer Task
    1.  Driving Quality
    2.  What are the metrics that are being computed inside the VOT ?
14. Minestar - Offline Planning -> Lane 
    1.  Find Path to drive 
    2.  Obstacle Avoidance -> stops for obstacle & it doesn't do it itself. Safety requirement needs the machine to be stopped. And manual trigger is required to continue. PEZ control room has to publish the zone so that truck know it can drive around an obstacle.
15. Another application - WheelLoader - global Planner
