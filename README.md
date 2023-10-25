# SpacedOut
Spaced Out! Design in Every Dimension

------
## Part One: Thinking in 3D

<a href="https://shorturl.at/GNRZ1" target="_blank">This simple scene</a> (click the `Fork` button) contains five _entities,_ each with an appended _geometry_ —we'll be using it as a place to start

-----

Placing and orienting objects in space, it's convenient to think in terms of a _coordinate system_  
In _two dimensions,_ operating on a plane (a flat area, like a piece of paper) we can visualize space as starting in the middle, at zero width, zero height and expanding outward from there into positive and negative numbers
<img src="https://www.mathsisfun.com/numbers/images/number-line.svg" alt="positive numbers appear to the right, negative numbers to the left of zero" style="width:300px">
which are the numbers to the left of zero on a number line   
If we arrange a pair of number lines at right angles (crossing each other like a `plus` sign) we create two axes (pronounced _axe-ease_) x and y  

Using these number lines we can identify any point on the plain by two coordinate numbers: `x, y`  
<img src="https://media.istockphoto.com/vectors/blank-cartesian-coordinate-system-in-two-dimensions-rectangular-vector-id1414318929?k=20&m=1414318929&s=612x612&w=0&h=jCfZ9Kb2CwYpfs5jXFEzAs-3_ncCSYtdl1sUIUTL8hU=" alt="a 2D system with width on the x-axis and height on the y-axis" style="width:300px">

###### This is a 2D system with width on the x-axis and height on the y-axis  

------

> ### **CHALLENGE: Orienting 2D**  
Find the point (-3x, 4y) 

------

We can do something similar in three dimensions (like the space inside a box) with a third axis, `z`  
We can identify any point in space with three coordinate numbers: `x, y, z`  
We sometimes call x, y and z "width, height and depth" 

<img src="https://upload.wikimedia.org/wikipedia/commons/3/3b/3D_Cartesian_coordinates.PNG" alt="a 3D system with width on the x-axis, height on the y-axis and depth on the z axis" style="width:300px">

###### This is a 3D system with width on the x-axis, height on the y-axis and depth on the z-axis
 
------

> ### **CHALLENGE: Orienting 3D**  
Find the point (-3x, 2y, -4z)  
(You may have to count the points on the line as these are not given)

------

> **The cartesian coordinate system was invented by <a href="https://en.wikipedia.org/wiki/Ren%C3%A9_Descartes" target="_blank">René Descartes</a> who famously wrote: <a href="https://en.wikipedia.org/wiki/Cogito,_ergo_sum#:~:text=Cogito%2C%20ergo%20sum%20is%20a,than%20Latin%20would%20have%20allowed" target="_blank">"I think, therefore I am"**</a>

### **NOTE:**   
From the default Point of View (POV) in A-Frame, negative numbers lie:
>* To the Left 
> * Downward and 
> * Forward 

### **BE AWARE THAT:**
* x-axis numbers will always be given first 
* y-axis second 
* z-axis third  
**And in A-Frame** the number units are considered to be _meters_

------

------

## **Camera**
<a href="https://aframe.io/docs/1.3.0/components/camera.html#sidebar" target="_blank">(The A-Frame Camera Documentation)</a>

The position of the POV) "camera" is, at launch: `0, 1.6, 0`  
That is, at a supposed "average eye level" —it's as if you were _standing on the `0, 0, 0` center point_  
Or consider that the `0, 0, 0` point will be -1.6 meters _below your POV_

In A-Frame, 3D coordinate systems apply separately to the Space (the world in general) and to each Entity (every object located in the world)   

### **JUST REMEMBER:** 
1. Anything can have its own c  oordinate system with `0, 0, 0` representing the center of that system
2. For an Entity with appended geometry, the center is considered the _middle of the geometry_ 

This means we have to think in terms which may not be familiar, as we're used to referencing the _surfaces of objects_ and not their _centers_

------
------

## Sign in to CodeSandbox

* **You'll need an Email Address**
* You can sign in with Github or Gmail  
If you don't have a gmail account, <a href="https://www.gmail.com" target="_blank">it's free!</a>

* **You Might Not Want Your Real Name** as your email address -tho this will not be visible to other Glitch users
* **Do Not Forget** your email, sign-in and password! 
* **Create a CodeSandbox user**  
Name it anything, but **you might not want to use your real name** as these user names _will be visible to other CodeSandbox users_   

Find the `Fork` button and 
<a href="https://shorturl.at/GNRZ1" target="_blank">"fork" this scene</a> —make it your own!   
 
------
------

## Navigating in Space

* **Click and drag your mouse** to "look around"
* **Use W, A, S, D keys** (or the left, right, up and down arrow keys) to move around the plane

------
------

## Positioning Geometries in Space

Compare the code in the index.html on the left hand side to the scene preview on the right hand side

### THE SCENE from the bottom, up

(Ignoring the "logohedron" for a moment)

**A plane** serves as a visual lower boundary   
> (If you have trouble finding things in the code at first, click anywhere in the code and press `Command + f` on a Mac or `Control + f` on a PC and type the word you want to "find")

#### The Plane
* Its `position="0 0 -4"` shows that it has been moved forward, along the _negative z axis_ to bring into the camera's field of view
* You may also note its `rotation="-90 0 0"` —this is because planes default to an upright orientation and we want this to lie flat 

> ### **CHALLENGE: Break Things**  
* Make the ground plane's `position="0 0 0"` then click and drag on the screen to find where it went  
* Using the arrow or WASD keys, move forward till your (POV) moves _inside the sphere_

**—huh-WHUHAPPEN?—**

* **REASONS YOU CAN'T SEE SOMETHING IN YOUR SCENE:**  
1. You positioned it out of your camera view  
2. The wrong side is facing you  
3. Code error  

#### A Cylinder 
Stands "upright" on the ground plane
* Its `height: 1.5`
* Its `position="1 0.75 -3"`

> **THREE PART CHALLENGE: Measure Up**  

### ONE: Riddle me This
The "ground plane" is positioned at `y=0`   
* The cylinder is positioned at `y=0.75`  
* The cylinder's y position is exactly half of its `height: 1.5`  
**WHY?**

### TWO: Place the Sphere on top of the Cylinder 
#### A Sphere 
Stands on the ground plane 
* Spheres don't have _a height attribute_ -instead they have [_a radius_](https://commons.wikimedia.org/wiki/File:Simple_sphere_with_radii.svg)
* The height of a "round" sphere will be _double the length of the radius_
* If I place the center of my sphere one radius above the _height_ of my cylinder (making its x and z positions identical to the cylinder's) the sphere will appear to rest atop the cylinder
* The cylinder's `height: 1.5`  plus the sphere's `radius: 1.25`  equals:  
**The Sphere should be positioned at y=2.75**

### THREE: Place the Box atop the sphere atop the cylinder
#### A box 
Stands on the ground plane

* The box has height, width and depth attributes, all, in this case, equal (making it a _cube_) 
    * Placing it at   
    `y=cylinder height + (sphere radius x 2) +  1/2 box height` puts the box on top of the sphere, on top of the cylinder  
    (You may have to move the cylinder deeper into the space (into the negative z numbers) to see all of this —remember to move the sphere's x and z coordinates to match the cylinder's!)  
    
> ### **CHALLENGE: Balancing Act**  
Can you rotate the box so that it appears to ballance exactly on one edge on top of the sphere? 

* Placing it at   
    `y=cylinder height + (sphere radius x 2) +  1/2 box height`  
    will not be accurate, because a square measures more between diagonal corners than its height

* * Let Wolfram Aplha <a href="https://www.wolframalpha.com/input?i=square+side+length+1" target="_blank">"do the math FOR you</a>  
(Check out the "diagonal length") 

* * The box is already rotated around its y axis  
Can you figure out how to make it rotate round its z axis _instead?_

> **CHALLENGE: More Geometries**  

Change the box to a "torus" (a donut) by typing "torus" instead of "box" after `geometry=primitive:`   
[**SEE MORE geometries**](https://aframe.io/docs/1.2.0/components/geometry.html#sidebar) and discover which numbers define them

> **CHALLENGE: Animation**  

There's an entity we should return to: the "logohedron"
* The name "logohedron" is made up; what geometric shape is it _really?_
* It's animated —can you, apply the same kind of animation to the box? 
* Can you explain what all parts of the animation code do? 
* * Try breaking it! Change the values (numbers) or delete elements of code —see what _happens!_

-----
-----


