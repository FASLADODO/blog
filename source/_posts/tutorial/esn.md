---
title: echo state network
date: 2018-08-08 09:00:00
comments: true
tags:
     - esn
categories: 
    - tutorial
---
Echo state network is a simple version of recurrent neural network(RNN) and claim to learn temporal information well.  
Dr.Saad and Dr.Liu of Wireless VT has produce some pioneer work of apply ESN as a RL method to fix wireless communication issues, as these work shown below.
Hoever, they skip comparison with mdp or the popular DQN, neither provide detailed evaluation. Hence we plan to make the comparision of **DQN vs ESN** in the further work.


# survey
[Explorations in Echo State Networks](http://www.ai.rug.nl/~mwiering/Thesis_Adrian_Millea.pdf)


# lecuture
https://www.coursera.org/lecture/neural-networks/echo-state-networks-9-min-s1bdp

# open source in python
* https://github.com/cknd/pyESN
* ESN_MIMO_Symbol_Detection (by Dr. Liu) https://github.com/JohnJohnZhou/ESN_MIMO_v1


# publication
* (By Dr. Liu) S. Mosleh, L. Liu, C. Sahin, Y. Zheng, and Y. Yi, " Brain-Inspired Wireless Communications: Where Reservoir Computing Meets MIMO-OFDM", IEEE Transaction on Neural Networks and Learning Systems, Dec. 2017, DOI: 10.1109/TNNLS.2017.2766162 https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8169663
* (By Dr. Saad)Mozaffari, Mohammad, et al. "A tutorial on UAVs for wireless networks: Applications, challenges, and open problems." arXiv preprint arXiv:1803.00680 (2018).