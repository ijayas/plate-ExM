# plate-ExM resources
This repository contains the resources for adopting 3D printable ExM microplates for 4x expansion microscopy and distortion tracking through pre- and post-ExM analysis.

You can download the Fusion 360 CAD files for the plate, the lid, and the silicone rubber inserts from Links: [plate+lid](https://a360.co/40CkanE/) and [inserts](https://a360.co/40CkanE/).

--- Data supplement---
--- Title: Geometry-preserving Expansion Microscopy microplates enable high fidelity 
nanoscale distortion mapping

The zip file contains the following directories and subdirectories. The files, recommended software, calling code and relevance to the main manuscript are included in the notes below:

(i)	“STL files” – Includes .stl file formats of the Expansion Microscopy microplate components. These files can be opened with any CAD software (e.g. Fusion 360) or any opensource 3D printer slicer programme (e.g. Chitubox v1.9.5)
(ii)	“Image alignment & distortion analysis code” – Directory containing the ImageJ macros and custom-written Python scripts for the analysis pipeline described in the main manuscript, from image scaling and alignment to for distortion plotting and RMS Error analysis and plotting. Subdirectories include:
a.	“Distortion analysis and RMSE plotting code” – Directory contains custom-written Python scripts for updated distortion analysis, plotting, RMS error calculation, and code for combining the plots. Each .py file can be run with any Python distribution. Dependency libraries and modules (all opensource) include numpy, os, cv2, skimage, and tifffile
b.	“Basic Align Macro.ijm” – ImageJ macro for basic image alignment of pre- and post-Expansion Microscopy images. Refer to https://imagej.nih.gov/ij/developer/macro/macros.html#tools on how to install and run ImageJ macros.

(iii)	“Example data and analysis scripts” – Directory containing example datasets and worked examples of analysis. Subdirectories include:
a.	“Single-channel_HeLa_cells”. Worked example of single-colour dataset of a cluster of HeLa cells stained with NHS-AZ488. Folder includes pre-Expansion and post-Expansion images (.tif format), overlays of the pre- and post-Expansion images along with distortion vector maps, and plots of normalised RMS error (in % values) against measurement length scale (in micrometers) saved as numpy arrays (.npy format). This can be called in using a Python code similar to:
numpy.load("file name")
b.	“Multiplexed_Drosophila_wing”. Worked example of two-colour dataset of Drosophila fly wing tissue images stained with NHS-Alexa647 and anti-E-cad-GFP/Alexa488. Folder includes pre-Expansion and post-Expansion images (.tif format), overlays of the pre- and post-Expansion images along with distortion vector maps, and plots of normalised RMS error (in % values) against measurement length scale (in micrometers) saved as numpy arrays (.npy format).
c.	“Multiplexed_HeLa_cells”. Worked example of two-colour dataset of cultured HeLa cell images stained with NHS-AZ488 and antibodies. Each folder includes pre-Expansion and post-Expansion images (.tif format), overlays of the pre- and post-Expansion images along with distortion vector maps, and plots of normalised RMS error (in % values) against measurement length scale (in micrometers) saved as numpy arrays (.npy format):
I.	“KDELAlexa594_NHSAZ488” – antibody staining against KDEL
II.	“NUP98Alexa594_NHSAZ488” – antibody staining against Nups98

d.	“Distortion Correction”. Folder contains two subfolders of output images from distortion corrections using the Linear Stack Alignment with SIFT plugin in ImageJ v1.54f. Each example consists of a pre- and post-Expansion image file, and the ‘corrected’ image file generated with 5, 10, and 50 voxel B-spline sampling.

These files are placed in public domain under Creative Commons license CC BY-ND 4.0
