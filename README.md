# Field of View and Line of Sight in 2D

[View it in action][1] in your browser!

The idea is to find the field of view from a given point in a 2D world which has buildings.  Many resources on the web doing 360&#176; FoV exists; these have their FoV's distance and angle unbound.  This is simpler to design; arriving at a fast implementation is easier since -- if rightly done -- there would be no intersection queries every iteration of the loop to eat up performance.  However, the FoV here is different; it's limited both by angle and distance.  Care is taken to have an optimised solution that avoids unnecessary intersection tests so that it's usable in a game where multiple agents would need their FoV computed every frame.

This implementation is done in HTML5 Canvas/JavaScript for easy viewing but the idea is mathematical and can be implemented in any language.  The only library it uses is [glMatrix][3] for vector calculations.  The code is heavily commented and includes references to articles and books for someone to learn from it.

[The design document][2] has all the gory details, again with references for further study.

[1]: http://legends2k.github.io/2d-fov
[2]: http://legends2k.github.io/2d-fov/design.html
[3]: http://github.com/toji/gl-matrix
