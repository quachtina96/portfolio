---
layout: post
title: not just goop
description: molding and casting
<!-- img: ../img/week7/attiny44A_pinout.jpg -->
---
# "design a 3D mold around the stock and tooling that you'll be using, mill it, and use it to cast parts"


**Materials**
* plastic cups
* wooden tongue depressors
* Oomoo
* Drystone
* cardboard
* [gaffer tape](https://www.amazon.com/Impact-Gaffer-4-Pack-Yellow-Orange/dp/B01NC3HPN4)

**Tools**
* Shopbot Desktop
* hot glue gun
* xacto knife
* straight edge

**Software**
* Inkscape - to trace image --> path
* Fusion360 - to create 3d model
* Image2Surface Fusion 360 Add-in - to convert greyscale image to 3d surface
* ShopBot Partworks3D - to generate roughing and finishing toolpaths
* ShopBot 3 - to control the Shopbot Desktop

**process**

I tried many different things in approaching this project...

* casting a model of a functioning toilet
	* GrabCAD didn't have a model, and I didn't have time to make one...
* casting a model of a succulent. a few years ago, i used the lost wax casting method to create a succulent.
	* I found a stl file I could use, but it would have been difficult to handle the undercuts.
* turning an image of me, my sister, and my grandma into a surface to mill and cast
	* First, I turned the color photo into greyscale via ImageMagick
	* Then,I used the Image2Surface Add-in for Autodesk Fusion 360
	* I realized that the surface wasn't actually a great translation
* converting "what a strange feeling" (drawing I found on tumblr 7 years ago and have loved since) into a surface
	* Instead of translating a regular photo, I thought a drawing, or something that was just black or white would work well...
	* I was wrong...
* use "what a strange feeling" to generate a path that i can extrude in Autodesk Fusion 360
	* Inkscape had no problem generating the path, however Fusion 360 really struggled to handle the sketch, and crashed a lot
* extruding a less complex drawing from Tumblr which I call "swim time"
	* this was still a struggle because of the complexity of the path. I tried to use Inkscape's simplify path tool to make the svg easier to use in Fusion 360. this made it confusing to extrude the appropriate faces, so I went with the original unsimplified path and was very patient with each step.

#### making
I settled on the extrusion of swim time with the idea that I'd cast in drystone, and then color the concrete with paint or marker and then pour epoxy to create an art piece.

__mill the positive out of the machineable wax__

0. change the endmill in the shopbot if it isn't the correct one. for the purpose of this class, most of us are working with 1/8th inch ball or flat end mills. Since my design has such intricate detail, Tom helped me use the 1/16th flat endmill.
1. get block of machineable wax and fixture it (using hot glue gun) to something (like OSB) that can be screwed into the sacrifical layer on the shopbot desktop
2. zero the x & y and then the z (using the plate), following a similar process as we used in the "make something big" week.
3. upload the roughing part file.
4. start the job!
5. upload the finish part file
6. start the job!
7. unfixture the osb from the sacrificial layer
8. vacuum the wax shavings. Neil mentioned that if you're really clean, you can save the shavings, melt, and reuse the wax for future work.

__cast a soft negative out of oomoo using the machineable wax__

After milling the positive, i used cardboard, gaffer tape + xacto knife to create walls for my pour of oomoo.
Oomoo is pretty easy to work with, only consisting of two parts that mix at a 1:1 ratio by volume. One approach I tried to use when pouring was using a "ribbon pour" in which the thin layer breaks bubbles as it comes out of the cup and into the mold. The curing time for oomoo is around 75 minutes... just over an hour.

__cast a rigid negative out of drystone using the soft oomoo mold__

<!--
<video controls loop>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
 -->