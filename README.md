
article
========

Particle is a package for simple physics simulations.
I will document this better, but for now, look
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

  
