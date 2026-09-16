---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching assistant experience and student mentorship.
nav: true
nav_order: 6
student_mentors:
  - name: Sultan Haidar Ali
    linkedin:
    website:
    portrait:
    project_image:
    project: 3-Segment Continuum Robot
    description: Driven by QDD motors using open-loop control.
  - name: Luka Lin
    linkedin:
    website:
    portrait:
    project_image:
    project: 2-Segment Joystick-Controlled Robot Demo Box
    description: An interactive robot demonstration box designed for K–12 outreach.
---

## Teaching Experience

Teaching assistant roles and related course involvement. Open an entry for details.

{% include courses.liquid %}

## Student Mentorship

Student projects developed through hands-on research mentorship.

<div class="mentor-list">
  {% for mentor in page.student_mentors %}
    <article class="mentor-card">
      <div class="mentor-profile">
        {% if mentor.portrait %}
          {% include figure.liquid path=mentor.portrait alt=mentor.name class="mentor-portrait" %}
        {% else %}
          <div class="mentor-image-placeholder mentor-portrait-placeholder" aria-label="Student portrait placeholder">
            <i class="fas fa-user" aria-hidden="true"></i>
            <span>Student selfie</span>
          </div>
        {% endif %}

        <div class="mentor-identity">
          <h3>{{ mentor.name }}</h3>
          <div class="mentor-links">
            {% if mentor.linkedin %}
              <a href="{{ mentor.linkedin }}" aria-label="{{ mentor.name }} on LinkedIn">
                <i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn
              </a>
            {% endif %}
            {% if mentor.website %}
              <a href="{{ mentor.website }}" aria-label="{{ mentor.name }}'s personal website">
                <i class="fas fa-globe" aria-hidden="true"></i> Personal website
              </a>
            {% endif %}
            {% unless mentor.linkedin or mentor.website %}
              <span class="mentor-links-pending">Links coming soon</span>
            {% endunless %}
          </div>
        </div>
      </div>

      <div class="mentor-project">
        {% if mentor.project_image %}
          {% include figure.liquid path=mentor.project_image alt=mentor.project class="mentor-project-image" %}
        {% else %}
          <div class="mentor-image-placeholder mentor-project-placeholder" aria-label="Project figure placeholder">
            <i class="fas fa-robot" aria-hidden="true"></i>
            <span>Project figure</span>
          </div>
        {% endif %}
        <div class="mentor-project-copy">
          <h4>{{ mentor.project }}</h4>
          <p>{{ mentor.description }}</p>
        </div>
      </div>
    </article>

{% endfor %}

</div>
