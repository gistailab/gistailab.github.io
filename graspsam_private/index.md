---
title: "GraspSAM: When Segment Anything Model Meets Grasp Detection"
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
        GraspSAM: When Segment Anything Model Meets Grasp Detection<br>
    </h1>
    <br>
    <!-- published in in 24' IEEE RA-L <br> -->
    <!-- <br> -->
    <!-- Authors ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;"><a href="mailto:sangjun7@gm.gist.ac.kr">Sangjun Noh</a></td>
                <td style="border: none;"><a href="mailto:jongwonkim@gm.gist.ac.kr">Jongwon Kim</a></td>
                <td style="border: none;"><a href="mailto:namdongwoo@gm.gist.ac.kr">Dongwoo Nam</a></td>
                <td style="border: none;"><a href="mailto:shback@gm.gist.ac.kr">Seunghyeok Back</a></td>
                <td style="border: none;"><a href="mailto:raeyo@gm.gist.ac.kr">Raeyoung Kang</a></td>
                <td style="border: none;"><a href="mailto:kyoobinlee@gist.ac.kr">Kyoobin Lee</a><sup>†</sup></td>
            </tr>
        </tbody>
    </table>
    <br>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
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
    <br>
    <!-- Links ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <a href="https://arxiv.org/abs/2409.12521" style="color: #ffffff">
                        <div class="link_button">
                            <i class="bi bi-file-earmark-richtext"></i> Paper
                        </div>
                    </a>
                </td>
                <td style="border: none;"></td> <!-- intervals -->
                <td style="border: none; display: initial;">
                    <a href="https://github.com/gist-ailab/GraspSAM.git" style="color: #ffffff">
                        <div class="link_button">
                            <i class="bi bi-github"></i> Code
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
                <td style="border: none;">( Official code will be released )</td>
            </tr>
        </tbody>
    </table>
</center>

<br>
<br>
<br>
<br>

<!-- Paper contents ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ----      ---- ---- ---- ---- -->

# Abstract

  Grasp detection requires flexibility to handle objects of various shapes without relying on prior object knowledge, while also offering intuitive, user-guided control. In this paper, we introduce GraspSAM, an innovative extension of the Segment Anything Model (SAM) designed for prompt-driven and category-agnostic grasp detection. Unlike previous methods, which are often limited by small-scale training data, GraspSAM leverages SAM’s large-scale training and prompt-based segmentation capabilities to efficiently support both target-object and category-agnostic grasping. By utilizing adapters, learnable token embeddings, and a lightweight modified decoder, GraspSAM requires minimal fine-tuning to integrate object segmentation and grasp prediction into a unified framework. Our model achieves state-of-the-art (SOTA) performance across multiple datasets, including Jacquard, Grasp-Anything, and Grasp-Anything++. Extensive experiments demonstrate GraspSAM’s flexibility in handling different types of prompts (such as points, boxes, and language), highlighting its robustness and effectiveness in real-world robotic applications.


<br>
<br>
<br>
<br>

# GraspSAM Pipeline

<!-- TODO: add image -->

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/model.png" alt="GraspSAM Pipeline abs" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<br>
<br>
<br>
<br>


# GraspSAM Result

<!-- | Feature            | Start Speed      | Incremental Speed | Constant RAM Overhead | Cumulative CPU Costs | Battery Implications |
|--------------------|------------------|-------------------|-----------------------|----------------------|----------------------|
| Compile this file  | ~1s per 100k LOC | <500ms            | 0                     | on keyboad shortcut  | minimal              |
| Format this file   | <1s              | <1s               | 0                     | on keyboad shortcut  | minimal              |
| Format on Save     | <1s              | <1s               | 0                     | on save              | notable              |
| Jump to Definition | ~2s per 100k LOC | <100ms            | 100MB                 | on key stroke        | significant          |
| Find Usages        | ↑                | ↑                 | ↑                     | ↑                    | ↑                    |
| Bulk Rename        | ↑                | ↑                 | ↑                     | ↑                    | ↑                    | -->

<br>
<br>
<br>
<br>

<section class="section">
# Inference GrapSAM in Real World Video

<div style="float:left; width:47.1%; border: 0px solid rgba(5, 130, 255, 0.534);">
    <h2 class="title is-5">Prompt: 1point</h2>
    <div class="column is-five-fifths">
        <div class="columns is-centered">
            <video width="90%" controls>
                <source src="./assets/videos/real_1point.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> 
        </div>
    </div>
</div>

<div style=" float:right; width:49.8%; border: 0px solid black;">
    <h2 class="title is-5">Prompt: 10point</h2>
    <div class="column is-five-fifths">
        <div class="columns is-centered">
            <video width="90%" controls>
                <source src="./assets/videos/real_10point.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> 
        </div>
    </div>
</div>

<br>

<div style="float:left; width:47.1%; border: 0px solid rgba(5, 130, 255, 0.534);">
    <h2 class="title is-5">Prompt: Box</h2>
    <div class="column is-five-fifths">
        <div class="columns is-centered">
            <video width="80%" controls>
                <source src="./assets/videos/real_bbox.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> 
        </div>
    </div>
</div>

<div style=" float:right; width:49.8%; border: 0px solid black;">
    <h2 class="title is-5">Prompt: Language</h2>
    <div class="column is-five-fifths">
        <div class="columns is-centered">
            <video width="80%" controls>
                <source src="./assets/videos/real_grounding.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> 
        </div>
    </div>
</div>

<br>

<div style="float:left; width:47.1%; border: 0px solid rgba(5, 130, 255, 0.534);">
    <h2 class="title is-5">Prompt: Eye Gaze</h2>
    <div class="column is-five-fifths">
        <div class="columns is-centered">
            <video width="80%" controls>
                <source src="./assets/videos/real_gaze.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video> 
        </div>
    </div>
</div>

</section>

<br>
<br>
<br>
<br>


## Additional Inference Results

- **Grasp-Anything(Seen)**

<center>
<figcaption>"RGB      Prompt      Pred Mask      Pred Grasp      Grasp Quality Map"</figcaption>
<img src="./assets/images/graspanything/seen/5/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/7/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/15/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/38/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/42/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/902/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/seen/903/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>

<br>

- **Grasp-Anything(Unseen)**

<center>
<img src="./assets/images/graspanything/unseen/7/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/8/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/10/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/14/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/17/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/1002/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspanything/unseen/1053/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>

<br>

- **Armbench**

<center>
<img src="./assets/images/armbench/1/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/armbench/11/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/armbench/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/armbench/34/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/armbench/86/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/armbench/99/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>

<br>


- **GraspNet**

<center>
<img src="./assets/images/graspnet/5/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspnet/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspnet/89/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspnet/92/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/graspnet/98/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>

<br>


- **OCID**

<center>
<img src="./assets/images/ocid/2/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/9/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/28/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/34/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/38/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/53/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<center>
<img src="./assets/images/ocid/64/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>

<br>

<!-- - **Soap tray (Novel Household Object)**

<center>
<img src="./assets/image/additional_result/2_Soap tray (Novel Household Object).png" alt="Additional Result 2" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<br>

- **Duct tape (Novel Household Object)**

<center>
<img src="./assets/image/additional_result/3_Duct tape (Novel Household Object).png" alt="Additional Result 3" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<br>

- **Watering can (Novel Household Object)**

<center>
<img src="./assets/image/additional_result/4_Watering can (Novel Household Object).png" alt="Additional Result 4" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<br>

- **Wooden bowl (Novel Household Object)**

<center>
<img src="./assets/image/additional_result/5_Wooden bowl (Novel Household Object).png" alt="Additional Result 5" style="margin: 10px 20px 10px 0px;" width="75%"/>
</center>
<br> -->

<!-- <br> -->
<!-- <br> -->
<!-- <br> -->
<!-- <br> -->
<!-- <hr style="border: solid 1px #c80000;"> -->
<hr style="#c80000;">
<br>
<br>
<br>
<br>

# Citation

```
@article{noh2024graspsam,
  title={GraspSAM: When Segment Anything Model Meets Grasp Detection},
  author={Noh, Sangjun and Kim, Jongwon and Nam, Dongwoo and Back, Seunghyeok and Kang, Raeyoung and Lee, Kyoobin},
  journal={arXiv preprint arXiv:2409.12521},
  year={2024}
}
```

<br>
<br>
<br>
<br>

<!-- # Acknowledgements

  This work was fully supported by the Korea Institute for Advancement of Technology (KIAT) grant funded by the Korea Government (MOTIE) (Project Name: Shared autonomy based on deep reinforcement learning for responding intelligently to unfixed environments such as robotic assembly tasks, Project Number: 20008613).
  This work was also partially supported by the HPC Support project of the Korea Ministry of Science and ICT and NIPA. -->

<br>
<br>
<br>
<br>

# Author Contacts

<center>
Contact email to get more information on this project<br>
<!-- GIST 광주과학기술원 ([gist.ac.kr](https://www.gist.ac.kr/kr/main.html)) | AILAB GIST AILAB  -->
</center>
<center>
<!-- <img src="./assets/~.png" alt="AILAB GAER Logo" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br> -->
<img src="./assets/image/GIST-AILAB.png" alt="GIST-AILAB Logo" style="margin: 10px 20px 10px 0px;" width="40%"/>
<br>
</center>

<br>
<br>

<center>
    [ Address : Dasan Building (C9) 204/206 & Central Research Facilities (C11) 403, <br>
    123 Cheomdangwagi-ro, Buk-gu, Gwangju, 61005, Korea ]
</center>

<br>
<br>

<footer class="footer">
  <div class="container">
    <div class="content has-text-centered">
      <!-- <a class="icon-link"
         href="./static/videos/nerfies_paper.pdf">
        <i class="fas fa-file-pdf"></i>
      </a> -->
      <center>
        <a class="icon-link" href="https://github.com/keunhong" class="external-link" disabled>website format
            <i class="fab fa-github"></i>
        </a>
      </center>
    </div>
    <div class="columns is-centered">
      <div class="column is-8">
        <div class="content">
          <center>
          <p>
            This website format is licensed under <br>
            a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
          </p>
          </center>
          <!-- <p>
            This means you are free to borrow the <a
              href="https://github.com/nerfies/nerfies.github.io">source code</a> of this website,
            we just ask that you link back to this page in the footer.
            Please remember to remove the analytics code included in the header of the website which
            you do not want on your website.
          </p> -->
        </div>
      </div>
    </div>
  </div>
</footer>
