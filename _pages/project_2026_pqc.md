---
layout: page
permalink: /post-quantum-cryptography-sdn/
title: "Post-Quantum Cryptography (PQC) Project"
nav: false
---

**Project description:**

We evaluate three quantum-safe cryptographic schemes in a software-defined network (SDN). In the first case, we use a simulation of the amortised cost of rekeying each scheme by building a Deep Reinforcement Learning solution. This is a direction that explores in this specific context the cost and practicality of schemes for this purpose.

I worked on post-quantum cryptography (PQC) cryptography during grad school, and had not seen much work in the specific cryptographic scheme within which I worked as a direction for this purpose. The project started as a directed project for the QWorld Qintern program where the scope of SDN and PQC was generally defined, and I found the direction of the specific schemes for evaluation under guidance of Professor Narwaria.

I hand-rolled one PQC scheme, and used libraries for the other two PQC schemes. I also built the deep learning model from scratch (with latency, simulation of traffic, etc). There are reference papers that served as the basis for the (1) deep learning scheme (2) the PQC scheme I wrote from scratch based on the mathematics delineated in a reference paper.

This particular problem matters because there are frequent threats against infrastructure systems that use SDN; railway systems, power grids and water systems. Additionally, the threat of quantum computing attacks such as Harvest Now, Decrypt Later (HNDL) means that with the arrival of fault-tolerant quantum computers, these are important security aspects to consider, as when these systems go down and there are effects (e.g. power outages, a breakdown of public transportation), they particularly affect marginalised communities most.

The project produced a publication (short paper) that is currently under review. Our larger goal is also to submit such work to a journal. (As such, I cannot (unfortunately) provide the github repo link until the review process has ended)

**Contributors:**
Krystal
