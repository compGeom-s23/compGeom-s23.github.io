---
layout: default 
title: Syllabus
nav_order: 1
---


## Computational Geometry, Spring 2023


## Syllabus


__Instructor:__ Laura Toma, email: ltoma at bowdoin.edu, office: Searles 219 

__Class time:__  TR 1:15-2:40

__Classroom:__  VAC North 304

**Prerequisites:** csci 2200 (Algorithms) and csci 2330 (Systems). In other words, knowledge of:

- basic analysis: asymptotic notation, growth, recurrences.
- basic algorithm design techniques: divide-and-conquer, greedy.
- basic algorithms and data structures: searching, sorting, binary search trees, priority queues.
- basic programming in C/C++
- basic Unix terminal commands and Makefiles


Computational geometry studies algorithms for problems that involve geometric data: (finite) sets of points, line segments and polygons. It is a young and growing field, driven by applications in graphics, robotics, autonomous vehicles, vision, image processing, and GIS. Some classical examples of geometric problems: Is a point inside or outside a given polygon? Do two polygons intersect? Given a set of points in the plane, what is the closest pair of points? What is the smallest convex polygon that contains a set of points in the plane? What are all the points that fall in a given query range? What is visible from a point in a polygon? How many points are sufficient to guard any polygon? Given two sets of segments, what are their intersections? Given a set of points, what is their smallest enclosing circle? Given a set of polygonal obstacles, and a polygonal robot moving in 2D with translation and rotation, what is an efficient path between a start and end location? And many more. This class is an introduction to computational geometry and will cover some fundamental problems and techniques in the field.

**Learning goals:** 

- Understand advanced algorithms and techniques used in computational geometry
- Understand algorithms at various levels of abstraction,  from abstract conceptual ideas to code
- Understand the importance in practice of handling degenerate cases
- Be able to come up with detailed code implementing a conceptual idea
- Experience the interplay between theory and practice 

## Syllabus overview:

The class will draw from fundamental topics: 

- Introduction (collinear points, closest pair of points)
- Geometric primitives (area of triangle, orientation, segment intersection)
- Convex hulls in 2D  (naive, gift wrapping, quickhull, Graham scan, incremental, divide-and-conquer; lower bound)
- Convex hulls in 3D
- Segment intersection (Bentley-Ottman sweep)
- Art gallery problem. Fisk's sufficiency proof.
- Polygon triangulation (quadratic, based on ear removal algorithm;  triangulation of monotone polygons; polygon triangulation in O(n lg n) via trapezoidalization).
- Geometric searching (orthogonal range searching with kd-trees and range trees).
- Voronoi diagrams and Delaunay triangulations.
- Combinatorial motion planning in 2D (C-space and C-obstacles; planning via graph search; visibility graph)
- Heuristical motion planning (grid-based techniques, sampling, PRM, RRT)


 
**Textbooks:** There is no required textbook. The course is based on two classical textbooks, below. You can find them in Searles 224 (you're more than welcome to read them, but please do not take them out of 224).

- [Computational geometry in C](https://www.amazon.com/Computational-Geometry-Cambridge-Theoretical-Computer/dp/0521649765/ref=sr_1_3?ie=UTF8&qid=1389985599&sr=8-3&keywords=computational+geometry). J. O'Rourke.
- [Computational geometry: algorithms and applications](https://www.amazon.com/Computational-Geometry-Applications-Mark-Berg/dp/3540779736/ref=pd_bxgy_b_img_z). Mark de Berg, Otfried Cheong, Mark van Kreveld, Mark Overmars.



     
  
**Work and Grading Policy:** 

The work for the class consists of programming projects (7 projects, approximately biweekly) and in-class work. 

- __Projects: 90%__ 

- __Class engagement: 10%__ This means attending class, working with your group, asking questions, engaging in discussions, volunteering answers,  participating on Slack, attending office hours and striving to turn in good work. 



**Collaboration policy:** 

You can work alone, or you can pair with a partner (pair-programming).

__Collaboration across teams is at level-1:__ that is, verbal collaboration without solution sharing. You are allowed and encouraged to discuss ideas with other class members, but the communication should be verbal and additionally it can include diagrams on board. Noone is allowed to take notes during the discussion (being able to recreate the solution later frommemory is proof that you actually understood it). Communication cannot include sharing pseudocode for the problem. Please read the department's collaboration policy.

__Pair programming policy:__ If you chose to work with a partner, you must work together, physically in the same place, for the entire project that you do together. The overall project must be a true joint effort, equally owned, created and understood by both partners. Specifically splitting the problem into parts and working on them separately is not allowed and violates the honor code for the class. If you start together as a team and are unable to complete the project together, then you will each inherit teh shared code, and split up to work individually on the remainder of the project. You would then submit individually, with a note on what happened.
There are many advantages to working with a partner (e.g. more fun, more learning, good skill for the "real world"), and I encourage you to try. You may also consider alternating between working alone and with a partner, and changing partners.

Remember that you are responsible for reading, understanding, and adhering to the policy. If you have any questions about any aspects of the policy, please do not hesitate to ask for clarification.


**Time Commitment:**
This is a 3000-level CS class and will demand a significant time commitment. It is critical that you budget your time accordingly.  

