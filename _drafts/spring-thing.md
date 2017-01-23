---
layout:     post
title:      Spring things
summary:  This post collects some ideas related to spring reverbs and how to use them in non-standard ways. 
comments: true
---
<img src="{{ site.baseurl }}/images/mod3.jpg" alt="mod" class="avatar" />

There is a lot more that you can do with a spring reverb than simply putting it on the other end of a VCO. Modular systems are made for experimentation and rethinking traditional signal paths. The following ideas and more were originally described in an illuminating muff-wiggler thread.[^1] 

>With the right amount of careful control in the reverb feedback system, a stricken banshee's keen can be summoned that will curdle milk.

## Build a feedback path for your springs

Put a bandpass filter on the feedback path and modulate the filter cutoff with a slow moving LFO. Use attenuation or a vca to control the feedback. This technique can yield some fantastic otherworldly results. With the right amount of careful control in the feedback system, a stricken banshee's keen can be summoned that will curdle milk.

Some spring reverb modules have a feedback path built in. If yours doesn't, take the spring reverb out through the bandpass filter and back into a mixer input. The mixer output then goes back into into the spring reverb input. You could also use a VCA here to control the feedback.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
graph TD;
A(Spring reverb output) --> B(Mixer/VCA)
B(Mixer/VCA)-->C(Bandpass filter)
C(Bandpass filter)-->E(Spring reverb input)
</div>
<sup><i>Basic spring reverb feedback patch</i></sup>

## Add texture to an FM modulation

Here is a neat idea - put your FM oscillator through a spring reverb to add extra character to the modulation. It lends a really woody and grainy sound to the FM modulation. It works best with simple waveforms like sine waves. Some of the usual thing you can do with spring reverbs in the context of modular synthesis apply here too - experiment with adding filters and other signal modifers in series with the spring reverb in the VCO FM signal path. 

This can also work with just a single VCO. Try patching an attenuated sine output from a VCO back to it's own FM input. Dialed in just right, it can yield a nitty-gritty flavour to the sound.
<div class="mermaid">
graph TD;
A(Modulation VCO sine out) --> B(Spring reverb)
B(Spring reverb)-->C(Primary VCO FM input)
</div>
<sup><i>Basic spring reverb FM modulation patch</i></sup>

## Create strange alien sirens and wails

Feeding an LFO into a self oscillating filter is fun. It's even more fun when you feed that filter into some springs. 
<div class="mermaid">
graph TD;
A(LFO) --> B(Self-oscillating bandpass filter)
B(Self-oscillating bandpass filter)-->C(Spring Reverb)
</div>
<sup><i>LFO into bandpass filter spring reverb patch</i></sup>

## Spring modulate a pitch CV

How does this sound?
<div class="mermaid">
graph TD;
A(Pitch CV) --> B(Spring reverb)
B(Spring reverb)-->C(VCO 1V/Oct input)
</div>
<sup><i>Spring modulated 1V/oct patch</i></sup>

---

[^1]: [https://www.muffwiggler.com/forum/viewtopic.php?t=70438](https://www.muffwiggler.com/forum/viewtopic.php?t=70438)