---
title: projects
layout: main
---
<div>
    <div class="text-box">
        <p>
            You can find me on
            <a href="" target="_blank" class="link-style">LinkedIn</a> or
            contact me via my
            <a href="" target="_blank" class="link-style">email</a>.
        </p>
    </div>
</div>
<div class="projects grid-two-columns">
{% assign sorted = site.posts | sort: 'date' | reverse  %}
{% for post in sorted %}
    <a href="{{ post.url }}" class="wrapper">
        <img src="{{ post.img-link }}" />
        <div class="project-brief">
            {{ post.project-title }}
        </div>
        <div class="project-detail">
            <strong>{{ post.project-subtitle }}</strong>
            <br />
            {{ post.description }}
        </div>
    </a>
{% endfor %}
</div>