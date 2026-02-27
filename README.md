# CFD_lid-drivenCavityFlow

The lid-driven Cavity Flow depicts how a simple shear-driven motion in a confined domain leads to complex vortex struactures and recirculation patterns. The shear motion that is applied moves the fluid and generates circulation inside the cavity. A primary vortex forms at the center, with secondary vortices appearing in corners at higher Reynolds numbers. It demonstrates how boundary layers develop alomg walls and how recirculation zones emerge in confined geometries.
It is used to validate numerical methods, solvers and mesh quality because the geometry is simple but the flow physics are non-trivial. 
It provides a controlled environment to test discretization schemes, turbulence models and solver stability. Essential physics phenomena like vortex dynamics, seperation, and secondary flows without geometric complexity are captured. It is also used to check how solvers handle increasing Reynolds numbers and mesh refinement.

### Equations
The governing equations are the incompressible Navier-Stokes equations along with the continuity equation:

Continuity:

