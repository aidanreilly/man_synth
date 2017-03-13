---
layout:     post
title:      The bells
summary:    The bells Esmerelda!
comments: true
---
<img src="{{ site.baseurl }}/images/mod5.jpg" alt="mod" class="avatar" />

#Rubicon bell III

Classic Chowning FM patch to manipulate the Rubicon. Dixie as modulator with off-integer frequency ratio. Sines from both oscillators. The rubicon output passes into a uVCA with partially exponential response. Quadra for both envelopes (amplitude and dynamic FM index). The signal then passes into a linear VCA for velocity-dependent amplitude control and finally to the Audio Damage Dimensions module. Dimensions is modulated by two different slewed S&Hs which yield new voltages each time the Rubicon sounds. Some outboard reverb and DAW delay

Beautiful bell timbres with classic Chowning FM. Rubicon makes it easier with the onboard index VCA. Patch your modulator into TZFM as usual. Then you need 3 copies of your 1v/oct pitch melody. One each to Rubicon and modulator (hopefully a Dixie) and the other into the CV input of a linear VCA. Then patch an envelope which is similar to the amplitude envelope you're using (maybe a tad shorter) through the VCA which your pitch melody is opening and onward to the Rubicon index input. Some off-octave carrier-modulator ratios will get you the sweetest tones. Ever more so with symmetry closer and closer to noon.

Symmetry at 1oclock(ish). Coarse all the way up. Fine tune to a 2nd vco. Patch 2nd vco into tzfm, patch envelope and modulation into index. Pitch sequences to both v/oct inputs. 

Think of symmetry and the 2nd vco frequency as coarse tune, so do NOt bump it or you lose pitch easily. 
Adjust coarse, tzfm, and index to taste. 

Theres some patch examples in the manual too

The bells[^1]

When it comes to bells, the Bell is a bingbingbing. The challenge with Bell is to find a combination of settings and routings that brings out the soul in the bell. The basic idea is simple enough, but the details and subtle modulation are where it comes alive. 


[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid" align="center">
graph TD;
A(Main envelope) -->B(Main VCA)
A(Main envelope) -->|EOC gate|J(Random 1V/oct)
A(Main envelope) -->|EOC gate|K(Random FM modulation)
I(VCO)-->B(Main VCA)
J(Random 1V/oct)-->I(VCO)
K(Random FM modulation)-->I(VCO)
E(Random attack modulation)-->A(Main envelope)
F(Random decay modulation)-->A(Main envelope)
B(Main VCA)-->D(Bandpass filter)
G(Random filter modulation)-->D(Bandpass filter)
D(Bandpass filter)-->H(Main out)
</div>
<sup><i>Simplifed bEll patch</i></sup>


---
[^1]: [https://vimeo.com/48466272](https://vimeo.com/48466272)