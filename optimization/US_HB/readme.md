# Unsteady Harmonic Balance 2D Multizone Axial Turbine
This folder contains an optimization test case representing a two-dimensional stator-rotor domain of an axial turbomachine. 
For the steady-state version of this same test case, please refer [here](../ST_MP).
 
The case itself is identical to the simulation case found [here](.../simulation/US_HB). More info on flow simulation runs can be found there.

### Setup

The shape parameterization method used is Free Form Deformation. The FFD boxes are shown in the figure below.

![A1_FFD](./figures/FFD.png) 

### Run
This shape optimization was only performed and checked functional in the *feature_TMZHB_temp* branch of *SU2*.
As discussed in much more detail in the Bitbucket *SU2* tutorial series, the test case can be run in series using

``shape_optimization.py -f a1_air_HB.cfg -n <number of cores> -g <gradient> -z <number of zones>``

Both the config and mesh files are present in this folder.




