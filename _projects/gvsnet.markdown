---
layout: page
title: "Generative View Synthesis: from Single-view Semantics to Multi-view Images"
description:
img: /assets/img/GVSNet.png
importance: 1
---
<div class="container">
  <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4">
    <div class="col"><center>
      <span style="font-size:20px"><a href="http://tedyhabtegebrial.github.io/">Tewodros A. Habtegebrial</a></span>
      </center></div>
    <div class="col"><center>
      <span style="font-size:20px"><a href="http://varunjampani.github.io/">Varun Jampani</a></span>
      </center></div>
    <div class="col"><center>
      <span style="font-size:20px"><a href="http://alumni.soe.ucsc.edu/~orazio/">Orazio Gallo</a></span>
      </center></div>
    <div class="col"><center>
      <span style="font-size:20px"><a href="https://av.dfki.de/members/stricker/">Didier Stricker</a></span>
      </center></div>
  </div>
</div>

<!-- <table align=center width=800px>
  <tr>
    <td align=center width=300px>
    <center>
      <span style="font-size:20px"><a href="http://tedyhabtegebrial.github.io/">Tewodros A. Habtegebrial</a></span>
      </center>
      </td>
    <td align=center width=200px>
    <center>
      <span style="font-size:20px"><a href="http://varunjampani.github.io/">Varun Jampani</a></span>
      </center>
      </td>
    <td align=center width=150px>
    <center>
      <span style="font-size:20px"><a href="http://alumni.soe.ucsc.edu/~orazio/">Orazio Gallo</a></span>
      </center>
      </td>
      <td align=center width=150px>
      <center>
      <span style="font-size:20px"><a href="https://av.dfki.de/members/stricker/">Didier Stricker</a></span>
      </center>
      </td>
      </tr>
</table> -->

<br>
<br>

<div class="container">
<div class="row">
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
     <div class="caption"> Input Semantics </div>
     <video autoplay="autoplay" loop="loop" width=150>
         <source src="/assets/video/carla/circle_r_0_25/0_input_sem.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <div class="caption"> GVSNet (Ours) </div>
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/0_Ours.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <div class="caption"> SPADE[1]+SM[2] </div>
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/0_SPADE+SM.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <div class="caption"> SPADE[1]+CVS[3] </div>
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/0_SPADE+CVS.mp4" type="video/mp4">
     </video>
    </div>
</div>
<div class="row">
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
     <video autoplay="autoplay" loop="loop" width=150>
         <source src="/assets/video/carla/circle_r_0_25/4522_input_sem.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/4522_Ours.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/4522_SPADE+SM.mp4" type="video/mp4">
     </video>
    </div>
    <div class="col-sm mt-4 mt-md-0 col-md-offset-2">
      <video autoplay="autoplay" loop="loop" width=150>
       <source src="/assets/video/carla/circle_r_0_25/4522_SPADE+CVS.mp4" type="video/mp4">
     </video>
    </div>
</div>
</div>

<br>

### Abstract
<div align="justify">
Content creation, central to applications such as virtual reality, can be a tedious and time-consuming.
Recent image synthesis methods simplify this task by offering tools to generate new views from as little
as a single input image, or by converting a semantic map into a photorealistic image. We propose to push
the envelope further, and introduce Generative View Synthesis (GVS), which can synthesize multiple photorealistic views
of a scene given a single semantic map. We show that the sequential application of existing techniques, e.g., semantics-to-image
translation followed by monocular view synthesis, fail at capturing the scene's structure. In contrast, we solve the semantics-to-image
translation in concert with the estimation of the 3D layout of the scene, thus producing geometrically consistent novel views that preserve
semantic structures. We first lift the input 2D semantic map onto a 3D layered representation of the scene in feature space, thereby preserving
the semantic labels of 3D geometric structures. We then project the layered features onto the target views to generate the final novel-view images.
We verify the strengths of our method and compare it with several advanced baselines on three different datasets. Our approach also allows for style
manipulation and image editing operations, such as the addition or removal of objects, with simple manipulations of the input style images and semantic maps respectively.

</div>
<br>



<br>
<br>
## Paper Link
Arxiv: <a href="https://arxiv.org/abs/2008.09106">link</a><br>
PDF:  <a href="https://arxiv.org/pdf/2008.09106.pdf">link</a><br>
<br>
<br>
## Code, supplemental video and more results
Coming soon
<br>
<br>
## References
[1] SPADE: <em>Semantic Image Synthesis with Spatially-Adaptive Normalization</em>, Park et al. <a href="https://arxiv.org/abs/1903.07291">link</a><br>
[2] SM: <em> Stereo Magnification: Learning View Synthesis using Multiplane Images</em>, Zhou et al. <a href="https://people.eecs.berkeley.edu/~tinghuiz/projects/mpi/"> link </a><br>
[3] CVS: <em> Monocular Neural Image Based Rendering with Continuous View Control</em>, Chen et al.   <a href="https://arxiv.org/abs/1901.01880">link</a><br>
