---
layout: page
title: Categories
<!--permalink: /categories/-->
---


<div class="tags categories">
  <div class="tags-list">
    {% for tag in site.categories %}
    <a href="#{{ tag[0] | slugify }}" class="category">{{ tag[0] }}</a>
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-section">
    {% for tag in site.categories %}
    <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
    <ul class="tags-posts">
      {% for post in tag[1] %}
      <li>
        <a class="post-title" href="{{ post.url }}">
        <strong>{{ post.title }}</strong><br />
        </a>
        <small class="post-date">{{ post.date | date_to_string }}</small>
      </li>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>

<!--
<div class="tags-list">
    {% for tag in site.categories %}
    <a href="#{{ tag[0] | slugify }}" class="category"><span class="icon-tag"></span>{{ tag[0] }}</a>
    {% endfor %}
 </div>

<div class="container">

<div class="row">
  <div class="text-center">
    <ul class="list">
       {% for tag in site.categories %}
        <li class="description">
            <div class="datetime">
                <span class="day">
                    {{ tag[0] }}
                </span>
            </div>
            <div class="post-details">
                <ul class="tags-posts">
									{% for post in tag[1] %}
											<a class="post-title" href="{{ site.baseurl }}{{ post.url }}">
												<li>
													{{ post.title }} | <small class="post-date">{{ post.date | date_to_string }}</small>
												</li>
											</a>
									{% endfor %}
								</ul>
            </div>
        </li>
        <div class="divider"></div>
       {% endfor %}
    </ul>
  </div>
</div>
</div>-->
