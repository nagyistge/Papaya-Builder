Papaya-Builder
==============

A tool to build and customize Papaya.  


How to build the build tool
-----
Run the Ant script, `build.xml`, found in the root of the project.  This will output `papaya-builder.jar` to the `build` 
folder.  Copy `papaya-builder.jar` to the `lib` folder in the [Papaya project](https://github.com/rii-mango/Papaya).

Usage
-----
```shell
usage: papaya-builder [options]
 -atlas <file>     add atlas
 -help             print this message
 -images <files>   images to include
 -local            build for local usage
 -root <dir>       papaya project directory
 -sample           include sample image
```

-atlas
-----
Atlas must follow the [FSL Atlas Specification](http://ric.uthscsa.edu/mango/imango_guide_atlas.html).  When building, 
provide the path to the atlas XML file.  Only non-probabilistic, label-based atlases are currently supported.  To use the 
default Talairach/MNI label atlas, leave the `<file>` field blank.

-local
-----
To build for local usage, include the `-local` flag.  In this case, image data is encoded and embedded within the 
JavaScript.

-images
-----
Specify one or more image file paths.  These images will appear as File menu options (similar to the sample image).

-root
-----
Point the builder to the root of the papaya folder.  Omiting this option will use the current working directory.

-sample
-----
Use this option to include a sample image.  An _Add Sample Image_ option will appear in the Papaya viewer File menu.
