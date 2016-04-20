
Ki67 Breast
==========
This software refers to this article published in Applied Immunohistochemistry & Molecular Morphology.

Prerequisites and software installation
This software requires installation of imageJ, an open source software written in Java, available for Linux, Mac OS X and Windows. ImageJ is available [here](https://imagej.nih.gov/ij/). Basic understanding of ImageJ will facilitate installation.
Current software (**BreastKi67.txt**) is a "toolset" written in imagej macro language and requires to be installed in the following directory:
```
→ ImageJ → macros → toolsets.
```

One additional "plugins" is required:
* Color Deconvolution plugin written by Gabriel Landini is available [here] (http://www.mecourse.com/landinig/software/cdeconv/cdeconv.html) with documentation.

Colour deconvolution name is: "Colour_Deconvolution.class" and has to be installed in the following directory
```
→ ImageJ → plugins
```
Prerequisites for IHC analysis
==========
Since the purpose of this analysis is to be a predictor of MYC dysregulation, It is expected that pre-analytical and analytical factors related to tissue handling are optimized and controlled as other [class II Biomarkers] (http://www.ncbi.nlm.nih.gov/pubmed/26286753)

Chromogen color properties (DAB and RED) might vary significantly among laboratories: for optimal color separation using color deconvolution algarithm, it is expected that individual laboratory measures as precisely as possible the "Optical Density (OD) Unitary Vectors" of each individual stain. This is achieved using preparation with pure stain (i.e. DAB alone and RED alone). Measured OD Unitary Vectors can be set in the software (see icon action below).
In order to measure OD Unitary Vectors, you can utilize this [open source software] (http://imagejdocu.tudor.lu/doku.php?id=plugin:color:colour_deconvolution:optimizing_selection_of_unitary_optical_density_vectors:start). For more details, please refer to this article [Color deconvolution. Optimizing handling of 3D unitary optical density vectors with polar coordinates.](http://www.ncbi.nlm.nih.gov/pubmed/23016461).

Operator is expected to grab multiple areas of viable tumour with maximal proliferation (High Ki67). The picture should be saved without compression as an ImageJ stack.

Operator is expected to grab a picture with a priori correction of background illumination as explained [here] (http://imagejdocu.tudor.lu/doku.php?id=howto:working:how_to_correct_background_illumination_in_brightfield_microscopy) by Gabriel Landini.

This involves multiple steps a) Image acquisition of a white field without oversaturation and white balance of RGB channels b) Image acquisition of a black field c) Image acquisition of the tissue specimen and d) the correction itself. These steps are available in the offered software if you use a Qimaging Camera. If not, the code could be adapted using a different camera and for instance a TWAIN plugin: see [here](https://imagej.nih.gov/ij/plugins/index.html#acq). This requires help from IT person or someone familiar with ImageJ and coding.
Software utilization
---------------
![hello](/pictures/KI67BreastImageJ.png) 

Icon action | Description
------------ | -------------
![](/pictures/selector.png) | Select BreastKi67 to launch the BreastKi67 toolbar 
![](/pictures/camera.png) | This only works if a [Qimaging camera](http://www.qimaging.com/) is installed and associated AcquireQCam plugin is installed to capture image  
![](/pictures/key.png) | Open a stack of image. You can download and use "sample.tif" (see below)  
![](/pictures/cytokerat.png) | Under your surveillance assess the best cytokeratin mask (The algorithm will provide the best threshold).
![](/pictures/ki67.png) | Under your surveillance assess the best cytokeratin mask (The algorithm will provide the best threshold).
![](/pictures/lunettes.png) | Verify the creates mask - if needed repeat previous steps.
![](/pictures/sigma.png) | Calculate the Vv ratio.
![](/pictures/setup.png) | Various setup - aome menu will require to check one box to exit (read lableing).


Image test and results
-----------------
You can use this small [stack](/pictures/sample.tif) to test the software. A minimum of 2 pictures is expected per stack. The following picture is only a representation of the stack available above.

<a href="url"><img src="/pictures/sample.jpg" align="center" height="500" width="500" ></a> 

Feedback
-----------------

Please send me your feedback at gilbert.bigras@ahs.ca

