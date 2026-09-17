---
title: 'Untrusted Quantum Relay Study Notes'
description: 'A study note about a paper on qkd with untrusted quantum relay nodes'
pubDate: 'Sep 16 2026'
updatedDate: 'Sep 17 2026'
heroImage: '../../assets/poe.jpg'
---

## Quantum Key Distribution with Untrusted Relay Nodes - A Solution With Single Photon Source Quantum Dot ##

### Introduction ###

This study note is mainly based on my reading of [this paper](https://www.nature.com/articles/s41567-025-03005-5?fromPaywallRec=false). What interest me the most from this paper is the fact that it uses untrusted quantum relay nodes. To my knowledge, the most common already implemented quantum network are done based on trusted relay node [ref](https://www.nature.com/articles/s41586-020-03093-8).

### Background ###
Quantum communication over long distance suffers from decoherence. In classical communication, the problem of signal loss over long distance are solved through the use of relay and repeater. Unfortunately the classical relay and repeater could not be implemented for quantum communication because of **no-cloning theorem**. To solve this problem, quantum repeater is proposed as a solution. But quantum repeater requires advances in quantum memory, non destructive measurement and many other key technologies that does not make it feasible at the moment.

### Phase Matching Quantum Key Distribution ### 

This paper achieves secure key distribution between users through the implementation of Phase Matching Quantum Key Distribution (PM-QKD). It follows the method outlined in this [paper](https://journals.aps.org/prx/abstract/10.1103/PhysRevX.8.031043) but it replaces the central relay node with three intermediate relay nodes that consist of 2 Bell state measurement nodes and single photon source node. PM-QKD itself is a variant of Twin Field Quantum Key Distribution(TF-QKD) which by itself is a variant of Measurement Device Independent Quantum Key Distribution. The advantage of TF-QKD over MDI-QKD is that it can retain coherency over longer distance when compared to MDI-QKD (**citation needed**). 

### Central relay node to distributed intermediate relay nodes ###
One implication of replacing the central relay nodes with 2 bell state measurement nodes and a single photon source generator node is that it has the potential to be more scalable than the central model. In this model, the loss of coherent light from each user is only affected by the fiber length to their respective bell state measurement node. While interference in the measurement node is also affected by the transmission loss of the single photon source to the measurement node, both of these transmission loss are independent of each other. Fiber transmission loss also grows exponentially.

Though the main scalability of this innovation is mainly about enhancing the transmission distance scalability of the network, I am curious if this method can be generalized to multiplexed communication between multiple users and what are the consequences of scaling to multiple users.
