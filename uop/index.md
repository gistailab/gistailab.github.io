---
title: "Learning to Place Unseen Objects Stably using a Large-scale Simulation"
---

<center>
<h1 style="display: block;">Learning to Place Unseen Objects Stably using a Large-scale Simulation</h1>
RA-L submitted <br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;"><a href="https://">Sangjun Noh</a><sup>*,1</sup></td>     <!-- TODO: add email -->
        <td style="border: none;"><a href="https://">Raeyoung Kang</a><sup>*,1</sup></td>   <!-- TODO: add email -->
        <td style="border: none;"><a href="https://">Taewon Kim</a><sup>*,1</sup></td>      <!-- TODO: add email -->
        <td style="border: none;"><a href="https://">Seunghyeok Back</a><sup>1</sup></td>   <!-- TODO: add email -->
        <td style="border: none;"><a href="https://">Seongho Bak</a><sup>1</sup></td>       <!-- TODO: add email -->
        <td style="border: none;"><a href="https://">Kyoobin Lee</a><sup>†, 1</sup></td>    <!-- TODO: add email -->
    </tr>
</table>
<br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;"><sup>*</sup>These authors contributed equally to the paper</td>
        <td style="border: none;"><sup>†</sup>Corresponding author</td>
        <td style="border: none;"><sup>1</sup>Gwangju Institute of Science and Technology (GIST)</td>
    </tr>
</table>
<br>
<table style="border: none; display: initial;">
    <tr style="border: none;">
        <td style="border: none;">
            <a href="https://" style="color: #ffffff">                      <!-- TODO: add arxiv -->
                <div class="link_button">
                    <i class="bi bi-file-earmark-richtext"></i> Paper
                </div>
            </a>
        </td>
        <td style="border: none; display: initial;">
            <a href="https://" style="color: #ffffff">                      <!-- TODO: add code -->
                <div class="link_button">
                    <i class="bi bi-github"></i> Code
                </div>
            </a>
        </td>
        <td style="border: none;">
            <a href="https://" style="color: #ffffff">                      <!-- TODO: add video -->
                <div class="link_button">
                    <i class="bi bi-youtube"></i> Video
                </div>
            </a>
        </td>
    </tr>
</table>
<br>
<video width="100%" autoplay muted loop>
    <source src="./assets/~~~~.mp4" type="video/mp4">                       <!-- TODO: add sample video -->
    Your browser does not support the video tag.
</video> 
</center>

# Abstract 

Object placement is a crucial task for robots in unstructured environments as it enables them to manipulate and arrange objects safely and efficiently. However, existing methods for object placement have limitations, such as the requirement for a complete 3D model of the object or the inability to handle complex object shapes, which restrict the applicability of robots in unstructured scenarios. In this paper, we propose an Unseen Object Placement (UOP) method that directly detects stable planes of an unseen object from a single-view and partial point cloud. We trained our model on large-scale simulation data to generalize over relationships between the shape and properties of stable planes with a 3D point cloud. We verify our approach through simulations and real-world robot experiments, demonstrating state-of-the-art performance for placing single-view and partial objects. Our UOP approach enables robots to place objects stably, even when the object's shape and properties are not fully known, providing a promising solution for object placement in unstructured environments. Our research has potential applications in various domains such as manufacturing, logistics, and home automation. We will release our code, dataset upon publication.


# Citation

```
@article{sang2023learning,
  title={Learning to Place Unseen Objects Stably using a Large-scale Simulation},
  author={Sangjun Noh, Raeyoung Kang, Taewon Kim, Seunghyeok Back, Seongho Bak, Kyoobin Lee},
  journal={arXiv preprint arXiv:},
  year={2023}
}
```

# Acknowledgements

This work was fully supported by the Korea Institute for Advancement of Technology (KIAT) grant funded by the Korea Government (MOTIE) (Project Name: Shared autonomy based on deep reinforcement learning for responding intelligently to unfixed environments such as robotic assembly tasks, Project Number: 20008613). 
This work was also partially supported by the HPC Support project of the Korea Ministry of Science and ICT and NIPA.
