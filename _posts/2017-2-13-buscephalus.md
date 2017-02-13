---
layout:     post
title:      Bucephalus Bouncing Ball
summary:    The bouncing ball patch is a great example of how to make your modular synth do things that are not easily done with fixed architecture synths. It is the quintessential modulate the modulator patch.
comments: true
---
<img src="{{ site.baseurl }}/images/mod12.jpg" alt="mod" class="avatar" />

>Gravity and restitution acting against each other in a simulacrum of voltage and wire.

Model real world physics with patch cables and electricity! No actual balls required. What you do need are two attack-decay (AD) envelopes with attack and decay modulation available. One envelope for the pervasive hand of gravity, one for the "ball" acting against. A pair of VCAs or LPGs are also required. The gravity/contour envelope should be long, slightly exponential. Controlling the response of the contour envelope allows you to shape the gravity portion of the system. Push the envelope more towards an exponential response and you're on Jupiter.  Acting against this gravity is the linear bounce or restitution of the ball. This should be a tight linear envelope. Extend the decay parameter of the bounce envelope to make the ball bounce into infinity. 

Gravity and restitution acting against each other in a simulacrum of voltage and wire. Other modulations that you could apply at various points are not shown in the diagram below. Use your imagination! This patch is also described in the Make Noise Maths manual.[^1]  

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 graph TB
F(Trigger)-->C(Looping bounce envelope)
G(VCO out)-->|VCA/LPG in|D(Main out VCA)
F(Trigger)-->A(Contour envelope)
A(Contour envelope)-->|Decay/Fall modulation|C(Looping bounce envelope)
B(Mod VCA/LPG)-->|CV in|D(Main out VCA/LPG)
A(Contour envelope) -->|CV in|B(Mod VCA/LPG)
C(Looping bounce envelope)-->|VCA/LPG in|B(Mod VCA/LPG)
D(Main out VCA/LPG)-->J(Main out)
</div>
<sup><i>Bouncing ball patch</i></sup>

[^1]:[http://www.makenoisemusic.com/content/manuals/MATHSmanual2013.pdf](http://www.makenoisemusic.com/content/manuals/MATHSmanual2013.pdf)


  


