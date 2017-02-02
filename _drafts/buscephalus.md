---
layout:     post
title:      Bucephalus Bouncing Ball
summary:    The bouncing ball patch is a great example of how modular synths are uniquely capable of great sound design. It is also the quintessential modulate the modulator patch.
comments: true
---
<img src="{{ site.baseurl }}/images/mod12.jpg" alt="mod" class="avatar" />

content.

>Gravity. Restitution.

Patch details below.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 graph TB
 D(Main out VCA)-->E(Main out)
F(Trigger)-->A(Contour envelope)
F(Trigger)-->C(Bounce envelope)
A(Contour envelope) -->|VCA in|B(Mod VCA)
B(Mod VCA)-->|Env fall modulation|C(Bounce envelope)
C(Bounce envelope)-->|CV in|D(Main out VCA)
</div>
<sup><i>Bouncing ball patch</i></sup>


    Apply same trigger or Gate to CH. 1 CH. 4 Trigger IN. Set Rise to full CCW and Fall to 3 o'clock, Scale/ Inversion to full CW. Patch CH. 1 Signal OUT to CH. 2 Signal IN. Set Ch. 2 Scale/ Inversion to 10 o'clock. Apply CH. 2 signal out to CH. 4 Both IN. Set CH. 4 Rise full CCW, Fall set to NOON, Scale/ Inversion to Full CW and engage Cycle Switch. Patch CH. 4 Signal out to QMMG CH. 1 Signal IN. Patch MATHS CH. 1 Signal OUT Multiple to QMMG CH. 1 Control Signal IN. Set QMMG CH. 1 Offset to full CCW, Feedback to 9 o'clock, set mode to VCA. Apply Signal to be bounced to QMMG CH. 2 Signal IN where Offset is set to full CCW and feedback is set to 9 o'clock, mode is Both. Patch QMMG CH. 1 Signal OUT to QMMG CH. 2 Control Signal IN. Monitor QMMG CH. 2 Signal OUT. MATHS Vari-Response panel controls will act as a sort of Gravity parameter, where both should be set similar and more Logarithmic response will be less gravity. MATHS CH. 1 Fall parameter is a sort of Restitution control. Increasing Fall parameter means the ball will bounce more times. Shorter Falls times will bring fewer bounces. Setting Fall to before NOON will result in no bouncing. High Gravity settings combined with fewer bounces yields a reverb like sound effect with QMMG. 


