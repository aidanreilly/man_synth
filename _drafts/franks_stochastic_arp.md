---
layout:     post
title:      Frank's Stochastic Arp
summary:    Frank's stochastic arp patch is taken from Allen Strange's book.
comments: true
---
<img src="{{ site.baseurl }}/images/mod1.jpg" alt="mod" class="avatar" />

content.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 %% Subgraph example
 graph TD
         subgraph Sound
         A(Master envelope) -->B(Main VCA)
         end
         subgraph Modulation
         C(Sound source)-->B(Main VCA)
         end
         subgraph Pitch
         A(Main envelope) -->|EOC gate|J(Random 1V/oct)
         end
</div>
<sup><i>Frank's stochastic arp patch</i></sup>


