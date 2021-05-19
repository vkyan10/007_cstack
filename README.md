# 007_cstack
Implementation of relative coordinate system, through adding a coordinate system stack and modifying the parser:
- push - push a copy of the current top of the coordinate system (cs) stack onto the cs stack
- pop - removes the top of the cs stack 
- move/rotate/scale 
  - create a translation/rotation/scale matrix
  - multiply the current top of the cs stack by it
- box/sphere/torus
  - add a box/sphere/torus to a temporary polygon matrix
  - multiply it by the current top of the cs stack
  - draw it to the screen
  - clear the polygon matrix
- line/curve/circle
  - add a line to a temporary edge matrix
  - multiply it by the current top
  - draw it to the screen 
  - clear the edge matrix
- save - save the screen with the provided file name
- display - show the image
- note that the ident, apply and clear commands no longer have any use
