---
layout: default
---
<div class="page-content">
    <div class="home wrapper">
        <img src="https://s.gravatar.com/avatar/a88020276317c22ebc3ab0185d7b4cb7?s=150" class="hero-img" alt=""/>
        <h1 class="hero-text">
            Aman Dogra
        </h1>
        <ul class="hero-props">
            <li>web developer</li>
            <li class="dot"><i class="fa fa-circle"></i></li>
            <li>artist</li>
            <li class="dot"><i class="fa fa-circle"></i></li>
            <li>developer</li>
        </ul>
        <div class="call-to-action-block">
            <a href="{{ site.baseurl }}/blog">Blog</a>
            <a href="{{ site.baseurl }}/work">Work</a>
        </div>
        <ul class="hero-social-list">
            {% if site.github_username %}
            <li>
                <a class="github" target="_blank" href="https://github.com/{{ site.github_username }}">
                    <i class="fa fa-github"></i>
                </a>
            </li>
            {% endif %}

            {% if site.linkedin_username %}
            <li>
                <a class="linkedin" target="_blank" href="https://linkedin.com/in/{{ site.linkedin_username }}">
                    <i class="fa fa-linkedin"></i>
                </a>
            </li>
            {% endif %}

            {% if site.facebook_username %}
            <li>
                <a class="facebook" target="_blank" href="https://www.facebook.com/{{ site.facebook_username }}">
                    <i class="fa fa-facebook"></i>
                </a>
            </li>
            {% endif %}
        </ul>
    </div>
</div>


