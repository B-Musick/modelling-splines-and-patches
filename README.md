# General
- For the Computer Graphics we had a couple assignments involving the use of splines and 
patches.
- The programs I wrote were in C++ and openGL

# Splines
- For the first assignment we were tasked with implementing:
    - Bezier Spline
    - Catmull-ROM Spline
    - B-Spline
- The same 12 control points were used to easily distinguish the different curves. Each 
control point could be selected (orange) and moved to a different location to see how the 
curve is shaped by the control points.

## Bezier Spline
- Left Image:
    - It can be seen that the bezier spline is calculated with respect to 4 control points, there are 4 separate splines being calculated in this image (can see the start and 
    end where the lines intersect with the control points).
    - You can see in the output below, the left is the original bezier spline where one control point is orange (which is the control point that will be moved). 
- Right Image:
    - The control point was moved and it can be seen that the spline changes with respect to 
    4 control points.

<img src="./images/hermite_init.png" style="height:250px;">  <img src="./images/hermite_change.png" style="height:250px;padding-left:30px">


## Catmull Splines
- It can easily be seen that Catmull splines are fully interpreted (meaning the curve passes through all control points).
- The main individuating factor of this spline calculation is that a tangent line from control points 2,4 and one between 1,3 is used in the matrix calculation. And 4 control points are needed to calculate the curve between control points 1,2. This 12 calculations were needed to interperet my curve, as compared to the 4 calculations for the Bezier curve.

<img src="./images/catmull_init.png" style="height:300px;">  <img src="./images/catmull_change.png" style="height:300px;padding-left:30px">

## B-Spline
- B-splines are interpreted much in the same way catmull-rom curves are, where 4 control points only determine the curve between the first 2 control points in the group, thus 12 calculations need to occur to get the whole curve.
- The main specialty of B-Splines is that it uses weights, so if a control point is interpreted multiple times, this control point has more weight on the curve and will thus cause more change in the shape of the curve.

<img src="./images/bspline_init.png" style="height:300px;">  <img src="./images/bspline_change.png" style="height:300px;padding-left:30px">


# Bicubic Patch
- For the subsequent assignment, we were tasked with implementing a Bicubic Patch to 
output the infamous Newell Teapot, as well as an object of our own creation.
- In this program the control points can be toggled on and off by pressing 'z', as can be 
seen comparing the right and left images (right shows the control points from which the 
curve is shaped).
- Rotated in the x, y and z axes using mouse
- This assignment gave me a keen intuition into how complex shapes are modelled in 
animated movies such as those from Pixar.

## Teapot Output
- The teapot is implemented using 32 patches of 16 control points
- Teapot data obtained from John Braico, original source it was adapted was from:
    - Newell's Utah teapot (with bottom): https://github.com/rm-hull/newell-teapot

<img src="./images/teapot.png" style="height:300px;">  <img src="./images/teapot_ctrl_pts.png" style="height:300px;padding-left:30px">

## Vase Output
- The vase I implemented uses 6 patches of 16 control points

<img src="./images/vase.png" style="height:300px;">  <img src="./images/vase_ctrl_pts.png" style="height:300px;padding-left:30px">

# Sources
John Braico - Computer Graphics Professor