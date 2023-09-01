---
title: "00 Learning to Place Unseen Objects Stably using a Large-scale Simulation"
---

<br>

<center>
<h1 style="display: block;">Learning to Place Unseen Objects Stably using a Large-scale Simulation</h1>
RA-L submitted <br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;"><a href="mailto:sangjun7@gm.gist.ac.kr">Sangjun Noh</a><sup>*,1</sup></td>
        <td style="border: none;"><a href="mailto:raeyo@gm.gist.ac.kr">Raeyoung Kang</a><sup>*,1</sup></td>
        <td style="border: none;"><a href="mailto:ailab.ktw@gm.gist.ac.kr">Taewon Kim</a><sup>*,1</sup></td>
        <td style="border: none;"><a href="mailto:shback@gm.gist.ac.kr">Seunghyeok Back</a><sup>1</sup></td>
        <td style="border: none;"><a href="mailto:bakseongho@gm.gist.ac.kr">Seongho Bak</a><sup>1</sup></td>
        <td style="border: none;"><a href="mailto:kyoobinlee@gist.ac.kr">Kyoobin Lee</a><sup>†, 1</sup></td>
    </tr>
</table>
<br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;"><sup>*</sup>These authors contributed equally to the paper</td>
        <td style="border: none;"><sup>†</sup>Corresponding author</td>
    </tr>
    <sup>1</sup>Gwangju Institute of Science and Technology (GIST)<br>
</table>
<br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;">
            <a href="https://arxiv.org/abs/2303.08387" style="color: #ffffff">
                <div class="link_button">
                    <i class="bi bi-file-earmark-richtext"></i> Paper (preprint)
                </div>
            </a>
        </td>
        <td style="border: none; display: initial;">
            <a href="https://github.com/gist-ailab/uop-net" style="color: #ffffff">
                <div class="link_button">
                    <i class="bi bi-github"></i> Code (Github)
                </div>
            </a>
        </td>
        <td style="border: none;">
            <a href="https://www.youtube.com/watch?v=08F4jxSEL7A" style="color: #ffffff">
                <div class="link_button">
                    <i class="bi bi-youtube"></i> Video (Youtube)
                </div>
            </a>
        </td>
    </tr>
</table>
<br>
<video width="100%" autoplay muted loop>
    <!-- <source src="./assets/~~~~.mp4" type="video/mp4">                       TODO: add sample video -->
    <source src="https://www.youtube.com/watch?v=08F4jxSEL7A" type="video/mp4">                       <!-- TODO: add sample video -->
    Your browser does not support the video tag.
</video> 
</center>

# Abstract 

Object placement is a fundamental task for robots, yet it remains challenging for partially observed objects. Existing methods for object placement have limitations, such as the requirement for a complete 3D model of the object or the inability to handle complex shapes and novel objects, which restrict the applicability of robots in the real world. Our focus was on addressing the Unseen Object Placement (UOP) problem. We tackled the UOP problem using two methods: (1) UOP-Net, a point cloud segmentation based approach that directly detects the most stable plane from partial point clouds, and (2) UOP-Sim, a large-scale dataset to accommodate various shapes and novel objects. Our UOP approach enables robots to place objects stably, even when the object's shape and properties are not fully known, providing a promising solution for object placement in various environments. We verify our approach through simulation and real-world robot experiments, demonstrating state-of-the-art performance for placing single-view and partial objects. For comprehensive findings, please refer to https://sites.google.com/uop-net. (This page)

<br>

# UOP Pipeline

<br>

# Citation

```
@article{noh2023learning,
  title={Learning to Place Unseen Objects Stably using a Large-scale Simulation},
  author={Noh, Sangjun and Kang, Raeyoung and Kim, Taewon and Back, Seunghyeok and Bak, Seongho and Lee, Kyoobin},
  journal={arXiv preprint arXiv:2303.08387},
  year={2023}
}
```

<br>

# Acknowledgements

This work was fully supported by the Korea Institute for Advancement of Technology (KIAT) grant funded by the Korea Government (MOTIE) (Project Name: Shared autonomy based on deep reinforcement learning for responding intelligently to unfixed environments such as robotic assembly tasks, Project Number: 20008613). 
This work was also partially supported by the HPC Support project of the Korea Ministry of Science and ICT and NIPA.
