# Final Graphics Engine - James Smith & Jack Cruse Pd. 10 Stuyvesant High School Computer Graphics

## Newly Implemented Features:
* OBJ Mesh files - Works with n-vertice faces(not restricted to any amount of vertices for a face)


# Syntax

## Stack Commands
`push`	- makes a new top level of the transformation stack and copies the previous top to the new top level

`pop`	- pops off the top of the coordinate system stack

## Transformations
`move x y z [knob]` - translates all objects in the coordinate system by x y z
`scale x y z [knob]`		- scales the dimensions of all objects in the coordinate system by x y z
`rotate x|y|z degrees [knob]`	- rotates all objects in the coordiante system about the specified axis with respect to the center of the coordinate system 
* Only specify one axis, x, y, or z per rotation instruction

## Image creation
`sphere x y z r` - creates a sphere
* x y z = center of sphere
* r = radius

`torus x y z r0 r1` - creates a torus
* x y z = center of torus
* r0 = outer radius
* r1 = inner radius

`box x0 y0 z0 h w d` - creates a box
* x0 y0 z0 = top left corner of the box
* h w d = height width and depth

`line x0 y0 z0 x1 y1 z1` - creates a line
* x0 y0 z0 = start point
* x1 y1 z1 = end point

`mesh filename` - load a mesh or set of edges from an obj file into the pointlist and or edge list directly(**OBJ format must have single space separations**)

## Knobs/Animation
`basename name` - sets the base filename to save the gif and its generated images under.

`set knobname value` - sets a knobs value (in the symbol table).

`frames num_frames`	- How many frames to generate all together.

`vary knob_name start_frame end_frame start_val end_val` - vary a knob from start_val to end_val over the course of start_frame to end_frame linearly

## Misc
`//` - comment to the end of a line

`save filename` - save the image in its current state under the name "filename."

`display`	- display the current image on the screen
