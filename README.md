The DVC simulator is the 3D cousin of the DIC Simulator. It’s also a Matlab-based GUI that assesses how “well” a particular user-provided volumetric image correlates given 4 different simulated 3D displacement fields. The import format for the 3D image stack is .mat, which is a 3 dimensional matrix (intensity values are stored at every x,y,z position). The purpose of the simulator is the same as for the DIC simulator, and we have found it to be of significant time and effort savings.

### Important pages
* [Download latest version v1.0!](https://github.com/FranckLab/DVC-Simulator/releases)
* [Example data](http://google.com)
* [FAQ](https://github.com/FranckLab/DVC-Simulator/blob/master/README.md#faq)
* [Questions/Issues](https://github.com/FranckLab/DVC-Simulator/issues)
* [Franck Lab](http://franck.engin.brown.edu)

## Purpose
The purpose of the stimulator is to allow the user to check if the speckle pattern and intenisty in the volume images are good enough for DVC to compute displacement reliably. If the results look good, the user can use FIDVC algorithm to compute displacments between volume images. 

Here, the Matlab script syntheticaly deformes the input volume image according to a prescribed displacement fields. Then, the DVC algorithm computes the displacements, which can be compared with the prescribed displacements to see if the match. The Matlab-GUI also plots strains. 

## Running the Matlab-GUI

### Steps
1. Save the 3D image stack, a 3 dimensional matrix (intensity values are stored at x, y and z position), in .mat file in the folder containing the matlab script. 
2. Have the same folder as the directory in Matlab and run the following command in command window to open the GUI: `DVC_simulator`
3. Use the upload button load the image stack.
4. If needed, resize the volume to a decrease the size. 
5. Adjust the subset size and subset spacing if needed, or can leave it at default value.
6. Adjust the prescribed strain and translation, or can leave it at the default value.  
7. Hit **Go!**

### Health warning!
The DVC simulator requires a 3D stack to be read in, which depending on the volume size can require a **large amount of RAM** in Matlab, and thus when running the simulator from a laptop, we strongly suggest to use the resize option within the GUI to decrease the total stack dimensions. My macbook air can only handle 128 x 128 x 96 sufficiently. 

## FAQ
*
  * *The GUI looks squashed and button don't appear properly, what should I do?*
  * The GUI in newer versions of Matlab and high resolution screens, can sometimes get squashed with various buttons and icons not appearing properly. The easiest way to solve this issue is to resize the GUI layout manually on your computer. Use the command `guide DVC_simulator.fig` and resize the buttons.


*What is the recommened minimum size of the input image stack?*

We recommend that the input image stack should have at least have 96 pixels in each dimension. 


## Author

## Contact and support
For questions, please first refer to [FAQ](https://github.com/FranckLab/DVC-Simulator#FAQ) and [Questions/Issues](https://github.com/FranckLab/DVC-Simulator/issues). Add a new quesiton if similar issue hasn't been reported. We shall help you at the earlist. The author's contact information can be found at [Franck Lab](http://franck.engin.brown.edu).



