# Thesis Test Cases
This repository contains a selection of test cases set up in the context of the master thesis work on 'Best Practices for Adjoint-based Shape Optimization of Turbomachinery Stages'. All cases correspond to a 2D stator-rotor turbine cascade.

#### 1. [Meshing](meshing) contains the background and input files required to set up the mesh for the test case in the in-house *UMG2* software.

#### 2. [Simulation](simulation) features the config and mesh files required to set up both [steady-state MP](simulation/ST_MP) and [unsteady HB](simulation/US_HB) flow simulations in *SU2*, along with instructions.

#### 3. [Optimization](optimization) explains and provides the config and mesh files required to set up both [steady-state MP](optimization/ST_MP) and [unsteady HB](optimization/US_HB) shape optimizations in *SU2*.

#### 4. [Various](various) contains a number of test cases and input files to *SU2* made for the purpose of the thesis. These do not contain any additional written information, but can be used for further exploration.

More detailed information on the test cases at hand, or more clarification on the background and purpose of these test cases can be found in the thesis report included [here](Master_Thesis_HJPM_Gaens.pdf).
