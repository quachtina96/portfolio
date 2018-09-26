---
layout: post
title: flowers and butterflies
description: computer controlled cutting
img: /img/week2/splash.jpg
---
### "design, lasercut, and document a parametric press-fit construction kit, accounting for the lasercutter kerf, which can be assembled in multiple ways"

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/week2-1.jpg" alt="" title="dodecahedron"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/week2-2.jpg" alt="" title="little shelves"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/week2-3.jpg" alt="" title="light cover"/>
</div>
<div class="col one caption">
	Final product!
</div>
<div class="col one caption">
	Another way to put the pieces together
</div>
<div class="col one caption">
	The underside for another perspective.
</div>

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/5.jpg" alt="" title="filler space"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/week2-5.jpg" alt="" title="star projector in action"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/5.jpg" alt="" title="filler space"/>

</div>
<div class="col three caption">
	Star projector in action!
</div>

I've got a rotating star/moon projector which makes for pretty rad, relaxing visuals... especially paired w/ [Sylvan Esso's "Uncantena"](https://www.youtube.com/watch?v=6yrGw0sRv3Q). Instead of just projecting stars and a moon--what if I could project branches, birds, or butterflies? Inspired by geometric construction kits and my love for lights and their projections, I decided to create a new projection dome.



#### design
I used Autodesk Fusion 360 to model the parts for the dome. I created an assembly, consisting of two components: pentagon and connector. Each component inclded a sketch that I then extruded.

In order to create the pentagonal faces, I set equality constraints on the dimensions of the edges of the face as well as the notches. Knowing that regular pentagons have 108 degree angles, I also constrained the design by requiring two of the angles be 10 degrees. I made this angle the a parameter that could be used by the connector as well. Once the sketch was done, I extruded the pentagon by the thickness of the cardboard (another parameter). Working with the assembly in mind, I sketched the connector directly onto a face of the pentagon's notch. In the third image below, you can see how the connector interfaces with the pentagonal face.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/sketch.jpg" alt="" title="CAD sketch of the pentagon face"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/pentagon_body.jpg" alt="" title="pentagon body extruded"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/model_connector.jpg" alt="" title="model of connector attached to pentagon face"/>
</div>
<div class="col one caption">
	Sketch of pentagonal face
</div>
<div class="col one caption">
	Extruded pentagonal face
</div>
<div class="col one caption">
	The connector interfaces with the pentagonal face.
</div>

My parametric design used the following parameters:
<img class="col three" src="{{ site.baseurl }}/img/week2/parameter.jpg" alt="" title="parameters used for the design"/>

Once I was satisfied with my design, I exported each component's sketch (<a href="{{ site.baseurl }}/img/week2/final_pentagon.dxf">pentagon</a>, <a href="{{ site.baseurl }}/img/week2/final_connector.dxf">connector</a> as a .dxf that I could then upload into CorelDraw in order to arrange the butterflies. The butterflies needed to be traced to form paths.

#### laser cut

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/lasercut2.jpg" alt="" title="the lasercut sheet"/>
	<img class="col two" src="{{ site.baseurl }}/img/week2/lasercut7.jpg" alt="" title="pieces popped out!"/>
</div>

Settings for the Epilog120: speed: 30, power: 80, frequency: 300

### "cut something on the vinylcutter"

This was my first time using a vinyl cutter ([Roland CAMM-1 GS-24](https://www.rolanddga.com/products/vinyl-cutters/camm-1-gs-24-desktop-vinyl-cutter))! I learned that the vinyl cutter works by moving a really small blade in one axis, and moving the sheet of vinyl in the other axis. By moving the sheet and the knife at the same time, the cutter is able to create smooth cuts.

__Process__
*Preparing the media*

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/none.jpg" alt="" title="blank filler"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/week2-0.jpg" alt="" title="original graphic"/>
</div>
<div class="col three caption">
	Birds of paradise are my favorite flower, so I found this graphic I adapted to create a laptop sticker.
</div>

* If the image is a rasteurized image, you can use CorelDraw (or Inkscape) to get the trace of the bitmap image. The result of the trace should be a set of paths that outline the different areas of the image. If you remove all color from the image, you can ensure that you only capture outlines of the black areas.
* From here (using CorelDraw) you can set the fill of the path to be no fill and the outline color to be black. At this point, you can clearly see the path the vinyl cutter will take.

*Setting up the vinylcutter*
* Get a sheet of vinyl. There is a lever in the upper left hand corner of the vinyl cutter. Push it back to move the wheels up so that you can slide the sheet of vinyl into the cutter. You want to move the wheels so that the ends of the sheet line up with the wheels and so that the sheet is about half way in. This will help the vinylcutter when it's measuring the dimensions of the space it can use for your cut. Pull the lever back towards you to hold the sheet in place.
* Now, you can go to the buttons on the cutter and select "Piece". Upon pressing "enter", the vinyl cutter will measure and display the dimensions of the area.
* Enter this area into CorelDraw so you can size and layout your cut.
* Preview your print, check/set settings (: cutting speed=20cm/s | force=80gf), and send it to the printer!


*Transferring the vinyl.
I want a bunch of disjoint pieces of vinyl to stay in the same orientation when I stuck it to my laptop. Here's how I did it.
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week2/peel.jpg" alt="" title="peeling the vinyl"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/contact.jpg" alt="" title="using contact paper"/>
	<img class="col one" src="{{ site.baseurl }}/img/week2/laptop_sticker.jpg" alt="" title="result of transfer to laptop"/>
</div>
<div class="col one caption">
	Remove the vinyl you don't want to transfer.
</div>
<div class="col one caption">
	Press contact paper firmly onto the vinyl you want to transfer. It helps to apply a lot of pressure to make sure the contact paper picks it up.
</div>
<div class="col one caption">
	Press the vinyl to the desired location firmly, ensuring that the vinyl sticks to the surface instead of getting pulled up by the contact paper. You can reduce the chance of pulling off the vinyl by pulling in the same plane as the surface you're sticking too instead of perpendicular.
</div>

