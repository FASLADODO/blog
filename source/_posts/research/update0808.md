---
title: update of Ersin's work
date: 2018-08-08 09:00:00
comments: true
tags:
     - dqn-radar 
categories: 
    - research
    - dqn-radar
---
I change the codes (see in https://github.com/yujianyuanhaha/Ersin) a little bit as below:
1. adding load python module commands into ```RunSimulations.m``` script to make setup easier,
2. put off the learning time of dqn, like line 677 of ```RadarMDPSim.m``` script
3. more description in respect README.md file
I also present some preliminary results with 1000 NumRuns as attachments, approximate take ~5 min on my laptop. By the way, I also plan to run it on ARC to generate more results recently.  
![mdp](/content/images/lab/0808dqn.jpeg)
![dqn](/content/images/lab/0808mdp.jpeg)


 ## follow up  
 <span style="color:blue"> *the result could be wrong, in that mdp train thousand of times and test one instance, while dqn is ONLINE trained all the time* </span> 

## To Do List
- [ ] run case