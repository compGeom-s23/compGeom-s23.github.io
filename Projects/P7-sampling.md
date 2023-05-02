---
layout: default 
title: ----Project 7 (3dof)
nav_order: 13
---



## Project 7:  Approximate motion planning with translation and rotation 


*** 
* __Assigned:__ Tuesday, May 2nd
* __Due:__  part 1 (Tuesday May 9th), final Friday May 19th
* Group policy: Partner-optional 
* Collaboration policy: Level 1
* Overall policy:  This project serves as a final exam, and as such you are expected to complete it without help from the instructor or the TAs.  Looking for resources on the www, including papers and code, is allowed. In terms of weight, all projects are weighed equally, and each project (this one included) amounts to 13% of the final grade. 



In this project you will implement approximate motion planning for a polygonal robot moving among polygonal obstacles in 2d  with translation and rotation (3dof) using one of the following algorithms:  A*, RRT or PRM .


### Interface 

When the program starts the user will enter the polygons using the mouse (in a manner similar to previous projects), then  once the scene is done, the user will enter the robot. Then the user will click on the start and end position of the robot.  

Whichever  planner you chose to implement, use it to find a path from start to end.  Then draw the path and  animate the robot traveling along the path. 



### What and how to  turn in


You will receive the assignment on GitHub; it contains no code.  To submit, simple push your
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
From the beginning, design your code knowing that you will
spend 90% of the time debugging it. If you approach your algorithm with a theoretical mindset, and think before you start coding, you will be a lot more effective. 
