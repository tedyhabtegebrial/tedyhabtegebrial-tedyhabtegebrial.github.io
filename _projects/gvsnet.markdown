---
layout: page
title: "Generative View Synthesis: from Single-view Semantics to Multi-view Images"
description:
img: /assets/img/GVSNet.png
importance: 1
---
<table align=center width=800px>
  <tr>
    <td align=center width=300px>
    <center>
      <span style="font-size:20px">Tewodros A. Habtegebrial</span>
      </center>
      </td>
    <td align=center width=200px>
    <center>
      <span style="font-size:20px"><a href="http://varunjampani.github.io/">Varun Jampani</a></span>
      </center>
      </td>
    <td align=center width=150px>
    <center>
      <span style="font-size:20px">Orazio Gallo</span>
      </center>
      </td>
      <td align=center width=150px>
      <center>
      <span style="font-size:20px">Didier Stricker</span>
      </center>
      </td>
      </tr>
</table>

<!-- GVS is a new problem where novel-views of a scene are rendered from a 2D semantic input. -->

<style>
table, th, td {
  padding: 5px;
}
table {
  border-spacing: 15px;
  text-align: center;
  vertical-align: middle;
}
</style>

<table style=" margin-left:auto;margin-right:auto;class:center">
 <tr>
   <th>Input Semantics</th>
   <th>GVSNet: Ours</th>
   <th>SPADE+SM</th>
   <th>SPADE+CVS</th>
   <th>SPADE+AF</th>
 </tr>
 <tr>
   <td>
     <video autoplay="autoplay" loop="loop" width="150" height="150">
       <source src="/assets/video/carla/circle_r_0_25/0_Ours.mp4" type="video/mp4">
     </video>
   </td>
   <td>
     <video autoplay="autoplay" loop="loop" width="150" height="150">
       <source src="/assets/video/carla/circle_r_0_25/0_Ours.mp4" type="video/mp4">
     </video>
   </td>
   <td>
     <video autoplay="autoplay" loop="loop" width="150" height="150">
         <source src="/assets/video/carla/circle_r_0_25/0_SPADE+SM.mp4" type="video/mp4">
           <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
     </video>
   </td>
   <td>
     <video autoplay="autoplay" loop="loop" width="150" height="150">
         <source src="/assets/video/carla/circle_r_0_25/0_SPADE+CVS.mp4" type="video/mp4">
           <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
     </video>
   </td>
   <td>
     <video autoplay="autoplay" loop="loop" width="150" height="150">
         <source src="/assets/video/carla/circle_r_0_25/0_SPADE+AF.mp4" type="video/mp4">
           <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
     </video>
   </td>
 </tr>

</table>

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

<!-- <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/1.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/5.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/5.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal it's glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/" target="_blank">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
``` -->
