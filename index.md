---
layout: page
title: Central Iowa Java User Group
tagline:  A group for Java, JVM, and other cool technologies
---
{% include JB/setup %}

## Who We Are

CIJUG is a user group for application developers in the Central Iowa area. We meet the first Tuesday of the month to discuss Java, JVM technologies, or 
anything else interesting (Javascript, NoSQL, DevOps, etc)

## Where to Find Us

We meet at [Meredith Publishing](http://maps.google.com/maps/place?q=1716+locust&hl=en&cid=11632086222648977254). Free parking is available in the garage on the south side of Locust.

## How to Join

To join: E-mail the Central Iowa Java User [Google Group](mailto:central-iowa-java-users-group+subscribe@googlegroups.com)

<div class="blog-index">  
  {% assign post = site.posts.first %}
  {% assign content = post.content %}
  {% include post_detail.html %}
</div>


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



