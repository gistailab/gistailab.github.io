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
                <td style="border: none;"><a href="https://scholar.google.co.kr/citations?user=tqylaI8AAAAJ&hl=ko&oi=ao"><sup>1</sup>Sangjun Noh</a></td>
                <td style="border: none;"><a href="https://scholar.google.co.kr/citations?hl=ko&user=VKULYHAAAAAJ"><sup>1</sup>Jongwon Kim</a></td>
                <td style="border: none;"><a href="https://scholar.google.com/citations?user=a7iMp8wAAAAJ&hl=ko&oi=sra"><sup>1</sup>Dongwoo Nam</a></td>
                <td style="border: none;"><a href="https://scholar.google.com/citations?user=N9dLZH4AAAAJ&hl=ko&oi=sra"><sup>1</sup>Seunghyeok Back</a></td>
                <td style="border: none;"><a href="https://scholar.google.com/citations?user=52DNwMIAAAAJ&hl=ko&oi=sra"><sup>1</sup>Raeyoung Kang</a></td>
                <td style="border: none;"><a href="https://scholar.google.com/citations?user=QVihy5MAAAAJ&hl=ko&oi=ao"><sup>1</sup>Kyoobin Lee</a><sup>†</sup></td>
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


<!-- -  **Grasp detection performance of each model given 10 points as prompt.** -->
<!-- | Methods            | Grasp-Anything        |             Grasp-Anything            |        Grasp-Anything                 | Jacquard            |              Jacquard           |         Jacquard                |
| :------------------ | :--------------------- | :----------------------- | :----------------------- | :---------------------- | :----------------------- | :----------------------- |
|          Methods          | Base                  | New                     | H                       | Base                   | New                     | H                       |
| GR-ConvNet*         | 0.68                  | 0.55                    | 0.61                    | 0.82                   | 0.61                    | 0.70                    |
| Det-Seg-Refine* | 0.58                  | 0.53                    | 0.55                    | 0.79                   | 0.55                    | 0.65                    |
| GG-CNN*             | 0.65                  | 0.53                    | 0.58                    | 0.73                   | 0.52                    | 0.61                    |
| LGD*                | 0.69                  | 0.57                    | 0.62                    | 0.83                   | 0.64                    | 0.72                    |
| GraspSAM-tiny (ours)| 0.78                  | 0.75                    | 0.77                    | **0.90**               | 0.81                    | **0.85**                |
| GraspSAM-t (ours)   | **0.83**              | **0.81**                | **0.82**                | 0.87                   | 0.75                    | 0.81                    | -->

<!-- ### **Grasp detection performance of each model given 10 points as prompt** -->
<h3 class="title is-3">Grasp detection with 10 points</h3>
<center>
<div style="text-align: center; margin: 0 auto;">
  <table style="width: 100%; margin: 0 auto; text-align: center;">
    <!-- <caption style="font-size: 1.5em;"><strong>Grasp detection performance of each model given 10 points as prompt</strong></caption> -->
    <tr>
      <th rowspan="2" style="width: 16.66%; border: 2px solid black;">Methods</th>
      <th colspan="3" style="width: 25%; border: 2px solid black;">Grasp-Anything <a href="https://arxiv.org/abs/2309.09818">[7]</a> </th>
      <th colspan="3" style="width: 25%; border: 2px solid black;">Jacquard <a href="https://ieeexplore.ieee.org/abstract/document/8593950">[6]</a> </th>
    </tr>
    <tr>
      <!-- <th style="width: 16.66%;"></th> -->
      <th style="width: 8.33%; border: 2px solid black;">Base</th>
      <th style="width: 8.33%; border: 2px solid black;">New</th>
      <th style="width: 8.33%; border: 2px solid black;">H</th>
      <th style="width: 8.33%; border: 2px solid black;">Base</th>
      <th style="width: 8.33%; border: 2px solid black;">New</th>
      <th style="width: 8.33%; border: 2px solid black;">H</th>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">GR-ConvNet* <a href="https://arxiv.org/abs/1909.04810">[3]</a> </td>
      <td style="width: 8.33%; border: 2px solid black;">0.68</td>
      <td style="width: 8.33%; border: 2px solid black;">0.55</td>
      <td style="width: 8.33%; border: 2px solid black;">0.61</td>
      <td style="width: 8.33%; border: 2px solid black;">0.82</td>
      <td style="width: 8.33%; border: 2px solid black;">0.61</td>
      <td style="width: 8.33%; border: 2px solid black;">0.70</td>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">Det-Seg-Refine* <a href="https://arxiv.org/abs/2107.05287">[4]</a> </td>
      <td style="width: 8.33%; border: 2px solid black;">0.58</td>
      <td style="width: 8.33%; border: 2px solid black;">0.53</td>
      <td style="width: 8.33%; border: 2px solid black;">0.55</td>
      <td style="width: 8.33%; border: 2px solid black;">0.79</td>
      <td style="width: 8.33%; border: 2px solid black;">0.55</td>
      <td style="width: 8.33%; border: 2px solid black;">0.65</td>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">GG-CNN* <a href="https://arxiv.org/abs/1804.05172">[2]</a> </td>
      <td style="width: 8.33%; border: 2px solid black;">0.65</td>
      <td style="width: 8.33%; border: 2px solid black;">0.53</td>
      <td style="width: 8.33%; border: 2px solid black;">0.58</td>
      <td style="width: 8.33%; border: 2px solid black;">0.73</td>
      <td style="width: 8.33%; border: 2px solid black;">0.52</td>
      <td style="width: 8.33%; border: 2px solid black;">0.61</td>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">LGD* <a href="https://arxiv.org/abs/2406.09489">[8]</a> </td>
      <td style="width: 8.33%; border: 2px solid black;">0.69</td>
      <td style="width: 8.33%; border: 2px solid black;">0.57</td>
      <td style="width: 8.33%; border: 2px solid black;">0.62</td>
      <td style="width: 8.33%; border: 2px solid black;">0.83</td>
      <td style="width: 8.33%; border: 2px solid black;">0.64</td>
      <td style="width: 8.33%; border: 2px solid black;">0.72</td>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">GraspSAM-tiny (ours)</td>
      <td style="width: 8.33%; border: 2px solid black;">0.78</td>
      <td style="width: 8.33%; border: 2px solid black;">0.75</td>
      <td style="width: 8.33%; border: 2px solid black;">0.77</td>
      <td style="width: 8.33%; border: 2px solid black;"><strong>0.90</strong></td>
      <td style="width: 8.33%; border: 2px solid black;">0.81</td>
      <td style="width: 8.33%; border: 2px solid black;"><strong>0.85</strong></td>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">GraspSAM-t (ours)</td>
      <td style="width: 8.33%; border: 2px solid black;"><strong>0.83</strong></td>
      <td style="width: 8.33%; border: 2px solid black;"><strong>0.81</strong></td>
      <td style="width: 8.33%; border: 2px solid black;"><strong>0.82</strong></td>
      <td style="width: 8.33%; border: 2px solid black;">0.87</td>
      <td style="width: 8.33%; border: 2px solid black;">0.75</td>
      <td style="width: 8.33%; border: 2px solid black;">0.81</td>
    </tr>
  </table>
</div>
</center>



<br>




<h3 class="title is-3">Category-agnostic Grasp Dection</h3>
<center>
<div style="text-align: center; margin: 0 auto;">
  <table style="width: 100%; margin: 0 auto; text-align: center;">
  <!-- <table style="width: 80%; margin: 0 auto; text-align: center; border-collapse: collapse; border: 3px solid black;"> -->
    <!-- <caption style="font-size: 1.5em;"><strong>Grasp detection performance comparison</strong></caption> -->
    <tr>
      <th rowspan="2" style="width: 16.66%; border: 2px solid black;">Methods</th>
      <th colspan="3" style="width: 25%; border: 2px solid black;">Grasp-Anything <a href="https://arxiv.org/abs/2309.09818">[7]</a> </th>
      <th colspan="3" style="width: 25%; border: 2px solid black;">Jacquard <a href="https://ieeexplore.ieee.org/abstract/document/8593950">[6]</a> </th>
    </tr>
    <tr>
      <th style="width: 8.33%; border: 2px solid black;">Base</th>
      <th style="width: 8.33%; border: 2px solid black;">New</th>
      <th style="width: 8.33%; border: 2px solid black;">H</th>
      <th style="width: 8.33%; border: 2px solid black;">Base</th>
      <th style="width: 8.33%; border: 2px solid black;">New</th>
      <th style="width: 8.33%; border: 2px solid black;">H</th>
    </tr>
    <tr>
      <td style="width: 16.66%; border: 2px solid black;">GR-ConvNet <a href="https://arxiv.org/abs/1909.04810">[3]</a> </td>
      <td style="width: 8.33%; border: 2px solid black;">0.75</td>
      <td style="width: 8.33%; border: 2px solid black;">0.61</td>
      <td style="width: 8.33%; border: 2px solid black;">0.67</td>
      <td style="width: 8.33%; border: 2px solid black;">0.88</td>
      <td style="width: 8.33%; border: 2px solid black;">0.66</td>
      <td style="width: 8.33%; border: 2px solid black;">0.75</td>
    </tr>
    <tr>
      <td style="border: 2px solid black;">Det-Seg-Refine <a href="https://arxiv.org/abs/2107.05287">[4]</a> </td>
      <td style="border: 2px solid black;">0.64</td>
      <td style="border: 2px solid black;">0.59</td>
      <td style="border: 2px solid black;">0.61</td>
      <td style="border: 2px solid black;">0.85</td>
      <td style="border: 2px solid black;">0.59</td>
      <td style="border: 2px solid black;">0.70</td>
    </tr>
    <tr>
      <td style="border: 2px solid black;">GG-CNN <a href="https://arxiv.org/abs/1804.05172">[2]</a> </td>
      <td style="border: 2px solid black;">0.72</td>
      <td style="border: 2px solid black;">0.59</td>
      <td style="border: 2px solid black;">0.65</td>
      <td style="border: 2px solid black;">0.78</td>
      <td style="border: 2px solid black;">0.56</td>
      <td style="border: 2px solid black;">0.65</td>
    </tr>
    <tr>
      <td style="border: 2px solid black;">LGD <a href="https://arxiv.org/abs/2406.09489">[8]</a> </td>
      <td style="border: 2px solid black;">0.77</td>
      <td style="border: 2px solid black;">0.65</td>
      <td style="border: 2px solid black;">0.70</td>
      <td style="border: 2px solid black;"><strong>0.89</strong></td>
      <td style="border: 2px solid black;">0.70</td>
      <td style="border: 2px solid black;">0.78</td>
    </tr>
    <tr>
      <td style="border: 2px solid black;"><strong>GraspSAM-tiny (ours)</strong></td>
      <td style="border: 2px solid black;">0.79</td>
      <td style="border: 2px solid black;">0.68</td>
      <td style="border: 2px solid black;">0.73</td>
      <td style="border: 2px solid black;">0.88</td>
      <td style="border: 2px solid black;"><strong>0.79</strong></td>
      <td style="border: 2px solid black;"><strong>0.83</strong></td>
    </tr>
    <tr>
      <td style="border: 2px solid black;"><strong>GraspSAM-t (ours)</strong></td>
      <td style="border: 2px solid black;"><strong>0.89</strong></td>
      <td style="border: 2px solid black;"><strong>0.82</strong></td>
      <td style="border: 2px solid black;"><strong>0.85</strong></td>
      <td style="border: 2px solid black;">0.83</td>
      <td style="border: 2px solid black;">0.72</td>
      <td style="border: 2px solid black;">0.77</td>
    </tr>
  </table>
</div>
</center>


<br>




<!-- -  **Grasp detection performance of each model given 10 points as prompt.** -->
<!-- | Methods                 | Grasp-anthing ++     |                       |                       |
| ----------------------- | ---------------------| --------------------- | --------------------- |
|                         | Base                 | New                   | H                     |
| CLIPORT                 | 0.36                 | 0.26                  | 0.29                  |
| CLIPGrasp               | 0.40                 | 0.29                  | 0.33                  |
| LGD                     | 0.48                 | 0.42                  | 0.45                  |
| GraspSAM w/ G.D (Ours)  | **0.64**             | **0.62**              | **0.63**              | -->

<!-- ### **Grasp dection performance comparison when using language as a prompt** -->
<h3 class="title is-3">Grasp dection with language</h3>
<center>
<!-- <div style="center; margin: 0 auto;"> -->
<table style="width: 60%; center;">
<!-- <caption style="font-size: 1.5em;"><strong>Grasp dection performance comparison when using language as a prompt</strong></caption> -->
<tr>
    <th rowspan="2" style="width: 40%; border: 2px solid black;">Methods</th>
    <th colspan="3" style="width: 60%; border: 2px solid black;">Grasp-anthing ++ <a href="https://arxiv.org/abs/2406.09489">[8]</a> </th>
</tr>
<tr>
    <!-- <th></th> -->
    <td style="width: 20%; border: 2px solid black;">Base</td>
    <td style="width: 20%; border: 2px solid black;">New</td>
    <td style="width: 20%; border: 2px solid black;">H</td>
</tr>
<tr>
    <td style="width: 40%; border: 2px solid black;">CLIPORT <a href="https://proceedings.mlr.press/v164/shridhar22a.html">[24]</a> </td>
    <td style="width: 20%; border: 2px solid black;">0.36</td>
    <td style="width: 20%; border: 2px solid black;">0.26</td>
    <td style="width: 20%; border: 2px solid black;">0.29</td>
</tr>
<tr>
    <td style="width: 40%; border: 2px solid black;">CLIPGrasp <a href="https://ieeexplore.ieee.org/abstract/document/10161041">[25]</a> </td>
    <td style="width: 20%; border: 2px solid black;">0.40</td>
    <td style="width: 20%; border: 2px solid black;">0.29</td>
    <td style="width: 20%; border: 2px solid black;">0.33</td>
</tr>
<tr>
    <td style="width: 40%; border: 2px solid black;">LGD <a href="https://arxiv.org/abs/2406.09489">[8]</a> </td>
    <td style="width: 20%; border: 2px solid black;">0.48</td>
    <td style="width: 20%; border: 2px solid black;">0.42</td>
    <td style="width: 20%; border: 2px solid black;">0.45</td>
</tr>
<tr>
    <td style="width: 40%; border: 2px solid black;"><strong>GraspSAM w/ G.D (Ours)</strong></td>
    <td style="width: 20%; border: 2px solid black;"><strong>0.64</strong></td>
    <td style="width: 20%; border: 2px solid black;"><strong>0.62</strong></td>
    <td style="width: 20%; border: 2px solid black;"><strong>0.63</strong></td>
</tr>
</table>
<!-- </div> -->
</center>


<br>
<br>
<br>
<br>


# Inference GrapSAM in Real World Video
<section class="section">
  <div class="columns is-centered has-text-centered">
      <div style="width:100%;">
        <!-- <div class="columns is-centered has-text-centered">
          <div class="column is-six-fifths">
            <h2 class="title is-3">Inference GrapSAM in Real World Video</h2> 
          </div>
        </div> -->
        <div style="float:left; width:49%; border: 0px solid rgba(5, 130, 255, 0.534);">
            <h3 class="title is-3">Prompt: 1point</h3>
            <div class="column is-five-fifths">
                <div class="columns is-centered">
                    <video width="90%" controls>
                        <source src="./assets/videos/real_1point.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video> 
                </div>
            </div>
        </div>
        <div style=" float:right; width:49%; border: 0px solid black;">
            <h3 class="title is-3">Prompt: 10points</h3>
            <div class="column is-five-fifths">
                <div class="columns is-centered">
                    <video width="90%" controls>
                        <source src="./assets/videos/real_10point.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video> 
                </div>
            </div>
        </div>
        <!-- <br> -->
        <br>
        <div style="float:left; width:49%; border: 0px solid rgba(5, 130, 255, 0.534);">
            <h3 class="title is-3">Prompt: Box</h3>
            <div class="column is-five-fifths">
                <div class="columns is-centered">
                    <video width="90%" controls>
                        <source src="./assets/videos/real_bbox.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video> 
                </div>
            </div>
        </div>
        <div style=" float:right; width:49%; border: 0px solid black;">
            <h3 class="title is-3">Prompt: Language</h3>
            <div class="column is-five-fifths">
                <div class="columns is-centered">
                    <video width="90%" controls>
                        <source src="./assets/videos/real_grounding.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video> 
                </div>
            </div>
        </div>
        <!-- <br> -->
        <br>
        <div style="float:left; width:49%; border: 0px solid rgba(5, 130, 255, 0.534);">
            <h3 class="title is-3">Prompt: Eye Gaze as Points</h3>
            <div class="column is-five-fifths">
                <div class="columns is-centered">
                    <video width="90%" controls>
                        <source src="./assets/videos/real_gaze1.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video> 
                </div>
            </div>
        </div>
      </div>
    </div>
</section>

<br>
<br>
<br>
<br>


# Additional Dataset Image Inference

<!-- - **Grasp-Anything(Seen)** -->
<h3 class="title is-3">Grasp-Anything(Seen)</h3>


<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <!-- <td  width="25%">RGB</td>
                <td  width="25%">Prompt</td>
                <td  width="25%">Mask</td>
                <td  width="25%">Grasp</td>
                <td  width="25%">Quality Map</td>
                <td  width="25%">RGB</td>
                <td  width="25%">Prompt</td>
                <td  width="25%">Mask</td>
                <td  width="25%">Grasp</td>
                <td  width="25%">Quality Map</td> -->
                <th style="font-size: 0.8em;">RGB</th>
                <th style="font-size: 0.8em;">Prompt</th>
                <th style="font-size: 0.8em;">Mask</th>
                <th style="font-size: 0.8em;">Grasp</th>
                <th style="font-size: 0.8em;">Quality Map</th>
                <th style="font-size: 0.8em;">RGB</th>
                <th style="font-size: 0.8em;">Prompt</th>
                <th style="font-size: 0.8em;">Mask</th>
                <th style="font-size: 0.8em;">Grasp</th>
                <th style="font-size: 0.8em;">Quality Map</th>
            </tr>
        </tbody>
    </table>
</center>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/5/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/7/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/15/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/38/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/seen/42/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<!-- <br> -->

<!-- - **Grasp-Anything(Unseen)** -->
<h3 class="title is-3">Grasp-Anything(Unseen)</h3>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/7/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/8/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/10/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/14/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/17/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspanything/unseen/1002/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<br>
<br>
<br>
<br>

# In the Wild Image Inference

<!-- - **Armbench** -->
<h3 class="title is-3">Armbench</h3>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/armbench/1/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/armbench/11/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/armbench/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/armbench/34/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/armbench/86/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/armbench/99/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<!-- <br> -->

<!-- - **GraspNet** -->
<h3 class="title is-3">GraspNet</h3>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspnet/5/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspnet/21/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspnet/89/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspnet/92/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/graspnet/98/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/graspnet/45/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<!-- <br> -->


<!-- - **OCID** -->
<h3 class="title is-3">OCID</h3>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/ocid/2/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/ocid/9/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/ocid/28/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/ocid/34/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/ocid/38/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/ocid/53/predict_vis_1h.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<br>
<br>
<br>
<br>

# Real Image Inference

<!-- - **1Point** -->
<h3 class="title is-3">Prompt: 1Point</h3>

<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_0.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_72.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_75.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_78.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_88.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/1point/real_img_95.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<!-- <br> -->




<!-- - **3Points** -->
<h3 class="title is-3">Prompt: 3Points</h3>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_16.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_20.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_28.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_32.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_44.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/3points/real_img_58.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<!-- <br> -->




<!-- - **5Points** -->
<h3 class="title is-3">Prompt: 5Points</h3>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_5.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_10.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_48.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_51.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_65.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/5points/real_img_70.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<!-- <br> -->




<!-- - **10Points** -->
<h3 class="title is-3">Prompt: 10Points</h3>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_12.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_30.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_60.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_68.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_92.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/10points/real_img_98.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>



<br>
<br>
<br>
<br>

# Real Image Inference with Grounding Dino

<h3 class="title is-3">Prompt: User Language</h3>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
            <td style="border: none;">
                <img src="./assets/images/real_images/dino/language/prompt_10.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
            </td>
            <td style="border: none;">
                <img src="./assets/images/real_images/dino/language/prompt_grasp_10.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_16.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_16.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_28.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_28.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_42.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_42.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_74.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_74.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_77.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_77.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>

<!-- <center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_10.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_10.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_16.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_16.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_28.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_28.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_42.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_42.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_74.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_74.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_77.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/language/prompt_grasp_77.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center> -->


<h3 class="title is-3">Prompt: Rigid </h3>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_0.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_0.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_9.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_9.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_28.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_28.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_47.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_47.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_80.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_80.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
<table style="border: none; display: initial;">
    <tbody>
        <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_97.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_97.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<!-- <center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_0.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_0.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_9.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_9.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_28.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_28.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_47.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_47.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center>
<center>
    <table style="border: none; display: initial;">
        <tbody>
            <tr style="border: none;">
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_80.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_80.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_97.jpg" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
                <td style="border: none;">
                    <img src="./assets/images/real_images/dino/grid/rigid_grasp_97.png" alt="Additional Result 1" style="margin: 10px 20px 10px 0px;" width="100%"/>
                </td>
            </tr>
        </tbody>
    </table>
</center> -->


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

# Acknowledgements

  This work was supported by Institute of Information & communications Technology Planning & Evaluation (IITP) grant funded by the Korea government(MSIT) No.RS2021-II212068, Artificial Intelligence Innovation Hub.

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
