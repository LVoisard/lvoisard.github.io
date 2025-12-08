---
layout: page
title: ECS Survivors
description: A survivors like game written in C++ with Raylib and Flecs
img: assets/img/ecs-thumbnail.png
importance: 0
category: games
related_publications: false
---

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ecs-thumbnail.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Over a year now, I have been trying to learn ecs by building concrete projects. ECS Survivors is the culmination of what I have learned so far.

ECS Survivors is made using Raylib for rendering and I am using the flecs framework as an ECS.

In fact ECS Survivors is one of the featured projects on the flecs [home page](https://www.flecs.dev/flecs/#ecs-survivors)!

You can find the source code on [github](https://github.com/ptidejteam/ecs-survivors), and you can also play the online demo on [itch.io](https://laurent-voisard.itch.io/ecs-survivors)

Features:
 - Player Movement
 - Custom Physics
 - Tilemap loading (using [Tiled](https://www.mapeditor.org/) and [tmxlite](https://github.com/fallahn/tmxlite))
 - Ranged Combat
 - Level progression
 - Custom GUI elements

TODO:
 - Refactoring into modules
 - Game Editor (for debugging)
 - Melee combat
 - SFX

Future features:
 - Procedural Level Generation
 - Client/Server multiplayer

