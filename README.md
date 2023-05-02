Download Link: https://assignmentchef.com/product/solved-computergraphics-assignment-12-glsl-brdf
<br>
5/5 - (1 vote)

GLSL BRDF

In this assignment, you have to write the code for computing the final color of the pixel for 5 different BRDF models. The application contained in index.html, has a user interface similar to the one of Example 04. Depending on the requested shader, the interface below changes to allow the user playing with the elements specific for the selected model. Shader code to compute the final pixel color should be written in file shaders.js. The code, written in GLSL, can use the following variables to find the elements necessary to compute the final color:

The shader can find the required information in the following variables:

vec3 fs_pos;

float SpecShine; float DToonTh; float SToonTh;

vec4 diffColor; vec4 ambColor; vec4 specularColor; vec4 emit;

vec3 normalVec; vec3 eyedirVec;

// Position of the point in 3D space

// specular coefficient for both Blinn and Phong // Threshold for diffuse in a toon shader// Threshold for specular in a toon shader

// diffuse color// material ambient color // specular color// emitted color

// direction of the normal vecotr to the surface // looking direction

The applications supports up to three lights, whose direction is contained into variables:

vec3 lightDirA; vec3 lightDirB; vec3 lightDirC;

and whose intensity can be found into the following variables:

vec4 lightColorA; vec4 lightColorB; vec4 lightColorC;

ambient light color contribution is returned into: vec4 ambientLight;The final color computed from the shader should be inserted into variable: vec4 out_color;

The following GLSL standard procedure can be helpful in solving this exercise:

<pre>normalize()cos()radians()pow()dot()</pre>

<pre>length()clamp()reflect()max()</pre>

whose reference can be found at pages 7 and 8 of the official WebGL reference card from Kronos Group (webgl20-reference-guide.pdf, enclosed in this ZIP file of Assignment 11).

To check the correctness of your shader, you can visually compare your results with the ones that can be obtained by Example E04, available on the Beep page of this course, after properly setting the same type of lights and materials.