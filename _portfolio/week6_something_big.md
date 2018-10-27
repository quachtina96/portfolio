---
layout: post
title: music shrine
description: computer-controlled machining
img: ../img/week6/digital_design/final.jpg
---
<!-- #### "test runout, alignment, speeds, feeds, and toolpaths for your machine"
For the group assignment, we were supposed to teest the runout, alignment, and toolpaths for my machine.  -->
#### "make something big"

__idea__

Initially, I wanted to make a loft for my friend Josh. But I realized that the project wasn't really fit for taking advantage of the ShopBot we were using, so I asked him what else he would appreciate for improving his room. The most exciting idea was the idea of making a piece of furniture that would highlight music as important to him--a kind of "music shrine".

Josh plays both electric bass guitar and trumpet, but I actually didn't know he played trumpet until recently. I have only ever seen him play guitar. He's more inclined to play bass because his guitars are easy to access. But if his trumpet & accessories for it were as convenient, he'd probably play it more.

Josh also has records, music books, and is planning to get a turn table for playing records.

He also has a pretty big part of his room that he could dedicate to music. Space we got excited about filling before realizing our material size: <a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_1_osb.jpg">4' x 8' sheet of OSB (Oriented Strand Board)</a>

My initial design, filling the 29" by 53" by 37" volume in Josh's room, involved extra table space and another bin more holding more records. I scaled down the design to support the essentials:

* record player (turntable)
* records
* music books
* trumpet
* trumpet mutes

<img  class="col three" src="{{ site.baseurl }}/img/week6/digital_design/final.jpg" alt="" title="music shrine visualized in fusion 360"/>
<div class="col three caption">
	music shrine visualized in fusion 360
</div>

__process__

**Software Tools**
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview) for CAD
* [CorelDRAW](https://www.coreldraw.com/en/) for laying out vectors
* [VCarvePro](https://www.vectric.com/products/vcarve.htm) for laying out vectors + post processing (adding tabs + dogbones/tbones)
* [ShopBot3](http://www.shopbottools.com/mSupport/controlsoftware.htm) for interfacing with machine and actually running the job.

**Hardware Tools**:
* [Full Size ShopBot](http://www.shopbottools.com/mProducts/prSalpha.htm)
* Power drill
* ~10 Screws + drillbit corresponding to screw thread size
* 1/4" downcut endmill

**Materials**:
* 4' x 8' sheet of [OSB](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Oriented_strand_board_at_Courtab%C5%93uf_2011.jpg/1200px-Oriented_strand_board_at_Courtab%C5%93uf_2011.jpg)


**Design**:

Based on our ideas, we sketched out some possiblities.

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/design/design_1.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/design/design_1.jpg" alt="" title="initial sketch"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/design/design_2.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/design/design_2.jpg" alt="" title="detailed sketch"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/design/design_3.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/design/design_3.jpg" alt="" title="exploring mechanism"/>
	</a>
</div>
<div class="col one caption">
	initial sketch
</div>
<div class="col one caption">
	detailed sketch
</div>
<div class="col one caption">
	exploring mechanism
</div>

In Autodesk Fusion 360, I used the following workflow for prototyping and designing.

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/digital_design/param.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/digital_design/param.jpg" alt="" title="screenshot of parameters in fusion 360"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/digital_design/reference_area.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/digital_design/reference_area.jpg" alt="" title="construction lines defining top and back reference areas"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/digital_design/topview_planning.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/digital_design/topview_planning.jpg" alt="" title="topview dividing up the bottom reference area"/>
	</a>
</div>
<div class="col one caption">
	1) define and get the values for parameters.
</div>
<div class="col one caption">
	2) create (bottom and back) reference sketches that contain construction lines for the volume the project can take
</div>
<div class="col one caption">
	3) create a sketch that divides the bottom area into the various components.
</div>

<div class="img_row">
	<img class="col two" src="{{ site.baseurl }}/img/week6/digital_design/turntable_holder.jpg" alt="" title="initial sketch"/>
	<img class="col one" src="{{ site.baseurl }}/img/week6/digital_design/topview_planning.jpg" alt="" title="exploring mechanism"/>
</div>
<div class="col one caption">
	4) pick a part of the furniture to make (e.g. the box holding the turntable or the shelf for books) & create an offset plane for that part of the furniture so that it can be at the proper height when you (next step) create a sketch of the profile of the part on that plane.
</div>
<div class="col one caption">
	5) extrude to the thickness of the material (keeping in mind that it's a defined parameter and you need to be careful that you extrude in the right direction based on the arrows OR the preview of the extrusion).
</div>
<div class="col one caption">
	6) In Fusion 360, extrusions can involve different actions like "New Body", "Join", "Cut", "Intersect". I mainly created new bodies, but found it useful to cut into specific bodies when trying to create slots that would fit into each other (for assembly).
</div>

As I added different components, I would use the faces of existing bodies to define the planes, since I wanted parts to be touching each other as the parts were being assembled.

I didn't have in mind that all the faces that were in the same plane could be cut as a single piece until I had a solid vision/model for how the pieces would end up fitting together. Once the pieces were all together, I selected the appropriate bodies to 'combine'.

Before exporting .dxf files for each of the faces I wanted to cut, I wanted to make sure the pieces would fit together in real life. At this point, the design (and sketches) were complex enough that I couldn't actually visually verify that there weren't interferences... luckily, Autodesk fusion has a tool for that!

<a href="{{ site.baseurl }}/img/week6/digital_design/interference.jpg">
<img  class="col three" src="{{ site.baseurl }}/img/week6/digital_design/interference.jpg" alt="" title="screenshot of interferences in fusion 360"/>
</a>
<div class="col three caption">
	You can see that there were many interferences detected when all bodies (including some that I ended up removing from my project) were selected.
</div>

To resolve the interferences, I went through and used Autodesk's highlighting to determine which pairs of bodies were contributing to what interferences. From there, I investigated the interference to come up w/ a plan.
1. remove bodies that I don't want nor care about
Then, for each interference...
2. pick one of the two bodies that needs to be cut away
3. create a sketch on the face of the body i want to keep
4. extrude that sketch as a cut into the body to cut away; this actually cuts away the body you wanted to keep SO!
5. extrude using the same sketch, this time creating a new body.

To obtain the dxfs, I right clicked on each body and created a sketch from that body. This made clean sketches that didn't include the construction lines I had used.

DXF Files:

_individual parts_

* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/back.dxf">back.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/book_shelf.dxf">book_shelf.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/far_right.dxf">far_right.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/mutes_shelf.dxf">mutes_shelf.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/record_bottom.dxf">record_bottom.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/record_front.dxf">record_front.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/shelf_left.dxf">shelf_left.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/shelf_right.dxf">shelf_right.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/turntable_bottom.dxf">turntable_bottom.dxf</a>
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/turntable_front.dxf">turntable_front.dxf</a>

_most parts laid out_
* <a href="{{ site.baseurl }}/img/week6/digital_design/dxf/tina_music_shrine.dxf">tina_music_shrine.dxf</a>


**Make!**

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_2_vcarve.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_2_vcarve.jpg" alt="" title="parts laid out on VCarvePro"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_2_5.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_2_5.jpg" alt="" title="shopbot"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_3_vac.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_3_vac.jpg" alt="" title="shopbot vac"/>
	</a>
</div>
<div class="col one caption">
	upload dxfs into VCarvePro and lay them out.
</div>
<div class="col one caption">
	check out the shopbot with its nice sacrificial layer
</div>
<div class="col one caption">
	the big vacuum keeps the job safe and clean as the shopbot may make multiple passes along the same cut t safely achieve greater depth.
</div>

Setting up the ShopBot:
* lay the material down on the sacrificial layer (after checking that that sacrificial layer isn't too beat up)
* drill holes only into the material to make some holes before fixturing the material to the sacrificial layer
* moving from one long end to the other, fixture the material by drilling, making sure to press the material flat.
* pick the desired cutter/endmill
* insert it into the Shopbot by using the two wrenches to loosen the collet
* inserting the endmill into the collet, verifying that as much of the endmill is in the collet such that no part of the cutter/blade is inside the collet. This is the safest orientation because the cutter being in the collet could damage the machine, yet having it stick out too far will result in a less stable cut and probably greater runout.
* hand screw the collet in first and then tighten with the two wrenches.
* add the brushes.

VCarvePro settings (useful for post processing, like adding bones & tabs):
* Job Size: 96"x48"
* Material: Zero on top of the material
* Pick origin to be bottom left corner
* Make sure offset of origin is 0.
* upload your DXF file(s)
* _Edit > Join Vectors_ to make sure that all shapes are closed so that various operations will work
* Default Tolerance: .1 in
* leave edge/margin of about 2 inches to leave room for the screws that will fixture the board down.
* You want to make sure there's enough spacing ~1.5-2 inches between each part
* For press fits, you want to add T or dog bones to the corners of inner slots so because the mill (by its circular design) cannot fit into corners.


For my job, I only needed to set up a Profile Toolpath, but if you would like for the Shopbot's cut to fill an area and not go all the way through, a pocket toolpath is needed.

VCarvePro Profile Toolpath settings:
* We set the max depth of the cut to be .52 inches so that it would cut all the way through the material and cut a little bit into the sacrificial laer.
* max path depth should be around .25 inches. We made it .26 inches so we could make 2 passes for a total cut of .52 inches.
* pass depth: size of each bite into the material
* stepover: 95% (is a big stepover, one that allows the job to go faster)
* feeds & speeds
	* spindle speed: 10000 rpm
	* feed rate: 120 in/min
	* plunge rate: 60 in/min (movement in the z axis)
* tool # is only applicable for machines with multiple tool heads.
* add tabs. tabs will stabilize your cut by maintaining an attachment to the rest of the materials. you want your tab to be thick enough to stay strong but thin enough to easily remove or break as you're removing your part. you can set the number of tabs and click away any tabs you don't want.
* add bones (T or dog).

Note:
* .15 in cut depth for the pocket is pretty good
* the toolpath order must specify that the pocket cut is done before the profile cut (so that the piece is not loose or detached from the board)

Once your toolpath(s) are ready, you can export them using two steps.
1. In the Toolpath panel, check the bottom of the panel to verify that you are exported only the toolpaths you desire. Click export toolpaths to generate a sbp file. this sbp file will be provided to ShopBot.
2. To save the work you did in VCarvePro, go to File > Save as... and save a .crv file, which should keep the settings.

Using the ShopBot (specific to the MIT Center for Bits and Atoms Shop setup):
* At the control panel, the red knob should be set to on
* use the key to activate the spindle and check that the spindle speed is 10000 rpm
* if necessary, reset the shopbot w/ the physical blue button.
* Open up the ShopBot3 software
* click on the yellow button to begin zero-ing the x and y axes.
	* PAGE UP to move endmill up in the z direction (preven it from hitting the material)
	* Use up/left/down/right arrow keys to position the endmill over the origin (set by you)
	* Use the Zero options at the top to set the X & Y.
* click on Cuts > C2 - Zero Z-axis w/ Zzero Plate & follow instructions
* Upload sbp file (& ignore popup)
* Use the physical green button to turn on the spindle
* Put hand over the red emergency stop button
* Make sure you know where the endmill should start its job and be ready to stop the job if anything looks or sounds wrong.
* Start the job :)

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_4_cut.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_4_cut.jpg" alt="" title="parts laid out on VCarvePro"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_5_troubleshoot.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_5_troubleshoot.jpg" alt="" title="shopbot"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/shopbot/shopbot_6.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/shopbot/shopbot_6.jpg" alt="" title="shopbot vac"/>
	</a>
</div>
<div class="col one caption">
	The shopbot was working pretty smoothly, until...suddenly it wasn't.
</div>
<div class="col one caption">
	an error message popped up... saying that the computer lost connection to the ShopBot and to check loose connections.
</div>
<div class="col one caption">
	when the machine was stopped, we removed the piece that had already been cut since it was no longer lying perfectly flat and could get in the way of the endmill.
</div>

It wasn't until a few days later as I was assembling my piece of furniture that I realized that I didn't cut out 2 parts of the furniture!

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_0_0065.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_0_0065.jpg" alt="" title="tina puts pieces together"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_2_0069.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_2_0069.jpg" alt="" title="tina presents what she has so far"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_3_2591.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_3_2591.jpg" alt="" title="trumpet mutes sitting in their holder"/>
	</a>
</div>
<div class="img_row">
<div class="col one caption">
Assembly excitement! The slot size I used was 7/16" (0.4375 in) and the measured thickness of the OSB was slightly less (0.417 in.) so the pieces fit in loosely but still securely.
</div>
<div class="col one caption">
all the pieces that I had so far, put together. I liked how the bottom of the record play and the bottom of the bookshelf fit together nicely and looked like they would properly sandwich the middle shelf. :)
</div>
<div class="col one caption">
The trumpet mutes also fit in quite nicely, although I would like to have them a little further out so that they are even easier to access.
</div>
</div>

I came in a few days later to cut the 2 missing parts and recut the trumpet mute holder. It was during this session with Tom and the Shopbot that I learned that it's important to have dogbones on not just the inside slots, but the outside ones. This caused me a lot of trouble as I was assembling the furniture and it wouldn't fit together as tightly as needed--leading the entire structure to be less stable. I compensated for this with a hammer and chisel, but in the cases where I overcompensated, the pieces only loosely fit together.

<div class="img_row">
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_4_on_floor.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_4_on_floor.jpg" alt="" title="Putting the pieces together in the hallway"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_5_josh_plays.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_5_josh_plays.jpg" alt="" title="Josh demonstrates musicality by emotionally supporting me"/>
	</a>
	<a href="{{ site.baseurl }}/img/week6/assembly/assembly_6_incontext.jpg">
		<img class="col one" src="{{ site.baseurl }}/img/week6/assembly/assembly_6_incontext.jpg" alt="" title="the music shrine is chillin'"/>
	</a>
</div>
<div style="height:100px">
<div class="col one caption">
Putting the pieces together in the hallway!
</div>
<div class="col one caption">
Josh demonstrates musicality by emotionally supporting me
</div>
<div class="col one caption">
the music shrine is chillin'
</div>
</div>


#### lessons learned + things i'd do differently
- test the robust-ness of your parametric design as you go along--while you're stil able to make changes and havent dug yourself deep.
- Using VCarvePro, I ran into trouble adding T-bones for my inner slots. To address this, I ended up manually adding the bones by drawing circles and using <a href="https://docs.vectric.com/docs/V9.0/VCarvePro/ENU/Help/Drawing/Object%20Merging.html">Object Merge tools under Edit Objects, specifically the Weld Vectors tool.</a>
- Using the ShopBot, the computer lost connection to the Shopbot 3 times during my ~37000 line job. In order to reconnect and start the job where you left off (saving time), you should take the following steps.
	1. write down the x and y location that the machine stopped at.
	2. write down the instruction (line number) that the machine stopped at.
	3. close the shopbot software and reopen it.
	4. click the yellow button to open the panel to manually move the shopbot.
	5. use the PAGE UP arrow key to lift the endmill in the axis before adjusting x and y (to match what you wrote down in step 1)
	6. upload the .spb part file to the shopbot software, but select the goto/line option.
	7. press the digital start button.
	8. in the modal, select the 'goto' option and then type in the line number from step 2.
	9. press 'go' so that the program jumps to that line.
	10. press the button to actually send the job to the shopbot.
	11. press the physical start button to start the spindle.
	12. press enter/start on the digital shopbot interface to start the job.

