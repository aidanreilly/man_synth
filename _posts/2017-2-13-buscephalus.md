---
layout:     post
title:      Bucephalus Bouncing Ball
summary:    The bouncing ball patch is a great example of how to make your modular synth do things that are not easily done with fixed architecture synths. It is the quintessential modulate the modulator patch.
comments: true
---
<img src="{{ site.baseurl }}/images/mod12.jpg" alt="mod" class="avatar" />

>A simulacrum of voltage and wire.

Tic      tic    tic   tic  tic tictictic. The bouncing ball patch. Model real world physics with patch cables and electricity! No actual balls required. It does require two attack-decay (AD) envelopes with attack and decay modulation available. One envelope for the pervasive hand of gravity, one for the "ball" acting against. A pair of VCAs or LPGs are also required. The gravity envelope should be long, slightly exponential. Controlling the response of the gravity envelope allows you to shape the gravity portion of the system. Extend the decay parameter to make the ball bounce into infinity. Acting against this gravity is the linear bounce or restitution of the ball. This should be a tight linear envelope.

There you have it. Gravity and restitution acting against each other in a simulacrum of voltage and wire. Other modulations that you could apply at various points are not shown in the diagram below. Use your imagination! This patch is also described in the Make Noise Maths manual.[^1]  

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid" align="center">
 graph TB
F(Trigger)-->C(Looping bounce envelope)
G(VCO out)-->|VCA/LPG in|D(Main out VCA)
F(Trigger)-->A(Gravity envelope)
A(Gravity envelope)-->|Decay/Fall modulation|C(Looping bounce envelope)
B(Mod VCA/LPG)-->|CV in|D(Main out VCA/LPG)
A(Gravity envelope) -->|CV in|B(Mod VCA/LPG)
C(Looping bounce envelope)-->|VCA/LPG in|B(Mod VCA/LPG)
D(Main out VCA/LPG)-->J(Main out)
</div>
<sup><i>Bouncing ball patch</i></sup>

Here is an example of what the patch can sound like:

<iframe width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/307778865&amp;color=ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;show_artwork=false"></iframe>

[^1]:[http://www.makenoisemusic.com/content/manuals/MATHSmanual2013.pdf](http://www.makenoisemusic.com/content/manuals/MATHSmanual2013.pdf)


  


