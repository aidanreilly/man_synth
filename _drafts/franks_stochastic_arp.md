---
layout:     post
title:      Frank's Stochastic Arp
summary:    Frank's stochastic arp patch is taken from Allen Strange's book.
comments: true
---
<img src="{{ site.baseurl }}/images/mod10.jpg" alt="mod" class="avatar" />

content.

[//]: <> (https://knsv.github.io/mermaid/#styling-and-classes)
<div class="mermaid">
 graph TB
         subgraph 
         A(Master envelope) -->B(Main VCA)
         end
         subgraph 
         C(Sound source)-->B(Main VCA)
         end
         subgraph   
         A(Main envelope) -->|EOC gate|J(Random 1V/oct)
         end
</div>
<sup><i>Frank's stochastic arp patch</i></sup>

Here is what it sounds like:

<iframe id="sc-widget" width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/287620763&amp;color=ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false"></iframe>
