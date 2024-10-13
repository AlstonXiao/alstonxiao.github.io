---
permalink: /
title: "Hello! This is Yan Xiao"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
![illustration](/images/about-normal.png){: .align-right width="300px"}
I’m passionate about 3D neural rendering and computer vision, driven by the belief that we can reshape the way people experience the digital world. My focus is on capturing the real world and creating digital twins that can be shared, relived, and freely edited. My experience spans neural relighting and delighting of objects, leveraging neural representations like NeRFs and SDFs to achieve photorealistic results. 

I currently working at Apple's Persona team and focusing on advancing dynamic neural representations for digital humans, pushing the boundaries of what's possible in immersive, lifelike virtual experiences.

I may write about general neural rendering and paper reviews on [my blog](/year-archive/).
<hr style="border:2px solid gray;border-radius: 2px;">

Publication
======
{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
## {{ category[1].title }}
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
