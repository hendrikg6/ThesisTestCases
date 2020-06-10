# Meshing
Meshing for this 2D turbine stage is performed using the in-house and open-source *UMG2* software.

Because of limitations in *UMG2* and *SU2_PERIO* applied to multizone meshes, stator and rotor blades are meshed separately at first. The [stator directory](1_stator) contains the files corresponding to the mesh of the stator row. The respective rotor mesh inputs are found in the [rotor directory](2_rotor).

The *Dd* folders in each of the directories contain the files containing inputs and settings for *UMG2*.

In order to generate the mesh, open a console and navigate to the respective directory. Please note that this is the directory one level above the *Dd* folder, and not the *Dd* director itself. 

The software consists of four executables that have to be run in sequence to generate a hybrid mesh. 
Running only the first three programs creates an unstructured mesh. Paths to the executables can be made in the Linux *bashrc* to make easier use of these executables.

* mcrv.exe:  builds the curves 
* bgrid.exe: builds the background grid
* umg2d.exe: builds the unstructured grid
* hyb2d.exe: builds the hybrid grid

After creating the meshes, they can be made periodic by running *SU2_PERIO*. This will require an *SU2* config file. After creating both periodic meshes (stator and rotor), they can be merged into one *.su2* file.
In order to make the mesh file functional, the markers need to be changed as follows:
* Change NZONE to 2
* Change the IZONE of the rotor row to 2
* Change outflow to outmix for the stator row
* Change inflow to inmix for the rotor row
* Change wall1 to wall2 for the rotor row
* Change periodic1 and periodic2 to periodic3 and periodic4 in the rotor row
