---
title: "04 Learning to Place Unseen Objects Stably using a Large-scale Simulation"
---
<br>
<head>
    <!-- <style>
        figure {
            border: 1px #cccccc solid;
            padding: 4px;
            margin: auto;
        }
        figcaption {
            background-color: black;
            color: white;
            font-style: italic;
            padding: 2px;
            text-align: center;
        }
        /* <figure>
            <img src="pic_trulli.jpg" alt="Trulli" style="width:100%">
            <figcaption>Fig.1 - Trulli, Puglia, Italy</figcaption>
        </figure> */
    </style> -->
    <!-- <style type="text/css">
        .avoid {
            page-break-inside: avoid !important;
            margin: 4px 0 4px 0;  /* to keep the page break from cutting too close to the text in the div */
        }
    </style> -->
    <!-- <img src="./assets/~.png" alt="AILAB GAER Logo" style="float: left; margin: 10px 20px 10px 0px;" width="40%"/> -->
</head>

<center>
    <h1 style="display: block;">
        Learning to Place Unseen Objects Stably<br>
        using a Large-scale Simulation
    </h1>
    RA-L submitted <br>
    <!-- Authors ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;"><a href="mailto:sangjun7@gm.gist.ac.kr">Sangjun Noh</a><sup>*,1</sup></td>
                <td style="border: none;"><a href="mailto:raeyo@gm.gist.ac.kr">Raeyoung Kang</a><sup>*,1</sup></td>
                <td style="border: none;"><a href="mailto:ailab.ktw@gm.gist.ac.kr">Taewon Kim</a><sup>*,1</sup></td>
                <td style="border: none;"><a href="mailto:shback@gm.gist.ac.kr">Seunghyeok Back</a><sup>1</sup></td>
                <td style="border: none;"><a href="mailto:bakseongho@gm.gist.ac.kr">Seongho Bak</a><sup>1</sup></td>
                <td style="border: none;"><a href="mailto:kyoobinlee@gist.ac.kr">Kyoobin Lee</a><sup>†, 1</sup></td>
            </tr>
        </tbody>
    </table>
    <br>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <sup>*</sup>These authors contributed equally to the paper
                </td>
                <td style="border: none;">
                    <sup>†</sup>Corresponding author
                </td>
            </tr>
        </tbody>
    </table>
    <br>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                    <sup>1</sup>Gwangju Institute of Science and Technology (GIST)
            </tr>
        </tbody>
    </table>
    <br>
    <!-- Links ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <a href="https://arxiv.org/abs/2303.08387" style="color: #ffffff">
                        <div class="link_button">
                            <!-- <center> -->
                            <i class="bi bi-file-earmark-richtext"></i> Paper
                            <!-- </center> -->
                        </div>
                    </a>
                </td>
                <td style="border: none;"></td> <!-- intervals -->
                <td style="border: none;"></td> <!-- intervals -->
                <td style="border: none; display: initial;">
                    <a href="https://github.com/gist-ailab/uop-net" style="color: #ffffff">
                        <div class="link_button">
                            <!-- <center> -->
                            <i class="bi bi-github"></i> Code 
                            <!-- </center> -->
                        </div>
                    </a>
                </td>
                <td style="border: none;"></td> <!-- intervals -->
                <td style="border: none;"></td> <!-- intervals -->
                <td style="border: none;">
                    <a href="https://www.youtube.com/watch?v=08F4jxSEL7A" style="color: #ffffff">
                        <div class="link_button">
                            <!-- <center> -->
                            <i class="bi bi-youtube"></i> Video 
                            <!-- </center> -->
                        </div>
                    </a>
                </td>
            </tr>
        </tbody>
    </table>
    <br>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">(Official code and dataset will be released at publication.)</td>
            </tr>
        </tbody>
    </table>
    <br>
    <br>
    <!-- PT video ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
    <video width="75%" controls autoplay muted loop>
        <source src="./assets/20230901_Home-DataGeneration_01.mp4" type="video/mp4">            <!-- TODO: add presentation video -->
        Your browser does not support the video tag.
    </video> 
</center>

<br>

<!-- Paper contents ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
# Abstract

Object placement is a fundamental task for robots, yet it remains challenging for partially observed objects. Existing methods for object placement have limitations, such as the requirement for a complete 3D model of the object or the inability to handle complex shapes and novel objects, which restrict the applicability of robots in the real world. Our focus was on addressing the Unseen Object Placement (UOP) problem. We tackled the UOP problem using two methods: (1) UOP-Net, a point cloud segmentation based approach that directly detects the most stable plane from partial point clouds, and (2) UOP-Sim, a large-scale dataset to accommodate various shapes and novel objects. Our UOP approach enables robots to place objects stably, even when the object's shape and properties are not fully known, providing a promising solution for object placement in various environments. We verify our approach through simulation and real-world robot experiments, demonstrating state-of-the-art performance for placing single-view and partial objects. For comprehensive findings, please refer to https://sites.google.com/uop-net. (This page)

<br>

# UOP Pipeline

<!-- TODO: add image -->
<center>
<img src="./assets/uop_pipeline/~.png" alt="uop_pipeline 1" style="margin: 10px 20px 10px 0px;" width="40%"/>
<img src="./assets/uop_pipeline/~.png" alt="uop_pipeline 2" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
</center>

<br>

# UOP-Sim Data Generataion

<center>
    <video width="75%" autoplay muted loop>
        <source src="./assets/20230901_Home-DataGeneration_01.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video> 
</center>

<br>

# Inference UOP-Net in Real World

## Comparison each Result with the YCB Object Set & Novel Household Objects

<!-- TODO: add gif image -->
<center>
<img src="./assets/image/inference_result/1_mustard.png" alt="Inference Result 1" style="margin: 10px 20px 10px 0px;" width="35%"/>
<img src="./assets/image/inference_result/1_mustard.gif" alt="Inference Result 1 gif" style="margin: 10px 20px 10px 0px;" width="60%"/>
<br>
<img src="./assets/image/inference_result/2_spam.png" alt="Inference Result 2" style="margin: 10px 20px 10px 0px;" width="35%"/>
<img src="./assets/image/inference_result/2_spam.gif" alt="Inference Result 2 gif" style="margin: 10px 20px 10px 0px;" width="60%"/>
<br>
<img src="./assets/image/inference_result/3_sugar_box.png" alt="Inference Result 3" style="margin: 10px 20px 10px 0px;" width="35%"/>
<img src="./assets/image/inference_result/3_sugar_box.gif" alt="Inference Result 3 gif" style="margin: 10px 20px 10px 0px;" width="60%"/>
<br>
<img src="./assets/image/inference_result/4_LEGO.png" alt="Inference Result 4" style="margin: 10px 20px 10px 0px;" width="35%"/>
<img src="./assets/image/inference_result/4_LEGO.gif" alt="Inference Result 4 gif" style="margin: 10px 20px 10px 0px;" width="60%"/>
<br>
<img src="./assets/image/inference_result/5_dinosaur.png" alt="Inference Result 5" style="margin: 10px 20px 10px 0px;" width="35%"/>
<img src="./assets/image/inference_result/5_dinosaur.gif" alt="Inference Result 5 gif" style="margin: 10px 20px 10px 0px;" width="60%"/>
<br>
</center>

<br>

## Additional Inference Results (pics)
<center>
<!-- TODO: add pic image -->
<img src="./assets/image/additional_result/~.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
<img src="./assets/image/additional_result/~.png" alt="Additional Result 2" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
<img src="./assets/image/additional_result/~.png" alt="Additional Result 3" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
<img src="./assets/image/additional_result/~.png" alt="Additional Result 4" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
<img src="./assets/image/additional_result/~.png" alt="Additional Result 5" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
</center>

<br>
<br>
<!-- <hr style="border: solid 1px #c80000;"> -->
<hr style="#c80000;">
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

<br>

# Authors & Contacts

<!-- TODO: add image -->
<center>
<img src="./assets/~.png" alt="AILAB GAER Logo" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
<img src="./assets/~.png" alt="GIST-AILAB Logo" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
</center>

<br>

<center>
    [ Address : Dasan Building (C9) 204/206 & Central Research Facilities (C11) 403, <br>
    123 Cheomdangwagi-ro, Buk-gu, Gwangju, 61005, Korea ]
</center>

