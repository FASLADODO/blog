---
title: Weekly Update - add policy-gradient on Cognitive-Radar and DSA-aided DQN-DSA
date: 2018-09-10 09:00:00
comments: true
tags:
     - dqn-radar
     - dqn-dsa 
categories: 
    - research
    - weekly update
---
# Cognitive Radar
* The ARC setup still stuck at ```import tensorflow error```, the expert of ARC seems lost patient on me and reply quite late, I have to open another ticket :( , hope it go through soon. The instructions of pbs bash or related commands would be released soon once it is setup.
* I take few minutes implement **Deep Policy Gradient(dpg)**. where you could set the *solver* as *dpg*. It reduce the computation time down ~ 33% compare to dqn, yet still cannot produce similiar result so far. It worth a try in the further work.
* some guidence is updated to adjust paras in dqn in [README.md](https://github.com/yujianyuanhaha/Ersin/blob/master/README.md).

# DQN-DSA
* dsa-aided dqn is implemented, which mean we prefer dsa-select action instead of random-select at begining stage. It seems it could accelerate the converge cast in current case.
* extra-memory dqn is implemented, yet it seems no signigficant benefits in convergecast speed.
* apart from current tiers dqn vs mdp, drqn vs pomdp, another exsiting method, namely [myopic](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5398950), claim to achieve nearly 66% utility of *2-state markov chain stochastic channel*, which could be a baseline to drqn, or give some hint when refining our learning nodes.
> Liu, Keqin, Qing Zhao, and Bhaskar Krishnamachari. "Dynamic multichannel access with imperfect channel state detection." IEEE Transactions on Signal Processing 58.5 (2010): 2795-2808.