# CFD_lid-drivenCavityFlow

This CFD report displays the results of the Lid-driven Cavity Flow. The Lid-driven Cavity Flow depicts how a simple shear-driven motion in a confined domain leads to complex vortex structures and recirculation patterns. The shear motion that is applied moves the fluid and generates circulation inside the cavity. A primary vortex forms at the center, with secondary vortices appearing in corners at higher Reynolds numbers. It demonstrates how boundary layers develop alomg walls and how recirculation zones emerge in confined geometries.
It is used to validate numerical methods, solvers and mesh quality because the geometry is simple but the flow physics are non-trivial. 
It provides a controlled environment to test discretization schemes, turbulence models and solver stability. Essential physics phenomena like vortex dynamics, seperation, and secondary flows without geometric complexity are captured. It is also used to check how solvers handle increasing Reynolds numbers and mesh refinement.

### Equations
The governing equations are the incompressible Navier-Stokes equations along with the continuity equation:

The continuity equation ensures there is no incompressibility where there is no density change and no sources of mass

$$
\nabla \cdot \mathbf{u} = 0
$$

The Navier-Stokes equation fluid inertia, pressure gradient and viscous diffusion

$$
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{u} = -\frac{1}{\rho}\nabla p + \nu \nabla^2 \mathbf{u}
$$



### Mesh:

<img width="1011" height="460" alt="wireframe2d-cavity" src="https://github.com/user-attachments/assets/f0ea5cdf-59e4-437c-a783-d7397d4a9495" />

This mesh has been refined from 20cm x 20cm to 50cm x 50cm.

### Boundary Conditions:

* Top lid (moving lid): u = Ulid, v = 0
* Other walls (Stationary walls): u = 0, v = 0
* No-slip condition applied everywhere

### Fluid Properties:
* Laminar

### Simulation Notes:

* solved with icoFoam on a uniform mesh
* Mesh resolution and grading were refined to improve accuracy
* ParaView used for velocity vectors, streamlines, and pressure contours

### Simulation Results:
Velocity:
<img width="1011" height="460" alt="cavity-velocity" src="https://github.com/user-attachments/assets/84f9d3a4-6df0-49e4-97eb-743410534c97" />
<img width="1011" height="460" alt="cavity-velocity tube" src="https://github.com/user-attachments/assets/079b7e9a-5d18-4496-a5d0-231a1284329d" />
<img width="1011" height="460" alt="cavity-velocity glyph" src="https://github.com/user-attachments/assets/b28fc001-318a-46a3-86a2-d27dec515e39" />
<img width="500" height="460" alt="cavity-graph" src="https://github.com/user-attachments/assets/5439dfdb-ef27-4ebe-b5df-c63d9ca7cdf0" />



Pressure:
<img width="1011" height="460" alt="cavity-pressure contour" src="https://github.com/user-attachments/assets/ee91ec3a-c60e-40f1-9c56-074a3de07fd2" />
<img width="1011" height="460" alt="cavity-pressure glyph" src="https://github.com/user-attachments/assets/4a90a4e1-f115-48fb-927a-c89189dc1ee2" />
<img width="1011" height="460" alt="cavity-pressure tube" src="https://github.com/user-attachments/assets/24c2aa64-a5ee-425c-bf9a-3aacdeb41ec7" />



