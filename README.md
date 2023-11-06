1. Heirarchical body
The bugs in the scene are heirarchical in terms of their segments. The bugs are children of the flower, 
so any motion of the flower would result in the bugs moving with it.
2. Textures
I used three textures in this project. The first texture was for the sky. This was taken from https://opengameart.org/content/seamless-sky-backgrounds, 
and is free for public use. The second texture was a procedural texture that I wrote for the flower centre. This texture 
is a gradient from orange to yellow. The third texture was a procedural texture that I wrote for the flower petals. This
texture generates a random pattern of two color lines to resemble some flower petals. 
3. ADS vertex -> Fragment shader
The ADS lighting from the vertex shader was successfully moved to the fragment shader. In addition, I modified the 
lighting to work on textures. This allowed me to apply the lighting to the flower petals and the flower centre.
4. Phong -> Blinn-Phong
I modified the ADS lighting to use Blinn-Phong lighting instead of Phong lighting.
5. Custom heart shader
I wrote a custom shader which projects the shape of a heart onto the sky behind the bugs. I wrote this shader based on a 
equation for a heart shape. The shader effect is mixed with the underlying texture, giving it a translucent effect
6. 360 fly around camera
This was done by moving the eye location in a circle around the flower.
7. Real time
8. Frame rate display