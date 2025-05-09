---
layout: page
permalink: /team/
title: Team
description: Members of PolySmart Group.
nav: true
nav_rank: 2
---

{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
## {{ group }}

    {% assign members = site.members | sort: "lastname" | where: "group", group %}
    {% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %}">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" style="padding-top: 0" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    <!-- {% if member.inline == false %}<a href="{{ member.url | relative_url }}">{% endif %} -->
                    <h5 class="card-title">{{ member.profile.name }}</h5>
                    {% if member.profile.degree %}<h6 class="card-subtitle mb-2 text-muted"><em>{{ member.profile.degree }}</em></h6>{% endif %}
                    {% if member.profile.position %}
                    <h6 class="card-subtitle mb-2 text-muted">
                        {{ member.profile.position }}{% if member.profile.award %}; <a href="https://www.polyu.edu.hk/gs/prospective-students/fellowship-scholarship-schemes/" style="font-style: italic; 
          background: linear-gradient(to right, #f39c12, #e67e22, #e74c3c); 
          -webkit-background-clip: text; 
          color: transparent; 
          font-weight: 600;">{{ member.profile.award }}</a>
                        {% endif %}
                    </h6>
                    {% endif %}
                    {% if member.profile.time %}<h6 class="card-subtitle mb-2 text-muted">{{ member.profile.time }}</h6>{% endif %}
                    <!-- <p class="card-text">
                        {{ member.teaser }}
                    </p> -->
                    {% if member.inline == false %} {% endif %}
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.scholar %}
                        <a href="{{ member.profile.scholar }}" class="card-link" target="_blank"><i class="fab fa-google-plus-square"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.linkedin %}
                        <a href="https://linkedin.com/in/{{ member.profile.linkedin }}/" class="card-link" target="_blank"><i class="fab fa-linkedin"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ member.profile.orcid }}" class="card-link" target="_blank"><i class="fab fa-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    {% if member.profile.website %}
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    {% if member.profile.interest %}
                        <p class="card-text" style="margin-bottom: 0.3rem;">
                            <small class="test-muted"><i class="fas fa-magnifying-glass"></i> {{ member.profile.interest | replace: '<br />', ', ' }}</small>
                        </p>
                    {% endif %}
                    {% if member.profile.address %}
                        <p class="card-text" style="margin-bottom: 0.3rem;">
                            <small class="test-muted"><i class="fas fa-thumbtack"></i> {{ member.profile.address | replace: '<br />', ', ' }}</small>
                        </p>
                    {% endif %}


                </div>
            </div>
        </div>
    </div>

</p>
    {% endfor %}
<br>
<br>
<br>
{% endfor %}
