---
title: "GIST - AILAB paper project home"
---

<br>

# GIST AILAB

[Homepage](https://sites.google.com/view/gistailab)

[GitHub](https://github.com/gist-ailab)

[Youtube](https://www.youtube.com/@gistailab)

[Project page (This page)](https://gistailab.github.io/)

<br>

## Paper Projects

### GraspSAM: When Segment Anything Model Meets Grasp Detection (25' ICRA accepted)

[Project Page](https://gistailab.github.io/graspsam/) | [Paper](https://arxiv.org/abs/2409.12521)

Grasp detection requires flexibility to handle objects of various shapes without relying on prior object knowledge, while also offering intuitive, user-guided control. In this paper, we introduce GraspSAM, an innovative extension of the Segment Anything Model (SAM) designed for prompt-driven and category-agnostic grasp detection. Unlike previous methods, which are often limited by small-scale training data, GraspSAM leverages SAM’s large-scale training and prompt-based segmentation capabilities to efficiently support both target-object and category-agnostic grasping. By utilizing adapters, learnable token embeddings, and a lightweight modified decoder, GraspSAM requires minimal fine-tuning to integrate object segmentation and grasp prediction into a unified framework. Our model achieves state-of-the-art (SOTA) performance across multiple datasets, including Jacquard, Grasp-Anything, and Grasp-Anything++. Extensive experiments demonstrate GraspSAM’s flexibility in handling different types of prompts (such as points, boxes, and language), highlighting its robustness and effectiveness in real-world robotic applications.

### Learning to Place Unseen Objects Stably using a Large-scale Simulation (24' RA-L accepted)

[Project Page](https://gistailab.github.io/uop/) | [Paper-IEEEXplore](https://ieeexplore.ieee.org/document/10417128)

Object placement is a fundamental task for robots, yet it remains challenging for partially observed objects. Existing methods for object placement have limitations, such as the requirement for a complete 3D model of the object or the inability to handle complex shapes and novel objects, which restrict the applicability of robots in the real world. Our focus was on addressing the Unseen Object Placement (UOP) problem. We tackled the UOP problem using two methods: (1) UOP-Net, a point cloud segmentation based approach that directly detects the most stable plane from partial point clouds, and (2) UOP-Sim, a large-scale dataset to accommodate various shapes and novel objects. Our UOP approach enables robots to place objects stably, even when the object's shape and properties are not fully known, providing a promising solution for object placement in various environments. We verify our approach through simulation and real-world robot experiments, demonstrating state-of-the-art performance for placing single-view and partial objects. For comprehensive findings, please refer to https://gistailab.github.io/uop/.
