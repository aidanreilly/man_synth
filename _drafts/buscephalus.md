---
layout:     post
title:      Bucephalus Bouncing Ball
summary:    The bouncing ball patch is a great example of how to make your modular synth do things that are not easily done with fixed architecture synths. It is also the quintessential modulate the modulator patch.
comments: true
---
<img src="{{ site.baseurl }}/images/mod12.jpg" alt="mod" class="avatar" />

Contour envelope should be long, slightly logarithmic. MATHS Vari-Response panel controls will act as a sort of Gravity parameter, where both should be set similar and more Logarithmic response will be less gravity. MATHS CH. 1 Fall parameter is a sort of Restitution control. Increasing Fall parameter means the ball will bounce more times. Shorter Falls times will bring fewer bounces. Setting Fall to before NOON will result in no bouncing. High Gravity settings combined with fewer bounces yields a reverb like sound effect with QMMG.

Some things you can do is modulate the rise and fall parameter of the contour envelope at the same time, 

>Gravity. Restitution.

Patch details below.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 graph TB
 D(Main out VCA)-->E(Main out)
F(Trigger)-->A(Contour envelope)
F(Trigger)-->C(Bounce envelope)
A(Contour envelope) -->|VCA in|B(Mod VCA)
B(Mod VCA)-->H(Attenuator)
H(Attenuator)-->|Env fall modulation|C(Bounce envelope)
C(Bounce envelope)-->|CV in|D(Main out VCA)
G(VCO out)-->D(Main out VCA)
</div>
<sup><i>Bouncing ball patch</i></sup>


  


