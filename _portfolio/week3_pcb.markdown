---
layout: post
title: avr isp programmer board
description: electronics production
img: /img/week3/pcb.jpg
---

This week, we learned how to mill a trace and solder the appropriate components given the layout. We each applied these skills to create a AVR ISP Programmer board. Upon the class staff's recommendation, I followed [Brian's awesome documentation](http://fab.cba.mit.edu/classes/863.16/doc/projects/ftsmin/index.html) which contain the files for milling and the schematic and layout for soldering.

Tools:
* Roland MDX-20 Mill
* Double-sided tape
* Sacrifical board
* Isopropanol (for cleaning off our oils that oxidize the copper)

Materials:
* 1x Milled board
* 1x ATtiny45 or ATtiny85
* 2x 1kΩ resistors
* 2x 499Ω resistors
* 2x 49Ω resistors
* 2x 3.3v zener diodes
* 1x red LED
* 1x green LED
* 1x 100nF capacitor
* 1x 2x3 pin header

#### Milling
We used the Roland MDX-20 with a 1/64" endmill to mill the trace and a 1/32" endmill to mill the board. Our adventure began with training from Tomas and was continued with a group of us (Nicole, Oceane, Ravi, Caro, Erik and me) characterizing the 1/64" endmill.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week3/teamwork.jpg" alt="" title="nicole and ravi working together to change endmill"/>
	<img class="col one" src="{{ site.baseurl }}/img/week3/mods_software.jpg" alt="" title="software for configuring and sending mill job"/>
	<img class="col one" src="{{ site.baseurl }}/img/week3/mill.jpg" alt="" title="mill working"/>
</div>
<div class="col one caption">
	Inserting a 1/64" endmill tip to do the trace.
</div>
<div class="col one caption">
	Using the mods.cba.mit.edu software to configure and send a job to the mill.
</div>
<div class="col one caption">
	The mill doing its thing!
</div>


<div class="img_row">
	<img class="col two" src="{{ site.baseurl }}/img/week3/endmill_fail.jpg" alt="" title="first attempt at characterizing the endmill"/>
	<img class="col one" src="{{ site.baseurl }}/img/week3/group_test.jpg" alt="" title="successful characterization of endmill"/>
</div>
<div class="col three caption">
	ON THE LEFT:
	Our first attempt: fail. Possible reasons: the board or the sacrificial layer was not flat. The head of the mill wasn't low enough. The endmill wasn't tightened such that it was touching the board.
	ON THE RIGHT:
	After making sure the endmill was touching the board, success!
</div>

<div>
<img class="col three" src="{{ site.baseurl }}/img/week3/fts_mini_traces.png" alt="" title="the traces"/>
<img class="col three" src="{{ site.baseurl }}/img/week3/fts_mini_cut.png" alt="" title="the board outline"/>
</div>


__Setup__
1. Double-sided tape a sacrificial layer flat onto the bottom of the mill
2. Double-sided tape the sheet you will mill onto the sacrificial layer.

__Setting up the Mill__
1. Turn off "view" mode.
2. Make sure you put in the proper endmill. Be careful not to let the endmill drop and break. The tip of the endmill needs to touch the material (which should be lying flat)
3. Lower the head of the machine such that it has the range of motion to cut as deep as is needed (the max depth parameter passed to the machine).
4. Once the bit has been loaded and the z-axis has been manually set, we can move to the software.

It's important to mill the traces before the outline because milling the outline could result in a loose part that could then wreck the sacrifical layer.

__Using the Mill__
1. Upload the traces file
2. Set the x,y origin from which to start the job. The x,y coordinate is deterministic and consistent per use of the machine.
3. Calculate the toolpath given the settings (below).
4. Ensure that there is a serial connection between the computer and the mill (so that the job information can be sent).
5. Send the job over!

__Mill Traces Settings__

* tool diameter (in): 0.0156 = 1/64"
* cut depth (in): 0.004
* max depth (in): 0.004
* offset number: 4

Note: the offset number corresponds to how many passes are made to increase the width of the trace.

__Mill Outline Settings__

* tool diameter (in): 0.0312 = 1/32"
* cut depth (in): 0.024
* max depth (in): 0.072
* offset number: 1

Note: Since the max depth is 3 times the assigned cut depth, the mill will make 3 passes going .024 inches deep with each cut. This exists to prevent the endmill from breaking. The offset number is 1 because we only want to basically cut the pcb out from the plate. The cut doesn't need to be wide.

#### Soldering
This was my first time soldering, and I didn't realize how hard it was! Tomas (one of our TA's) made it look so easy!

Anyway, I basically followed Brian's advice and referenced the schematic and layout:
<img class="col three" src="{{ site.baseurl }}/img/week3/pcb_full.png" alt="" title="using contact paper"/>
<img class="col three" src="{{ site.baseurl }}/img/week3/schematic.png" alt="" title="peeling the vinyl"/>

The layout tells you where to particular components go. The schematic is tells you information about the parts of the circuit and you can use it to figure out what it does.

Some things I learned:
* **Let the solder flow.** In the beginning, the solder would ball up and become a big glob and when I saw that happen I'd immediate move it away from the board instead of letting it flow.
* **Clean the solder tip.** It reduces the likelihood of globbing.
* **Keep the board steady** It's hard to keep the board steady when both of your hands are in use. I used doublesided tape to keep the board in place, but I later learned there's a clip to hold the board down.

Here's the final result!
<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/img/week3/pcb.jpg" alt="" title="final pcb"/>
</div>
<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/week3/pcb_zoom1.jpg" alt="" title="zoomed in view of pcb"/>
	<img class="col one" src="{{ site.baseurl }}/img/week3/pcb_zoom3.jpg" alt="" title="second zoomed in view of pcb"/>
	<img class="col one" src="{{ site.baseurl }}/img/week3/pcb_zoom2.jpg" alt="" title="third zoomed in view of pcb"/>
</div>

