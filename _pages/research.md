---
permalink: /research/
title: "Research"
description: ""
keywords: "networked control, optimal control, neuromorphic sensing, information theory, homomorphic encryption, path integral control, deceptive control"
author_profile: false
redirect_from:
  - /research.html
---

We have several research projects across control, robotics, and information theory domains. The following diagram tries to capture our research trajectories and the story behind individual research projects. We hope the diagram is helpful in navigating through various exciting projects currently going on in our lab.
Although both of these fields are well-established on their own, it is surprisingly tricky to translate a concept from one field to another. One reason is that these subjects are rarely taught together in educational programs, resulting in distinct research cultures. To address this gap, I am developing a graduate-level course on Networked Control Systems, aiming to teach elements of these two subjects in a single semester.

![Research History](/images/research_history.png)

---

Networked Control Systems
======
Modern control systems are comprised of multiple decision-making components (sensors, computers, actuators) that communicate with each other over resource-limited networks. Such systems are commonly called Networked Control Systems (NCSs) to emphasize the interplay between control-theoretic and communication-theoretic design challenges inherent in such platforms. Conventionally, control algorithms and communication protocols are researched by separate communities. However, there are many situations in which the co-design of control and communication algorithms significantly improves the system-level performance. Our NSF project titled “Directed Information Theory for Networked Control Systems in Big Data Regime” aims to provide a systematic approach to such a co-design by a hybrid use of control and information theory.

![Architecture to minimize the feedback bit rate for Linear-Quadratic-Gaussian (LQG) optimal control [ISIT16, L-CSS22].](/images/ncs-1280x625.png)

As a canonical research challenge, we have been studying the problem of stochastic optimal control with a limited feedback data rate. Using directed information as the main theoretical vehicle, we develop specialized source coding schemes that enable task-aware, real-time data compression and transmission for control applications. Based on our early-stage work [[ISIT16](https://ieeexplore.ieee.org/document/7541729), [TAC17](https://ieeexplore.ieee.org/document/7546898), [TAC18](https://ieeexplore.ieee.org/abstract/document/7935462)], our recent focus is on the generalization to nonlinear [[TAC22](https://www.sciencedirect.com/science/article/abs/pii/S000510982300300X), [AUT23](https://ieeexplore.ieee.org/document/9388883)], online/adaptive [[JSAIT22](https://ieeexplore.ieee.org/document/10002900), CDC23], and multi-terminal [[TAC21](https://ieeexplore.ieee.org/document/9531489), [CISS21](https://ieeexplore.ieee.org/document/9400217), [RNC22](https://onlinelibrary.wiley.com/doi/abs/10.1002/rnc.6076)] networked control systems.

---

Neuromorphic Sensing
======
Neuromorphic vision sensors (event cameras) are characterized by their unique, bio-inspired pixel readout mechanisms that are fundamentally different from their conventional, frame-based counterparts. Frame-based cameras encode a dynamic visual scene as a sequence of static images I(t1), I(t2), · · · with periodic sampling times. In contrast, event cameras’ photoreceptor circuit arrays allow independent and asynchronous pixel readouts. Each pixel “fires” only when it detects a light intensity change beyond a given threshold and remains silent otherwise. Typical event cameras available today encode visual scenes using the so-called address-event representation (AER). In AER, each output packet from the camera is formatted as (x,y,p,t), where (x,y) indicates the pixel location where the “event” happened, p denotes polarity (single-bit information encoding whether the light intensity increased or decreased), and t encodes the timestamp.

Utilizing these unique features of neuromorphic vision sensors, we aim to develop a high-speed machine perception system that achieves less power, less data generation, and less computational cost. To unleash the full potential of neuromorphic cameras, we adopt systems & control theoretic perspectives [[COT23](https://arxiv.org/abs/2309.06504)]. Our long-term goal is to integrate neuromorphic sensors with neuromorphic computers to create a visual pathway similar to humans’ visual pathways.

![frame_and_neuro_pathways](/images/frame_and_neuro_pathways-1280x628.png)

---

Path Integral Control
======
Path integral control is a novel method of controlling a system under stochastic dynamics, originally introduced by H.J Kappen. Stochastic dynamics present a very unique set of challenges, making control much more complex than under deterministic dynamics. Optimal control strategies may qualitatively change under increased noise. In path integral control, the controller makes certain assumptions about the problem to reduce the non-linear and computationally intractable Hamilton-Jacobi-Bellman (HBJ) equations to a tractable and linear stochastic differential heat equation. Then, Monte Carlo sampling allows the controller to numerically solve for an approximation to the optimal control sequence.

We believe that path integral control has potential in the specific case of depetive control. In this problem, an attacker has hijacked a control system, inserting its own control inputs and replacing the sensor outputs observed by the controller. The simplest attack strategy is "Playback Loop" attack (as seen in every heist movie ever), where the attacker relays old recordings (or trivial permutations thereof) of safe system dynamics while applying unsafe control inputs. We are applying path integral control theory to the problem of detecting and defeating such attacks in real-time by applying a constant KL-Divergence-based hypothesis test to observations of the system. We aim to accomplish this by placing a "watermark" on the system controls and observing the effects. If observations diverge beyond tolerance from the expected effect of the watermarked control strategy, then we must conclude we are under attack. Of course, the watermark itself degrades control system performance, and is therefore a tradeoff between security and effectiveness. We intend to integrate this hypothesis testing into the cost function of path integral control to constantly maintain the ideal balance between system effectiveness and security.

![DeceptivePathIntegralControlDiagram](/images/DPIDiagram.png)

---

Privacy and Security in Control
======

Modern control systems are tightly integrated with computation and data exchanges over a shared network. This motivates us to investigate cryptographic security enhancement of networked control system. Our latest experiment (see below) successfully implemented the encrypted dynamic controller on stabilizing an inverted pendulum (see Figure and Video below). This is a challenging encrypted control task in several aspects. First, running a dynamic controller entirely on an encrypted state estimates requires the underlying cryptosystem to handle both addition and multiplication (fully homomorphic) and to maintain correct decryptions after a long iterative operation on ciphertexts without intermediate decryptions. Second, the computation time must be fast enough to meet a stringent real-time requirement imposed by the control task. Our rotary inverted pendulum required about 30 Hz sampling frequency for stabilization.

![Encrypted Control Diagram](/images/enc_dyn_control_figure_web.png)

Kalman Filter and linear quadratic regulator (LQR) were designed in advance, and we transformed the dynamic controller into an integerized system using the pole placement technique proposed in [KIM22]. Encryptions of the designed controller and data were performed using the LWE-GSW cryptosystem [Regev09, GSW13]. Our experiment was conducted using a rather restricted set of encryption parameters due to computation requirements. Nevertheless, to the best of our knowledge, this is the first successful physical demonstration of the encrypted dynamic controller using the LWE-GSW cryptosystem. Our experimental testbed will allow emerging future research in encrypted control to be readily tested and evaluated, which will help advance the field of secure control systems.

<iframe src="https://www.youtube.com/embed/UROEGujwwx8"></iframe>

---

Simultaneous Perception-Action Design (SPADE)
======

In [[AUT23]](https://www.sciencedirect.com/science/article/abs/pii/S000510982300300X), we study the problem of information-constrained path planning in finite state-space systems. We consider a variation of the standard Markov decision process (MDP), referred to as a perception MDP, in which the decision-maker is able to synthesize its own belief-dependent perception strategy in addition to its strategy for action selection. We refer to this joint synthesis procedure as the simultaneous perception-action design (SPADE) framework. To capture costs associated with sensing, we impose an information-theoretic perception cost that penalizes information flow from the environment to the decision-maker. We propose a novel method of invariant, finite belief sets (IFBS), in which the decision-maker operates exclusively on a representative sample of belief states. We provide conditions under which this sample of belief states remains invariant, and develop a computationally-efficient algorithm for solving the SPADE problem over this sample.↳

One application of the proposed SPADE framework is in the problem of strategic sensor selection, where the objective is to dynamically choose a subset of sensors such that the cumulative sensing error is minimized. Using the perception strategy obtained through solving the SPADE problem as a reference, the decision-maker chooses the subset of sensors whose combined observation function most closely matches it. Figure below on the left shows that, intuitively, as the relative cost of information increases, the number of selected sensors at each time step decreases. Furthermore, as shown in the table below, although requiring slightly more online computation time, our proposed sensor selection strategy is able to scale to more complicated sensor selection problems with only a modest performance loss relative to PBVI, a common algorithm for solving for an optimal strategy in a POMDP.


![SPADE](/images/Screen-Shot-2023-10-02-at-7.42.40-PM-4-1280x743.png)

---

Information Theory and Path Planning
======

We develop motion planning algorithms that enable “minimum sensing navigation.” In many robot navigation tasks, perception (sensing and data processing) is an expensive process. A natural approach to mitigating the perception cost is to generate a motion plan that is executable with minimum sensing effort. For example, the shortest path from the origin to the destination may not be the easiest path to follow – maybe you have to go through a narrow and uncertain passage (Path A in the following video) that requires extensive use of sensors. If the required perception cost is excessive, it makes more sense to choose an alternative, longer path that goes through a wide-open area (Path B in the video). Such a path may be followed with a moderate sensing effort, and the required perception cost can be saved.

To let our motion planning algorithm discover a path like B, we do not use the conventional Euclidean distance metric to measure the path length. Alternatively, we embed a non-Euclidean, information-geometric “distance” notion in which Path B looks shorter than Path A. The invention of such a “distance” notion is the core of our research contribution. To discover the shortest path with respect to this new “distance” function, we have developed RRT*- and PRM*-based numerical shortest path solvers thus far.

<iframe src="https://www.youtube.com/embed/5MHLmFykZ9I"></iframe>

---
