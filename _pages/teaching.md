---
layout: page
permalink: /teaching/
title: teaching
description: 
nav: true
---

<p><i>"It is the supreme art of the teacher to awaken joy in creative expression and knowledge." - ALBERT EINSTEIN</i></p>



  <h4> As teaching assistant: </h4>
   <h6>University of California Santa Barbara, Department of Engineering Sciences:</h6>
   <p>
     <ul>
     <li> ENGR 3. Introduction to Programming (4times), </li>
     </ul>
   </p>

   <h6>University of California Santa Barbara, Department of Mechanical Engineering:</h6>
   <p>
     <ul>
       <li>ME 125/225ML. Special Topics: Research Topics in Machine Learning and System Identification,</li>
       <li>ME 152B. Fluid Mechanics II,</li>
       <li>ME 151B. Thermosciences II,</li>
       <li>ME 17. Mathematics of Engineering (twice),</li>
     </ul>
   </p>

   <h6>New Mexico State University, Department of Computer Science: </h6>
   <ul>
     <li>Object Oriented Programming with C++ (3times), </li>
     
   </ul>
   <h6> New Mexico State University, Young Women in Computing Program (YWiC):</h6>
   <ul>
     <li>YWiC offers fun and engaging activities for elementary, middle and high school students.  The primary goal is to share the creativity of computing through hands-on tasks and project-based learning.  I was involved  in  developing  interactive  and  engaging  curriculum,  teaching  Java,  Java  Script,  HTML  andLinux, Scratch, Pencil Code, LilyPad Arduino, EV3, MIT App Inventor, etc.  as well as assisting the outreach events and activities such as summer camps and after school programs.</li>

   </ul>

<br>

<div class="projects grid">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  {% for project in sorted_projects %}
  {% if project.title== "YWiC"%}
  <div class="grid-item">
    {% if project.redirect %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
   

