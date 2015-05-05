---
layout: page
title: Central Iowa Java User Group
tagline:  A group for Java, JVM, and other cool technology aficionados
---
{% include JB/setup %}

<div class="blog-index">  
  {% assign post = site.categories.meeting.first %}
  {% assign content = post.content %}
  {% include post_detail.html %}
</div>

{% comment %}<a href="http://www.teksystems.com/locations/united-states/iowa/des-moines"><img src="http://www.teksystems.com/~/media/teksystems_com/images/utility_images/teksystems-logo.ashx?h=65&la=en&w=245" alt="TekSystems"></a>{% endcomment %}
<a href="http://www.mumosystems.com/careers/"><img src="/assets/mumo-dsmhack-large.png" alt="Mumo Systems"></a>

## Who We Are

CIJUG is a user group for application developers in the Central Iowa area. We meet the first Tuesday of the month to discuss Java, JVM technologies, or 
anything else interesting (Javascript, NoSQL, DevOps, etc)


## How to [Join](https://groups.google.com/forum/?fromgroups#!forum/central-iowa-java-users-group)

<div style="display: inline-block">
	<form action="http://groups.google.com/group/Central-Iowa-Java-Users-Group/boxsubscribe">	  
	  <ul class="tag_box inline" style="float:right;">
		<li>
			<input type="text" name="email" placeholder="Enter your e-mail..." style="float:left; margin-right:5px"/>
			<a href="#" onclick="document.forms[0].submit();">Join</a>
		</li>
	  </ul>     
	</form>
</div>

## Where to Find Us

We usually meet at [Businessolver](https://www.google.com/maps/place/Businessolver+Inc/@41.5851253,-93.7179891,17z/data=!3m1!4b1!4m2!3m1!1s0x0:0xc9221c27d26bc690)
-> 1025 Ashworth Rd #403, West Des Moines, IA 50265


## Archives

<ul class="posts">
  {% for post in site.categories.meeting limit: 5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
