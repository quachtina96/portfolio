---
layout: post
title: klein bottle + my hand
description: 3D scanning and printing
img: ../img/week4/focus_splash.jpg
---
#### "design and 3D print an object (small, few cm) that could not be made subtractively"
[A Klein bottle](https://en.wikipedia.org/wiki/Klein_bottle)

To design my Klein bottle, I used Autodesk Fusion 360 (which runs on MacOS unlike Solidworks...). I aimed to follow a [~5 min tutorial that used Solidworks to design the Klein bottle](https://www.youtube.com/watch?v=MpfFYe0OGg4). It's pretty crazy that this person was able to design the bottle in 5 minutes... It took me on the order of hours as I learned how to do certain operations in Fusion 360. ANYWAY! HUGE thanks to Ben Gray for taking his experience using Solidworks and translating it to Fusion 360 to help me!

__Process__
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/1_sketch.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/2_revolve.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/3_sketch_spline_arc.jpg" alt="" title=""/>
</div>
<div class="col one caption">
	Sketch half of the wide part of the bottle.
</div>
<div class="col one caption">
	Revolve this sketch to form the bottle body.
</div>
<div class="col one caption">
	Create another sketch containing a path. Construct this path with a spline and an semicircle arc, tangent to each other.
</div>
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/4_plane.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/5_circle_on_plane.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/6_sweep.jpg" alt="" title=""/>
</div>
<div class="col one caption">
	Create a plane that is parallel to the top of the bottle body.
</div>
<div class="col one caption">
	Draw a circle on the plane. This circle will provide the profile for the sweep.
</div>
<div class="col one caption">
	Now, sweep the circular profile along the path (made of the spline + arc).
</div>
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/7_surface_loft_bottom.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/8_surace_loft_top.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/9_solid_sectional_analysis_xy.jpg" alt="" title=""/>
</div>
<div class="col one caption">
	Create a surface loft from the bottom of the bottle body to the bottom end of the sweep.
</div>
<div class="col one caption">
	Create a surface loft from the top of the bottle body to the top end of the sweep.
</div>
<div class="col one caption">
	At this point, all of the bodies (3D objects) we've created are solid. We don't want that.
</div>
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/10_shell.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/11_sweep_cut.jpg" alt="" title=""/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/12_surface_loft_cut.jpg" alt="" title=""/>
</div>
<div class="col one caption">
	Shell the klein bottle using a 1mm thickness for the wall At this point, you can see that there still exists a 1mm wall at the bottom of the bottle and at the bottles intersection into itself.</div>
<div class="col one caption">
	To get rid of the wall at the intersection, we cut with another sweep of a circular profile along the same path. The circle forming the profile for this sweep needs a radius of 1mm less than the original.
</div>
<div class="col one caption">
	Finally, to get rid of the bottom wall, we create a surface loft that will cut the bottom away. To achieve the smooth curve, you must define the appropriate circle on the bottom surface.
</div>

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/final_1.jpg" alt="" title="front view of klein bottle"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/final_2.jpg" alt="" title="bottom view of klein bottle"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/splash.jpg" alt="" title="klein bottle modeled as made of blue glass"/>
</div>
<div class="col one caption">
	Front view of klein bottle
</div>
<div class="col one caption">
	Bottom view of klein bottle so you can see the hole in the bottom.
</div>
<div class="col one caption">.
	Klein bottle visualized as made of blue glass.
</div>

From Autodesk Fusion, you can export your model to an STL file via the File > 3D Print option. I didn't realize that at first, so I exported a STEP file and an IGES. Tom ended up converting the STEP file to an STL in Rhino, and based on the 3D print, there might have been an artifact of the conversion resulting in a shape my friend Karishma calls "a 9 on a Hershey's kiss"

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/13_prusa.jpg" alt="" title="grey hollow, 3d-printed klein bottle"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/power_wash.jpg" alt="" title="TODO: include image of the bottle after removing supports"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/14_dimension_support.jpg" alt="" title="white 3d-printed klein bottle with supports inside"/>
</div>
<div class="col one caption">
	PLA material printed with the Prusa MK3 without support material on the inside.
</div>
<div class="col one caption">
</div>
<div class="col one caption">
	ABS material printed With the Stratysys Dimension with supports on the inside. These supports are made with a water soluble material that gets removed by letting the bottle sit in a heated bath containing water and lye (basically a really strong soap) that is ultrasonically agitated. Since there isn't room for hte supports to escape, it not really sure what will happen there.
</div>

Since the prints didn't come out as expected, Tom said I could try reprinting it with the Prusa.

Settings:
* Materials: Prusa PLA
* Quality: Detail 0.1mm
* Infill: Hollow/Shell - 0%
* Support: Only from build plate
(Trying to print it without support resulted in it coming off the plate because there's only a thin circle actually holding it to the plate.)

#### "3D scan an object (and optionally print it)"
Since I want to have a model of my hand for my final project, I tried using the Sense2 3D Scanner to scan my hand. I knew it was going to be hard to keep an even distance between the sensor and my hand on my own, so I asked John to help me out! It was pretty funny and involved teamwork as we took turns holding the scanner steady as John moved to my other side. We made two attempts (One in 'Scan Object' mode and one in 'Scan Head' mode) and got about the same results.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/15_sense2_hand.jpg" alt="" title="Front view of right hand scan"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/16_sense2_hand_side.jpg" alt="" title="Side view of right hand scan"/>
	<img class="col one" src="{{ site.baseurl }}/img/week4/17_sense2_hand_solidify.jpg" alt="" title="Solified hand scan"/>
</div>
<div class="col one caption">
	Front view of right hand scan
</div>
<div class="col one caption">
	Side view of right hand scan
</div>
<div class="col one caption">
	You use the software to solify the scan in order to get an STL that you can actually print using the 3D printer.
</div>

I tried to use the erase tool to clean up the hand, but when I went to solidify the hand after erasing, it undid my hard work so I decided to try scanning my head (again with Tom's help). So that was kind of a fail.

Scanning my head was also pretty difficult, because as the scan is occuring, you often need to move the scanner very slowly and stay very still. It's hard to do that and ensure that the scanner still knows how to combine the information in a way that makes sense. Once the scanner loses its tracking of the object its scanning (caused by quick movements, changes in proximity, or other objects getting in the way), it's difficult to find again. Here's the result.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week4/20_sense2_head_scan.jpg" alt="" title="Scan of tina's head"/>
	<video class="col two video" controls>
	  <source src="{{ site.baseurl }}/img/week4/0_sense2_head2.mp4" type="video/mp4">
	</video>
</div>
<div class="col one caption">
	Scan of my head using Sense2 scanner.
</div>
<div class="col two caption">
	I figured I'd settle for a mount rushmore kind of aesthetic.
</div>

<!-- #### "Characterize the 3D printer"
Another printer made available to the class is the Sindoh 3DWox. Nicole and I printed a testfile to the Sindoh 3DWox to characterize it. Using this print given to us, we
 -->


