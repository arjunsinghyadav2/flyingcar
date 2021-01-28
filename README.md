# FCND - 3D Motion Planning
![Getting Started](./misc/enroute.png)



This project is a continuation of the Backyard Flyer project where you executed a simple square shaped flight path. In this project you will integrate the techniques that you have learned throughout the last several lessons to plan a path through an urban environment. Check out the [project rubric](https://review.udacity.com/#!/rubrics/1534/view) for more detail on what constitutes a passing submission.

1. Writeup / README that includes all the rubric points and how I addressed each one.

the Starter Code
  motion_planning.py 
  The code contains a motion planner class that contains helper function that help in arming the drone, takeoff and transitioning to waypoints, the core of the code is a A* algorithm that helps in planning path from point A to point B selected by user. Here also the local, home and global position of the drone are also constantly received in the code. 
  
  planning_utils.py:
  the code contains tools which creating a grid using the collider.csv data as well as Action that our drone can possibly take along with cost of each action, these action are using in A* algorithm . Lastly the code contains a heuristic method that allows us to calculate distance between two points and adding the distance to our cost for path planning.


And here's a lovely image of my results 
![alt text](https://github.com/arjunsinghyadav2/flyingcar/blob/master/image.jpg?raw=true)

![alt text](https://github.com/arjunsinghyadav2/flyingcar/blob/master/image1.jpg?raw=true)


1. Set your global home position
Line 129 (motion_planning.py)

2. Set your current local position
line 132 (motion_planning.py)

3. Set grid start position from local position
Line 148 (motion_planning.py)

4. Set grid goal position from geodetic coords
This step is to add flexibility to the desired goal location. Should be able to choose any (lat, lon) within the map and have it rendered to a goal location on the grid.
Line 150 (motion_planning.py)

5. Modify A* to include diagonal motion (or replace A* altogether)
Minimal requirement here is to modify the code in planning_utils() to update the A* implementation to include diagonal motions on the grid that have a cost of sqrt(2), but more creative solutions are welcome. Explain the code you used to accomplish this step. 
class Action(Enum): Line 58-61 (planning_utils.py)


6. Cull waypoints
For this step you can use a collinearity test or ray tracing method like Bresenham. The idea is simply to prune your path of unnecessary waypoints. Explain the code you used to accomplish this step.
Line 161 (motion_planning.py)

Execute the flight
1. Does it work?
It works!