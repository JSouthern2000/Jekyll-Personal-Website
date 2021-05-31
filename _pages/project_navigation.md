---
layout: default
title: Projects
permalink: /project/
heading: Projects
subheading: See the work I've done!
---
<div class="row row-cols-1 row-cols-md-3 g-4 align-items-center justify-content-center">
  {% for post in site.categories['project'] %}
    <div class="col">
      <div class="card text-white bg-dark w-75 h-100" href="{{ project.url }}" >
        <img class="card-img-top" src="{{ project.thumbnail }}">
        <div class="card-body">
          <h5 class="card-title">{{project.title}}</h5>
          <p class="card-text">{{ project.description | truncatewords: 30 }} </p>
        </div>
        <div class="card-footer">
              <small class="text-muted">{{ post.tags }} • {{ post.date-custom }}</small>
        </div>
        <a href="{{ project.url }}" class="stretched-link"></a>
      </div>
    </div>
  {% endfor %}
</div>
