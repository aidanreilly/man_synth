---
layout:     post
title:      Spring Things
summary:  Collects some ideas related to spring reverbs and how to use them in non-standard ways in your modular.
comments: true
---
<img src="{{ site.baseurl }}/images/mod11.jpg" alt="mod" class="avatar" />

There is a lot more that you can do with a spring reverb than simply putting it on the other end of a VCO. Modular systems are made for experimentation and rethinking traditional signal paths. The following ideas and more were originally described in an illuminating muff-wiggler thread.[^1]  I have experience with two different spring reverb modules, the Doepfer A-199, and the Music Thing Spring Reverb. The ideas below are equally applicable to both.  

>With the right amount of careful control in the reverb feedback system, a stricken banshee's keen can be summoned that will curdle milk.

## Build a feedback path for your springs

Spring reverb feedback is one of the most simultaneously chaotic and glorious sounds you can produce with a modular synthesizer. When the feedback is tightly controlled, there is nothing else quite like it. It's like holding a perfectly formed miniature explosion in the palm of your hand. 

Put a bandpass filter on the feedback path and modulate the filter cutoff with a slow moving LFO. Use attenuation or a vca to control the feedback. This technique can yield some genuinely otherworldly and unsettling results. With the right amount of careful control in the feedback system, a stricken banshee's keen can be summoned that will curdle milk.

Some spring reverb modules have a feedback path built in. If yours doesn't, take the spring reverb out through the bandpass filter and back into a mixer input. The mixer output then goes back into the spring reverb input. You could also use a VCA here to control the feedback.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
graph TD;
A(Spring reverb) -->|Reverb output| E(Main Out)
B(Mixer/VCA)-->C(Bandpass filter)
C(Bandpass filter)-->|Reverb input|A(Spring reverb)
A(Spring reverb) -->|Reverb output|B(Mixer/VCA)
</div>
<sup><i>Basic spring reverb feedback patch</i></sup>

## Add a metallic flavour to an FM modulation

Here is a neat idea - put your FM oscillator through a spring reverb to add extra character to the modulation. It lends a really grainy sound to the FM modulation. This works best with simple waveforms like sine waves. Some of the usual things you can do with spring reverbs in the context of modular synthesis apply here too - experiment with adding filters and other signal modifers in series with the spring reverb in the VCO FM signal path. 

This can also work with a single self-patched VCO. Try patching an attenuated sine output from a VCO back to it's own FM input. Dialed in just right, it can yield a nitty-gritty flavour to the sound.

<div class="mermaid">
graph TD;
A(Modulation VCO sine out) --> B(Spring reverb)
B(Spring reverb)-->C(Primary VCO FM input)
</div>
<sup><i>Basic spring reverb FM modulation patch</i></sup>

## E.T. wail home

Feeding an LFO into a filter teetering on the edge of self-oscillation is fun. It's even more fun when you feed that filter into some springs. Each component of this patch will need some tweaking to find the sweet spots. Add additional modulation to taste.

<div class="mermaid">
graph TD;
A(LFO) --> B(Self-oscillating bandpass filter)
B(Self-oscillating bandpass filter)-->C(Spring Reverb)
C(Spring reverb) -->G(Main Out)
</div>
<sup><i>LFO into bandpass filter spring reverb patch</i></sup>

## Reverse swell reverb

Hat tip to Tom Whitwell at [music-thing.co.uk](http://musicthing.co.uk/) for this one. You'll need 2 envelopes with an end of cycle (EOC) gate output on one of the envelopes.

  1. Set up one of the envelopes to control a VCA that is clamping down on a sound source to create a string of short blips. Patch the blips into the spring reverb.
  2. Trigger the second envelope with the EOC gate from the first. Make sure the second envelope is set to not loop.
  3. Use the second envelope to control the mix amount between the wet and dry signal coming out  of the reverb. Set the mix amount mostly dry to begin with. The second envelope controls the pseudo-reverse reverb swell. 
  5. Tweak the envelopes and mix CV controls.

<div class="mermaid">
graph TD;
F(Sound source)-->E(VCA)
A(VCA envelope)-->E(VCA)
E(VCA)-->|Reverb input|D(Spring reverb)
A(VCA envelope) -->|EOC trigger| B(Reverb envelope)
B(Reverb envelope)-->|Mix control|D(Spring reverb)
D(Spring reverb) -->G(Main Out)
</div>
<sup><i>Reverse swell reverb patch</i></sup>


---

[^1]: [https://www.muffwiggler.com/forum/viewtopic.php?t=70438](https://www.muffwiggler.com/forum/viewtopic.php?t=70438)