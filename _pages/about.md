---
layout: default
permalink: /
title: about
nav: about

<!--description: <a href="https://ai.google/" target="_blank">Google AI</a> -->
<!--address: <a href="https://www.google.com/maps/place/Googleplex/@37.4220656,-122.0862837,17z/data=!3m1!4b1!4m5!3m4!1s0x808fba02425dad8f:0x6c296c66619367e0!8m2!3d37.4220656!4d-122.0840897" class="page-description" target="_blank">Mountain View, California, USA </a-->
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Clément Quinton</h1>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>

<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'prof_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
         I am an associate professor at the University of Lille, member of the <a href="https://team.inria.fr/spirals/">Spirals</a> group, a joint team between the University of Lille within the <a href="https://www.cristal.univ-lille.fr/en/?force_lang=true">CRIStAL</a> research center, and <a href="https://www.inria.fr/en/">Inria</a>.
        </p>
        
        <p>
         Before joining the University of Lille, I was a postdoctoral fellow at Politecnico di Milano. I hold a MSc. in Computer Science from the University of Montpellier, and a PhD in Computer Science from the University of Lille. Prior to the PhD, I spent two years as a software engineer developing tools and apps for smartphones.
        </p>
    </div>
</div>

<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge blue darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
