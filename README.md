
Particle
========

`Particle` is a package for simple physics simulations.
The idea is to set up a particle with a certain
mass, initial position, initial velocity, and shape
(rectangle or ellipse for now).  Then to define a field,
e.g. the gravitational field.  The package gives tools
for constructing  

```
     orbit = [a, f a, f^2 a, ... , f^n a]
```

where   `a`   is the particle in its initial state and
the function   `f`   is the "next-state" function which
evolves the particle according to some discrete version
of Newton's laws of motion.  The resulting list
of particles can then be rendered as a list of SVG
elements by

```
    renderedOrbit = List.map draw orbit
```

I will document this better later , but for now, look
in the examples folder for demo code:

Demo 1:

```
   $ cd examples
   $ elm make StaticBouncingBall.elm
```

Demo 2:

```
   $ elm make BouncingBall.elm
```

In both cases a ball is subject to two forces.  The first
is the constant downward force of gravity.  The second
is a short-range upward force localized in the "floor".
This force decays exponentially with height.

NOTE: If you look at the simulations, you will see
that "the angle of reflection is equal to the
angle of incidence."  This is achieved by solving the 
equations of motion, not by using ray optics.

NOTE: I need to do some optimization in Demo 2.  The
simulation slows down as it progresses.  Pull requests
appreciated!  
