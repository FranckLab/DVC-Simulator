The DVC simulator is the 3D cousin of the DIC Simulator. It’s also a Matlab-based GUI that assesses how “well” a particular user-provided volumetric image correlates given 4 different simulated 3D displacement fields. The import format for the 3D image stack is .mat, which is a 3 dimensional matrix (intensity values are stored at every x,y,z position). The purpose of the simulator is the same as for the DIC simulator, and we have found it to be of significant time and effort savings.

### Important pages
* [Download latest version!](http://google.com)
* [Example data](http://google.com)
* [FAQ](http://google.com)
* [Questions/Issues](http://google.com)
* [Franck Lab](http://franck.engin.brown.edu)

## Application
The purpose of the stimulator is to allow the user to check if the speckle pattern and intenisty in the volume images are good enough for DVC to compute displacement reliably. If the results look good, the user can use FIDVC algorithm to compute displacments between volume images. 

Here, the Matlab script syntheticaly deformes the input volume image according to a prescribed displacement fields. Then, the DVC algorithm computes the displacements, which can be compared with the prescribed displacements to see if the match. The Matlab-GUI also plots strains. 

## Running the Matlab-GUI

### How?
Save the 3D image stack, a 3 dimensional matrix (intensity values are stored at x, y and z position), in .mat file in the folder containing the matlab script. Have the same folder as the directory in Matlab and run the following command in command window to open the GUI:
```
DVC_simulator
```


### Health warning
The DVC simulator requires a 3D stack to be read in, which depending on the volume size can require a **large amount of RAM** in Matlab, and thus when running the simulator from a laptop, we strongly suggest to use the resize option within the GUI to decrease the total stack dimensions. My macbook air can only handle 128 x 128 x 96 sufficiently. 







