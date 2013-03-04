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

## Who We Are

CIJUG is a user group for application developers in the Central Iowa area. We meet the first Tuesday of the month to discuss Java, JVM technologies, or 
anything else interesting (Javascript, NoSQL, DevOps, etc)

## Our Sponsor
<a href="http://www.teksystems.com/"><img src="http://www.teksystems.com/~/media/Images/Branding/TEKsystems-logo.ashx" alt="TekSystems"></a>

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

We meet at [Meredith Publishing](https://maps.google.com/maps?ie=UTF8&cid=7053981532446613691&q=Meredith+Corporation&iwloc=A&gl=US&hl=en-US). Free parking is available in the garage on the south side of Locust.

<ul class="posts">
  {% for post in site.categories.meeting limit: 5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
