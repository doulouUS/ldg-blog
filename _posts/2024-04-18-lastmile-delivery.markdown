---
layout: post
title:  "Optimising last-mile deliveries using Reinforcement Learning."
date:   2024-04-18 13:03:20 +0200
tag:
- last-mile delivery
- reinforcement learning
---

> This a high level overview about a paper published in the Computers & Industrial Engineering journal. This is joint work with Chenhao Zhou, Jingxin Ma, Ek Peng Chew, and Loo Hay Lee at the National University of Singapore (NUS). I really want to thank Chenhao who kept pushing this work from my master thesis into this publishable paper.

> Link to ScienceDirect paper [here](https://www.sciencedirect.com/science/article/abs/pii/S0360835223004679). Feel free to reach out for a PDF copy of the paper.

The idea was started back in 2017 during my master of Engineering at NUS. The context is rather simple: a delivery truck needs to drop parcels at known locations while picking up other parcels at random locations, appearing over time. It is a variant of the well-known Vehicle Routing Problem (VRP) that seeks to find the shortest path to visit locations.

Though there exist many ways to tackle this problem, we first wanted to exploit an obvious source of expertise: can we create a model that reproduces delivery drivers' decisions? With such a model, we then moved on to further train it in a simulated environment with the hope of improving upon human performance.

The result? Driver decisions could be reproduced in 50% of the test cases. Even with this imperfect model, between 8 and 12% more jobs could be served in the simulated environment, compared to a simple strategy that consists in always going for the nearest delivery/pickup location.

These are academic results and of course, a proper real-world evaluation would be needed as a next step. It is important to note that in the growing logistics industry where margins are extremely low but volumes are large, small improvements can have important financial implications.

This is a fascinating problem with real-world impact and there would be so many things to try next: better data collection, multi-agent RL, more advanced RL algorithms, parallel and GPU-optimised implementation, deployment, UI/UX for planners and drivers, etc.