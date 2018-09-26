---
layout: post
title: holding hands from 3000 miles away
description: computer aided design
<!-- img: /img/12.jpg -->
---
#### Background
In our first week, Neil introduced a variety of computer aided design (CAD) tools. Our assigment: "model (raster, vector, 2D, 3D, render, animate, simulate, ...) a possible final project". After lots of brainstorming*, I found one idea most compelling.

My boyfriend (Yanni) and I want to hold hands from across the country.

What could allow us to do that, allow us to feel like we are holding each other's hands, and actually convey our physical action? Can this happen at almost the same time?

#### Ideas
1) We each have molds of each other’s hands that are robotically controlled to mirror the activity of the other person.
2) We each have gloves that monitor our motion + simulate the feeling of the other person’s hand.
3) Use a leap motion to get the hand tracking data (How does this complicated with the introduction of the robotic hand into the view of the leap motion)

#### Design Considerations
- The hand should be warm and soft --> feel realistic
- The hand should have a very similar form as the hand being represented (The hand I hold should be about the same size as Yanni's hand).

#### Related Work
[OPENBIONICS](http://www.openbionics.org/) is an open-source initiative that focuses on the development of affordable, light-weight, modular, adaptive robot hands. The bio-inspired robotic hand they created uses acrylic for the body and silicon sheets for the flexure joints. [Roboticists at Cornell created a soft robot hand with touch sensitivity](https://www.recode.net/2016/12/18/14001048/robotic-hand-cornell-delicately-human-soft-robots). The soft robotic hand is hollow--they fill it with compressed air to give it its shape. It seems that it's an active area of research to robotic hands that can sense. Luckily, that's not what my project aims to do.

[Can we 3D print soft materials? (2015)](https://lewisgroup.seas.harvard.edu/files/lewisgroup/files/3d_printing_soft_materials_what_is_possible.pdf)

On GrabCAD, I found a bunch of hand models:
* [This one looks like it's from an old video game](https://grabcad.com/library/hand-53)
* [These look very realistic](https://grabcad.com/library/different-hands-1)
* [This is Adam's hand but idk who Adam is](https://grabcad.com/library/adam-s-hand-1)
* [Biomimetic hand--Terminator vibes](https://grabcad.com/library/biomimetic-hand-v2-1)

#### Potential Materials
Inspired by soft robots, I would like to mold some sort of flexible silicon to form the skin/body of the hand. However, the ability to lasercut hard materials and make them bend widens the possibilities.
I learned about shape memory alloy nitinol (nickel titanium alloy). Nitinol wire flexes when heated up/when enough current is run through it. Depending the material used to form the hand as well as how much wire I have, I might be able to use nitinol to actuate the fingers of the hand.
In order to support rotation, I will likely need another actuator.


#### *Brainstorming
* Some kind of interactive or functional art?
* physical blind accessible Tetris
* Modular/Compact Pampusan chair
* Hanging mobile (that does something extra idk)

Some inspirational themes/words:
* assistive technology
* accessible games
* light
* reflection
* geometry
* generative art

<!-- <div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/img/1.jpg" alt="" title="example image"/>
	<img class="col one" src="{{ site.baseurl }}/img/2.jpg" alt="" title="example image"/>
	<img class="col one" src="{{ site.baseurl }}/img/3.jpg" alt="" title="example image"/>
</div>
<div class="col one caption">
	Caption photos easily. On the left, a road goes through a tunnel.
</div>
<div class="col one caption">
	Caption photos easily.  Middle, leaves artistically fall in a hipster photoshoot.
</div>
<div class="col one caption">
	Caption photos easily.  Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/img/5.jpg" alt="" title="example image"/>
</div>
<div class="col three caption">
	This image can also have a caption. It's like magic.
</div>
 -->
