## CSC 305 Assignment 2
My scene depicts two bugs on a flower. These bugs kiss each other, and when they do so a heart appears behind them in the
sky. I used Lab 5 as my base code, and added the following features:

### 1. Hierarchical body

The bugs in the scene are hierarchical in terms of their segments. The bugs are children of the flower, 
so any motion of the flower would result in the bugs moving with it. The bugs segments are drawn hierarchically, and 
the motion is done by rotating each segment before it is drawn. I aimed to make the motion of the bugs as close to the 
motion of inchworms as possible. In addition, the bugs have eyes and antennae which are children elements of the bugs.

### 2. Textures

I used three textures in this project. The first texture was for the sky. This was taken from [OpenGameArt](https://opengameart.org/content/seamless-sky-backgrounds),
and is free for public use. The second texture was a procedural texture that I wrote for the flower centre. This texture 
is a gradient from orange to yellow, with the color being orange at the outside and yellow in the centre. The third 
texture was a procedural texture that I wrote for the flower petals. This texture generates a random pattern of two 
color lines to resemble the patten some flower petals have. 

### 3. Moving ADS lighting from vertex to fragment shader

The ADS lighting from the vertex shader was successfully moved to the fragment shader. In addition, I modified the 
lighting to work on the textures I created. This allowed me to apply the lighting to the flower petals and the flower centre.

### 4. Converting Phong lighting to Blinn-Phong

I modified the ADS lighting to use Blinn-Phong lighting instead of Phong lighting. This was done by calculating the
vector H between L and V, and using this vector in the lighting equation instead of the vector R. This resulted in 
a more realistic lighting effect.

### 5. Custom heart shader

I wrote a custom shader which projects the shape of a heart onto the sky behind the bugs. I wrote this shader based on an 
equation for a heart shape. The shader effect is mixed with the underlying texture, giving it a translucent effect. For
each fragment in the sky, it is passed in to a function, and this function determines if the value of that fragment falls
within the bounds of the heart shape. If it does not, it is rasterized as normal. If it does, the color of the heart is 
blended with the sky texture. The heart color is a gradient that varies with x and y coordinates, as well as time. This gives
it a gradient effect that changes as time passes.  

### 7. 360 fly around camera

In the scene, the camera appears to be continuously flying around the flower. This was done by moving the eye location 
in a circle around the flower, while keeping the coordinate that it should look at constant. 

### 7. Real time

This scene is rendered in real time.

### 8. Frame rate display

Below the animation, the frame rate is displayed. This is updated once every 2 seconds. The frame rate is calculated by
taking the number of frames rendered in the last 2 seconds, and dividing it by the time elapsed.