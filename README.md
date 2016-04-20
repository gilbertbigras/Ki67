
IHC MYC
==========
This software refers to this article published in Applied Immunohistochemistry & Molecular Morphology.

Prerequisites and software installation
This software requires installation of imageJ, an open source software written in Java, available for Linux, Mac OS X and Windows. ImageJ is available [here](https://imagej.nih.gov/ij/). Basic understanding of ImageJ will facilitate installation.
Current software (**MYC_IHC.txt**) is a "toolset" written in imagej macro language and requires to be installed in the following directory:
```
→ ImageJ → macros → toolsets.
```

Two additional "plugins" are required:
* Color Deconvolution plugin written by Gabriel Landini is available [here] (http://www.mecourse.com/landinig/software/cdeconv/cdeconv.html) with documentation.
* Euclidean minimum spanning tree plugin written by Gilbert Bigras available [here] (http://imagejdocu.tudor.lu/doku.php?id=plugin:morphology:euclidean_minimum_spanning_tree:start).

Colour deconvolution and Euclidean minimum spanning tree plugin names are respectively: "Colour_Deconvolution.class" and "e_mst.jar". Both files (plugins) have to be installed in the following directory
```
→ ImageJ → plugins
```
Prerequisites for IHC analysis
==========
Since the purpose of this analysis is to be a predictor of MYC dysregulation, It is expected that pre-analytical and analytical factors related to tissue handling are optimized and controlled as other [class II Biomarkers] (http://www.ncbi.nlm.nih.gov/pubmed/26286753)

Chromogen color properties (DAB and hematoxylin) might vary significantly among laboratories: for optimal color separation using color deconvolution algarithm, it is expected that individual laboratory measures as precisely as possible the "Optical Density (OD) Unitary Vectors" of each individual stain. This is achieved using preparation with pure stain (i.e. DAB alone and hematoxylin alone). Measured OD Unitary Vectors can be set in the software (see icon action below).
In order to measure OD Unitary Vectors, you can utilize this [open source software] (http://imagejdocu.tudor.lu/doku.php?id=plugin:color:colour_deconvolution:optimizing_selection_of_unitary_optical_density_vectors:start). For more details, please refer to this article [Color deconvolution. Optimizing handling of 3D unitary optical density vectors with polar coordinates.](http://www.ncbi.nlm.nih.gov/pubmed/23016461).

Operator is expected to grab an area of viable tumour with the most intense IHC staining. The picture should be saved without compression or with lossless compression (general principle related to good practice in image analysis). NB: the picture available below is compressed because of limitation of the GitHub repository.

Operator is expected to grab a picture with a priori correction of background illumination as explained [here] (http://imagejdocu.tudor.lu/doku.php?id=howto:working:how_to_correct_background_illumination_in_brightfield_microscopy) by Gabriel Landini.

This involves multiple steps a) Image acquisition of a white field without oversaturation and white balance of RGB channels b) Image acquisition of a black field c) Image acquisition of the tissue specimen and d) the correction itself.
Software utilization
---------------
![hello](/pictures/ImageJ_034.png) 

Icon action | Description
------------ | -------------
![](/pictures/camera.png) | This only works if a Qimaging camera is installed and associated  
![](/pictures/key.png) | Open a stack of image. You can download and use "sample.tif" (see below)  
![](/pictures/cytokerat.png) | Under your surveillance assess the best cytokeratin mask (The algorithm will provide the best threshold).
![](/pictures/ki67.png) | Under your surveillance assess the best cytokeratin mask (The algorithm will provide the best threshold).
![](/pictures/lunettes.png) | Verify the creates mask - if needed repeat previous steps.
![](/pictures/sigma.png) | Calculate the Vv ratio.
![](/pictures/setup.png) | Various setup - aome menu will require to check one box to exit (read lableing).


Image test and results
-----------------
You can use this small picture (test.jpg) to test the software.

<a href="url"><img src="/pictures/test.jpg" align="center" height="500" width="500" ></a> 

At the end, a scatterplot shows the (x,y) (ratio EMST, CV) coordinates of the patient among the original data utilized for the article published in Applied Immunohistochemistry & Molecular Morphology. If you reproduce your own in house study, you might have different logistic regression parameters that you can set in the software (see icon action above).

<a href="url"><img src="/pictures/results.png" align="center" height="500" width="500" ></a>


Feedback
-----------------

Please send me your feedback at gilbert.bigras@ahs.ca

