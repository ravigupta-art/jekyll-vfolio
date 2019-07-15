---
layout: normal
title: Non Fiction Films
---
 <div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1 class="text-center text-banner font-weight-bold text-title">NON FICTION FILMS</h1><!-- Card padding is custom css added to have a proper space between h1 and cards -->
    {% assign no_of_videos = site.data.non-fiction-films | size %}
    {% assign count = 0 %}
    {% assign half = no_of_videos | divided_by: 2 %}
    {% for item in (1..half) %}
      {% if site.data.non-fiction-films.first %}
         <div class="card-deck mb-3 text-center card-padding">
           {% for j in (1..2) %}
            <div class="card mb-4 box-shadow">
              <div class="card-header">
                <h4 class="my-0 font-weight-normal text-title"><strong>{{ site.data.non-fiction-films[count].videotitle }}</strong></h4>
              </div>
              <div class="card-body">
                <div class="embed-responsive embed-responsive-16by9">
                 {% if site.data.non-fiction-films[count].videotype == 'youtube' %}
                   <iframe src="https://www.youtube.com/embed/{{ site.data.non-fiction-films[count].videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                   {% elsif site.data.non-fiction-films[count].videotype == 'vimeo' %}
                   <iframe src="https://player.vimeo.com/video/{{ site.data.non-fiction-films[count].videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                 {% endif %}
                </div>
                <h5><br>{{site.data.non-fiction-films[count].videodescription }}</h5><br>
                <p><span class="font-weight-bold">My Contribution:</span> {{ site.data.non-fiction-films[count].contrib }}</p>
                <ul class="list-unstyled mt-3 mb-4">
                  <li class="font-weight-bold">Awards:</li>
                  {% for entry in site.data.non-fiction-films[count].Awards %}
                   <li>{{ entry.award }}
                     {% if entry.awardinfo %}
                     <span class="text-muted">
                       <br>{{ entry.awardinfo }}
                     </span>
                     {% endif %}
                   </li><br>
                  {% endfor %}
                </ul>
              </div>
            </div>
            {% assign count = count | plus:1 %}
           {% endfor %}
         </div>

      {% endif %}
    {% endfor %}
    {% assign odd_videos = no_of_videos | modulo: 2 %}
    {% if odd_videos != 0 %}
      <div class="card-deck mb-3 text-center">
        <div class="card mb-4 box-shadow">
          <div class="card-header">
            <h4 class="my-0 font-weight-normal text-title"><strong>{{ site.data.non-fiction-films[count].videotitle }}</strong></h4>
          </div>
          <div class="card-body">
            <div class="embed-responsive embed-responsive-16by9">
             {% if site.data.non-fiction-films[count].videotype == 'youtube' %}
               <iframe src="https://www.youtube.com/embed/{{ site.data.non-fiction-films[count].videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
               {% elsif site.data.non-fiction-films[count].videotype == 'vimeo' %}
               <iframe src="https://player.vimeo.com/video/{{ site.data.non-fiction-films[count].videoID }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
             {% endif %}
            </div>
            <h5><br>{{site.data.non-fiction-films[count].videodescription }}</h5><br>
            <p><span class="font-weight-bold">My Contribution:</span> {{ site.data.non-fiction-films[count].contrib }}</p>
            <ul class="list-unstyled mt-3 mb-4">
              <li class="font-weight-bold">Awards:</li>
              {% for entry in site.data.non-fiction-films[count].Awards %}
               <li>{{ entry.award }}
                 {% if entry.awardinfo %}
                 <span class="text-muted">
                   <br>{{ entry.awardinfo }}
                 </span>
                 {% endif %}
               </li><br>
              {% endfor %}
            </ul>
          </div>
        </div>
      </div>
    {% endif %}
  </div>
</div>
