---
layout: page
title: Hydraulic Erosion
description: A hydraulic erosion simulation using grid based physics (2022)
img: assets/img/erosion/image007.png
importance: 1
category: simulations
related_publications: true
---


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/erosion/image007.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

I have always been in awe at what mother nature can craft over millennia. Simple rain drops over millions of years shape rivers, valleys, and more. That's why for my geometric modelling class, I decide to capture the process of hydraulic erosion.

The simulations run in real time for smaller terrain meshes and are fully interactable to allow users to understand the process of hydraulic erosion.

This project was implemented in C++, OpenGL and GLFW.

### Gallery

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/erosion/coast_waves.webm' | relative_url }}" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
<caption> 
    Rain falls from the hills while waves crash onto the coast.
</caption>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/erosion/paint_brush.webm' | relative_url }}" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
<caption> 
    Water paint brush in action.
</caption>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/erosion/visibility_modes.webm' | relative_url }}" type="video/webm">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
<caption> 
    Showcase of the debug modes for the terrain and water. Water: Normal | Velocity | Sediment Qty, Terrain: Erosion Susceptibility | Sediment Added/Remove
</caption>