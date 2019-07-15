---
layout: default
title: Jekyll-Vfolio homepage
---
<div class="jumbotron jumbotron-fluid">
  <div class="container">
    {% if site.data.index.title %}
    <h1 class="text-center text-title font-weight-bold">{{ site.data.index.title }}</h1>
    {% endif %}
    <p class="text-center lead">{{ site.data.index.para1 }}</p>
    <p class="text-center lead">{{ site.data.index.para2 }}</p><br>
  </div>
</div>
<div class="container">
<blockquote>
  {% if site.data.index.credittitle %}
  <p>
    <ul class="text-center">{{ site.data.index.credittitle }}
      {% for entry in site.data.index.creditlinks %}
      <li>{{ entry.linkinfo }} - <a href="{{ entry.linkaddress }}" rel="nofollow noopner noreferer">{{ entry.linktext }}</a></li>
      {% endfor %}
    </ul>
  </p>
  {% endif %}
</blockquote>
</div>
