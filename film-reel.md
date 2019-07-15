---
layout: normal
---

<div class="jumbotron jumbotron-fluid">
  {% for item in site.data.film-reel %}
  <div class="container">
    <h1 class="text-center text-banner font-weight-bold text-title">{{ item.heading }}</h1>
    <p class="lead text-center">{{ item.subheading }}</p>
     <div class="embed-responsive embed-responsive-16by9">
      {% if item.videotype == 'youtube' %}
       <iframe src="https://www.youtube.com/embed/{{ item.videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        {% elsif item.videotype == 'vimeo' %}
        <iframe src="https://player.vimeo.com/video/{{ item.videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      {% endif %}
     </div>
  </div>
  {% endfor %}
</div>
