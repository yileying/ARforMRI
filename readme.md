# Instructions

## What does this AR WebApp support?

1.  multiple 3D objects
2.  multiple 2D images
3.  multiple (custom) markers
4.  adjustable position/angle/size of the 3D objects and images

## The current set-up

The HIRO marker controls 3D models of a human head; a custom marker controls a 3D model of a cube.

## How to use this AR WebApp

1. Upload the contents of the repo to a web server and open the index.html in your browser e.g.:  your.webserver.address/ARforMRI/index.html (opening a webpage directly from the local drive won't work). You can also open a demo from https://yileying.github.io/projects/2018ARforMRI/demo/ (mind this may be outdated)
2.  Allow the page to use camera
3.  Point the camera to the marker(s), e.g. [HIRO](https://jeromeetienne.github.io/AR.js/data/images/HIRO.jpg) and [a custom marker](markers/custommarker.png)
4.  Use the text input boxes on the top of the page to adjust the size / location / angle of the 3D models relative to the marker(s)
5.  Hide the text input boxes by clicking on the Hide/Show button on the top right corner
6.  Tick/untick the check boxes on the top to hide or show specific objects
7.  You can also move / rotate the marker(s) to project the models as you desire

## How to change/add 2D image(s) in this AR WebApp

The 2D image displayed in the WebApp is actually a 3D plane using the image as its texture. The obj/mtl files with 'image' in its filename is the 3D model of the plane.

To change the image:

1.  Upload your own image to the same folder where the obj/mtl files are
2.  Open the mtl file of the 3D plane, replace the filename of the image in the mtl file to match your own image

To add more images:

1.  Duplicate the existing obj/mtl files of the 3D planes, and rename them into Prefix+'image'+*.obj/mtl, e.g. humanimage1.obj/mtl. The Prefix part should be the same to the other obj/mtl files of 3D models.
2.  Upload the images to the same folder where the obj/mtl files are
3.  Open the mtl files of the 3D planes, replace the filenames of the image in the mtl files to match the images. **One 3D plane can only host one 2D image.**
4.  Follow the instruction in the code to include all the images

## How to use this AR WebApp for your own 3D models

1.  Save them as '*.obj' with '*.mtl' files, and rename to 'PrefixObject.obj/mtl', e.g. humanhead.obj/mtl. :
    *   Prefix part: e.g. patient name, dates. The prefix should be the same for all obj/mtl, otherwise the code will have to be modified.
    *   Object part: e.g. 'brain', 'head','image1'. When the object is a plane hosting a 2D image, the Object part should start with 'image', e.g. 'image1','image-mri'.
2.  Upload all the obj, mtl and image files to the object folder
3.  Follow the instruction in the code to include all the models

## How to use your custom pattern markers

1.  Follow the ReadMe document in the 'markers' folder to create your own marker(s)
2.  Upload the '*.patt' file(s) to some web server
3.  Follow the instruction in the code to include your own marker(s)

## Acknowledgements
This software is built using [AR.js](https://github.com/jeromeetienne/AR.js/blob/master/README.md) library.  
The human head MRI 3D model is built using the [sample data](http://slicer.kitware.com/midas3/download/?items=330421,1) in [3D Slicer](https://www.slicer.org).

## License
[![Creative Commons Licence](https://i.creativecommons.org/l/by-nc/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc/4.0/)  
This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).
