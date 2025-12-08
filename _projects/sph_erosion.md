---
layout: page
title: SPH Erosion
description: A hydraulic erosion simulation using SPH for water (2022)
img: assets/img/sph/thumbnail.png
importance: 0
category: simulations
related_publications: true
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sph/thumbnail.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

As one of the deliverables for this my computer animations (COMP 477) final project, we had to make a html report of the projet, I will let it speak for Itself.

I implemented GPU instancing for the spheres, a spatial-hash grid for the neighbouring search, the SPH algorithm and integrating it with the sediment transport, and the random terrain generation.

### PROJECT GOAL
For our final project, we aimed to deliver an OpenGL application that could simulate fluid dynamics and its erosion effects on terrain in real-time.
The project was too ambitious and we were not able to implement all parts we wanted, but we believe that the results are still respectable.

---
			
### EVOLUTION OF RESULTS

As it happens gradually, erosion and sediment deposition can be difficult to notice. The videos below here are sped up as to better showcase them.
Such changes to the terrain can be made more obvious by quickly scrubbing through the video using the timeline bar. We also recommend viewing the videos in fullscreen to that effect.

The amount of sediment contained within each SPH particle is indicated by its color turning from blue to orange. Some particles are randomly chosen to start with some sediment

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/02_1.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/02_2.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>

Erosion along the slope leading to noticeable sediment deposition at the bottom.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/03_1.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/03_2.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
Pooling results in fluid gradually depositing eroded sediment.
				
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/04.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
Longer slope leads to more sediment accumulation in the fluid, resulting in larger deposition.

#### Surface Normal Calculations

During development, we noticed that there were inaccuracies in the behavior of the SPH fluid, especially so near the borders of the terrain. 
This turned out to be the caused by the way we computed surface normals from the terrain. 
The videos below showcase the fluid behavior prior to demonstrate improvements made in this regard.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/01_2.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
The fluid flows less naturally, and seems to "stick" to the cliffside. Erosion occurs as it should regardless.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video class="img-fluid rounded z-depth-1" controls autoplay muted loop>
            <source src="{{ '/assets/img/sph/00.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
An extreme example where the fluid in the border cells would climb uphill.

---


### REFLECTION
As stated above, the project was too ambitious for a team of 2. 
We did not have time to implement proper fluid sources or paint brushes to edit terrain in real-time. 


Despite this, the SPH simulation paired with the erosion model can still demonstrate 
nice and, altough exaggerated for demonstration purposes, believeable-looking erosion. 
The project exists as a nice proof of concept that could be expanded later if desired.

### DEPENDENCIES
This project was created using OpenGL3 with ImGUI and stb image libraries.
