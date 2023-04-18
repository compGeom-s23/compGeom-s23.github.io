---
layout: default 
title: ----Project 6 (path planning via vis graph)
nav_order: 12
---



## Project 6:  Path Planning via Visibility Graph


*** 
* __Assigned:__ Tuesday, April 18
* __Due:__  Sunday April 30th 
* Group policy: Partner-optional 
* Collaboration policy: Level 1
 


In this project you will implement geometric motion planning for a point robot
moving among polygonal obstacles in 2d  using the visibility
graph (VG) approach.

![](vg1.png) ![](vg1.png) ![](vg3.png)


### Overview

One of the fundamental problems in robotics is motion planning: given
a robot R and an environment (or physical space), a start position
and an end position, find a path so that the robot can
move from start to end, without collisisons. Generally speaking, in
most situations we are happy to compute just a path, not necessarily
the optimal/shortest, but in some special situations we are able to compute
an optimal shortest path.

In this first project we will consider a simple instance of the path
planning problem and make some simplifying assumptions which will
allow us to do optimal routing:


 - 2D: We'll assume that the environment consists of a set of 2D
   polygons that represent the obstacles. Furthermore, we assume that
   the robot is moving in a large bounding box B that contains all
   polygons.

- Static: We'll assume that the environment is static (the obstacles are fixed).

- Known: The environment is known, i.e. the robot knows the list of
  obstacles with their vertices and edges. That is, the robot does not
  rely on sensors to learn the environment, instead the environment is
  given.

- Point robot: the robit is assume to be a point (yes, that's not very
  realistic, but it's a good place to start).


The general idea of motion planning is to start by computing a
decomposition of the free space (the space where the robot can move)
into cells, and construct a road map of the free space to guide the
motion between neighboring cells. The road map is essentially a graph
of free space. Ideally we want to build the roadmap so that:

    1. Any path in the road map corresponds to a collision-free path in
    the free space.
    2. Any path in the free-space corresponds to a path in the road map.

If we are able to compute a road map of free space with these
properties, then to move from a location s to a location t, we will find a path in the road map
from s to t. We know that any path in the road map is colision-free
(by (1)), and we know that if a path in the road map does not exist,
then no path exists (by (2)). Essentially we have reduced the motion
planning problem to a path problem in a graph.


For a point robot moving among polygonal obstacles in the plane, it is
possible to construct a type of roadmap that will allow to compute
optimal paths: the visibility graph.  This is a graph whose vertices are
the vertices of the obstacles, and its edges (u,v) are all the pair of
vertices that can "see" each other, that is, segment uv does not
intersect the interior of any obstacle. Some screenshots above. 


Shortest paths in 2D have the very nice and convenient property that
they are straight lines, and they have to go through the vertices of
the obstacles. This basically means that any shortest path will be
contained in the VG. Once the visibility graph (VG) is computed, the
shortest paths from start to end can be computed for e.g. using
Dijkstra's algorithm.


### This project


1. When you start your code, have a pre-set scene with polygonal
obstacles.  Allow the user to reset the scene and and enter polygons
using the mouse (in a manner similar to previous projects).  
scene.

2. Once the scene is done, compute and render the visibility graph.


3. Allow the user to click on the start and end position of the
"robot" in the scene. Then, run Dijkstra's algorithm on the VG and
render the resulting path (for e.g. in a different color and different
line width). Let the user enter different start and end positions and re-compute the path. 


All the geometric primitives that you'll need for this project, you've
already written them.  So that part should feel easier. The other part
is implementing Dijsktra's algorithm. In csci2200 we discussed the
pseudocode for Dijkstra. In this project you have an opportunity to
figure out the details.


### Dijkstra's algorithm 

In theory we always assume that the graph is given nicely in an
adjacency list form.  Here you have a bunch of edges, and
you will need to  create an adjacency list for the VG graph.


Once you have an adjacency list, you can pretty much forllo with the
algorithm from the textbook.


## Extra features


* Implement a point-in-polygon method and use it to detect if start or
  end points are inside an obstacle.
* Detect if a polygon is self-intersecting.
* Detect if polygons are overlapping.
* Draw the polygons filled. Note that openGL can only fill correctly
  convex polygons, so if you want it filled, you'll need to compute a
  triangulation.


### What and how to  turn in


You will receive the assignment on GitHub. To submit, simple push your
code into your github repository for this assignment. Do not turn in
any object or executable files.

Add a README file containing: a brief, description of the project;
info on the interface, i.e. everything one needs to know in order to
run your code; a list of known bugs (if any) and when they happen; a
list of the main functions you implemented (); any extra features you
implemented.

Also: Capture a movie of the screen while you demo your code and
upload it to github, either in #general or a a direct message. To
demo, no voice, just run your code and show what it can do (To capture
a movie on a Mac press shift+command+5 and then choose the option that
says record selected portion).

### Start early, program well and enjoy the proces!

By now you know how frustrating debugging can be.  It is crucial that you
develop your code one piece at a time, and test before you move on to
the next. From the beginning, design your code knowing that you will
spend 90% of the time debugging it. 


