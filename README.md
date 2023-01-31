The DVC simulator is the 3D cousin of the DIC Simulator. It’s also a Matlab-based GUI that assesses how “well” a particular user-provided volumetric image correlates given 4 different simulated 3D displacement fields. The import format for the 3D image stack is .mat, which is a 3 dimensional matrix (intensity values are stored at every x,y,z position). The purpose of the simulator is the same as for the DIC simulator, and we have found it to be of significant time and effort savings.

## Important pages
* [Download latest version v1.1!](https://github.com/FranckLab/DVC-Simulator/releases)
* [Example data](https://app.globus.org/file-manager?origin_id=86401693-5974-4013-b498-eb4484e08eb4&origin_path=%2FFranckLab%2FDVC-Simulator_example%2F)
* [FAQ](https://github.com/FranckLab/DVC-Simulator/blob/master/README.md#faq)
* [Questions/Issues](https://github.com/FranckLab/DVC-Simulator/issues)
* [Cite](https://github.com/FranckLab/DVC-Simulator/blob/master/README.md#cite)
* [Franck Lab](http://franck.engin.brown.edu)

# Purpose
The purpose of the stimulator is to allow the user to check if the speckle pattern and intensity in the volume images are good enough for DVC to compute displacement reliably. If the results look good, the user can use FIDVC algorithm to compute displacements between volume images. 

Here, the Matlab script synthetically deforms the input volume image according to a prescribed displacement fields. Then, the DVC algorithm computes the displacements, which can be compared with the prescribed displacements to see if the match. The Matlab-GUI also plots strains. 

# Running the Matlab-GUI

## Steps
1. Save the 3D image stack, a 3 dimensional matrix (intensity values are stored at x, y and z position), in .mat file in the folder containing the matlab script. Download the [example data](https://drive.google.com/folderview?id=0ByhZqlrbo5srUDI5clRCM3VCX3M&usp=sharing) for an example test on your computer. 
2. Have the same folder as the directory in Matlab and run the following command in command window to open the GUI: `DVC_simulator`
3. Use the upload button load the image stack.
4. If needed, resize the volume to a decrease the size. 
5. Adjust the subset size and subset spacing if needed, or can leave it at default value.
6. Adjust the prescribed strain and translation, or can leave it at the default value.  
7. Hit **Go!**

## Health warning!
The DVC simulator requires a 3D stack to be read in, which depending on the volume size can require a **large amount of RAM** in Matlab, and thus when running the simulator from a laptop, we strongly suggest to use the resize option within the GUI to decrease the total stack dimensions. My macbook air can only handle 128 x 128 x 96 sufficiently. 

Also, the algorithm expects the speckle pattern to cover the entire field-of-view of the image and will either error out or provide eroneous result if this is not the case.

# FAQ
**The GUI looks squashed and button don't appear properly, what should I do?**

The GUI in newer versions of Matlab and high resolution screens, can sometimes get squashed with various buttons and icons not appearing properly. The easiest way to solve this issue is to resize the GUI layout manually on your computer. Use the command `guide DVC_simulator.fig` and resize the buttons.


**What is the recommended minimum size of the input image stack?**

We recommend that the input image stack should have at least have 96 pixels in each dimension. 


# Cite
If used please cite:
[Estrada, J., Franck, C.,”Intuitive Interface for the Quantitative Evaluation of Speckle Patterns for Use in Digital Image and Volume Correlation Techniques”, J. Applied Mechanics, 2015.](https://appliedmechanics.asmedigitalcollection.asme.org/article.aspx?articleid=2336782)

```bibtex
@article{estrada2015intuitive,
  title={Intuitive Interface for the Quantitative Evaluation of Speckle Patterns for Use in Digital Image and Volume Correlation Techniques},
  author={Estrada, Jonathan B and Franck, Christian},
  journal={Journal of Applied Mechanics},
  volume={82},
  number={9},
  pages={095001},
  year={2015},
  publisher={American Society of Mechanical Engineers}
}
```


# Contact and support
For questions, please first refer to [FAQ](https://github.com/FranckLab/DVC-Simulator#FAQ) and [Questions/Issues](https://github.com/FranckLab/DVC-Simulator/issues). Add a new question if similar issue hasn't been reported. We shall help you at the earliest. The author's contact information can be found at [Franck Lab](http://franck.engin.brown.edu).



