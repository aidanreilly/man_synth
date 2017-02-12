---
layout:     post
title:      Bucephalus Bouncing Ball
summary:    The bouncing ball patch is a great example of how to make your modular synth do things that are not easily done with fixed architecture synths. It is the quintessential modulate the modulator patch.
comments: true
---
<img src="{{ site.baseurl }}/images/mod12.jpg" alt="mod" class="avatar" />

>Gravity. Restitution. 

You'll need two envelopes with modulation available for attack and decay portions of the envelopes. One envelope for the pervasive hand of gravity, one for the "ball" acting against. The gravity/contour envelope should be long, slightly logarithmic. Controlling the response of the contour envelope allows you to shape the gravity portion of the system. Push the envelope towards exponential and you're on Jupiter. 

Acting against gravity is the bounce or restitution of the ball. Extend the decay parameter of the bounce envelope to make the ball bounce into infinity.  

Gravity. Restitution. Acting against each other in a simulacrum of voltage and wire. Simple patch is diagram below. Other modulation that you could apply at various points not shown. Use your imagination. 

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 graph TB
F(Trigger)-->C(Looping bounce envelope)
F(Trigger)-->A(Contour envelope)
B(Mod VCA)-->|CV in|D(Main out VCA)
A(Contour envelope) -->|CV in|B(Mod VCA)
C(Looping bounce envelope)-->|VCA in|B(Mod VCA)
G(VCO out)-->|VCA in|D(Main out VCA)
D(Main out VCA)-->J(Main out)
</div>
<sup><i>Bouncing ball patch</i></sup>


  


