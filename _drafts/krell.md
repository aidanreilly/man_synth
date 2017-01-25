---
layout:     post
title:      Behold the Krell
summary:    Behold the Krell
comments: true
---
<img src="{{ site.baseurl }}/images/mod5.jpg" alt="mod" class="avatar" />

The Krell patch is based on an idea for the Buchla 200e articulated by Todd Barton[^1]. Krell captures the imagination. When it is emerges from the skronky murk, it is a phantasm, writhing and cavorting in the machine.  The challenge with Krell is to find a combination of settings and routings that brings out the soul in the machine. The basic idea is simple enough, but the details and subtle modulation are where it comes alive. 

At the heart of it is a single monophonic synth sound controlled by an AD envelope with seperate modulations for the attack and fall portions the envelope. These rise and fall modulations can give amazing variations in tempo and dynamics depending on how modulation is applied.

There are any number of variations of this patch and it can grow and be expanded upon to fit whatever size modular system you have at hand. For my purposes, I like to keep things as simple as possible.

The heart of Krell is a single looping envelope controlling a master output VCA. An AD envelope that has an end-of-cycle (EOC) gate output and rise and fall modulation control is ideal. The cycling EOC gate trigger is used to drive the entire patch. The EOC gate is used to grab a random pitch voltage and feed it to a VCO whose amplitude is controled by the master output VCA. Slow random VCO FM modulations are woven in and out as time progresses. A final random modulated filter adds timbral variation. 

A module that provides some level of control over a random voltage is pretty essential for Krell. However, you can get pretty far with some sample and hold, slew, and noise/LFOs. At each point along the relatively simple path outlined above, you add as much or as little modulation as the patch needs.

Add correlation between elements such as pitch, FM depth, filter frequency to really make this patch sing. For example, Use one related random voltage to select lower or higher pitches, while the other other slowly sweeps the filter frequency. Modulate the attack and decay parameters of the master envelope with cross patched  LFOs. Match pitch to envelope.

>When it is emerges from the skronky murk, it is a phantasm, writhing and cavorting in the machine.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
graph TD;
A(Main envelope) -->B(Main VCA)
I(VCO)-->B(Main VCA)
J(Random 1V/oct)-->I(VCO)
E(Attack modulation)-->A(Main envelope)
F(Decay modulation)-->A(Main envelope)
B(Main VCA)-->D(Bandpass filter)
G(Filter modulation)-->D(Bandpass filter)
D(Bandpass filter)-->H(Main out)
</div>
<sup><i>Simplifed Krell patch</i></sup>


---
[^1]: [https://vimeo.com/48466272](https://vimeo.com/48466272)