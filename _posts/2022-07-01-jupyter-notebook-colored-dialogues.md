---
layout: post
title: Jupyter Notebook Colored Dialogue Boxes
tags: python
---

Many thanks to [Daniel Kotik](https://gist.github.com/DanielKotik/4b81480c479a57e0dd13ac4d153e4451) for the following HTML that can be dropped into a Jupyter notebook markdown cell:

```html
<div class="alert alert-block alert-info"> 
    <b>NOTE</b> 
    Use blue boxes for Tips and notes. 
    </div>

<div class="alert alert-block alert-success"> 
    Use green boxes sparingly, and only for some specific purpose 
    that the other boxes can't cover. For example, if you have a 
    lot of related content to link to, maybe you decide to use 
    green boxes for related links from each section of a notebook. 
    </div>

<div class="alert alert-block alert-warning"> 
    Use yellow boxes for examples that are not inside code cells, 
    or use for mathematical formulas if needed. 
    </div>

<div class="alert alert-block alert-danger"> 
    In general, just avoid the red boxes. 
    </div>
```