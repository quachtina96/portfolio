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

#### "3D scan an object (and optionally print it)"
TODO
