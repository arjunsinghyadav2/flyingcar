# FCND - 3D Motion Planning
![Getting Started](./misc/enroute.png)



This project is a continuation of the Backyard Flyer project where you executed a simple square shaped flight path. In this project you will integrate the techniques that you have learned throughout the last several lessons to plan a path through an urban environment. Check out the [project rubric](https://review.udacity.com/#!/rubrics/1534/view) for more detail on what constitutes a passing submission.

1. Writeup / README that includes all the rubric points and how I addressed each one.

the Starter Code
1. motion_planning.py 
  The code contains a motion planner class that contains helper function that help in arming the drone, takeoff and transitioning to waypoints, the core of the code is a A* algorithem that helps in planning path from point A to point B selected by user. Here also the local, home and global position of the drone are also constantly received in the code. 
  
  planning_utils.py:
  the code contains tools which creating a grid using the collider.csv data as well as Action that our drone can possibly take along with cost of each action, these action are using in A* algo. Lastly the code contains a heurestic menthod that alows us to calculate distance between two points and adding the distance to our cost for path planning.


And here's a lovely image of my results 
![alt text](https://github.com/arjunsinghyadav2/flyingcar/blob/main/image.png?raw=true)

![alt text](https://github.com/arjunsinghyadav2/flyingcar/blob/main/image1.png?raw=true)

Here's	A	Snappy	Table
1	highlight	bold	7.41
2	a	b	c
3	italic	text	403
4	2	3	abcd
Implementing Your Path Planning Algorithm
1. Set your global home position
Here students should read the first line of the csv file, extract lat0 and lon0 as floating point values and use the self.set_home_position() method to set global home. Explain briefly how you accomplished this in your code.

And here is a lovely picture of our downtown San Francisco environment from above! Map of SF

2. Set your current local position
Here as long as you successfully determine your local position relative to global home you'll be all set. Explain briefly how you accomplished this in your code.

Meanwhile, here's a picture of me flying through the trees! Forest Flying

3. Set grid start position from local position
This is another step in adding flexibility to the start location. As long as it works you're good to go!

4. Set grid goal position from geodetic coords
This step is to add flexibility to the desired goal location. Should be able to choose any (lat, lon) within the map and have it rendered to a goal location on the grid.

5. Modify A* to include diagonal motion (or replace A* altogether)
Minimal requirement here is to modify the code in planning_utils() to update the A* implementation to include diagonal motions on the grid that have a cost of sqrt(2), but more creative solutions are welcome. Explain the code you used to accomplish this step.

6. Cull waypoints
For this step you can use a collinearity test or ray tracing method like Bresenham. The idea is simply to prune your path of unnecessary waypoints. Explain the code you used to accomplish this step.

Execute the flight
1. Does it work?
It works!