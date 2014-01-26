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
<a href="http://www.teksystems.com/it-careers/search-results?toff=477&officeid=641"><img src="http://www.teksystems.com/~/media/Images/Branding/TEKsystems-logo.ashx" alt="TekSystems"></a>

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

We meet at [Startup City](https://maps.google.com/maps?q=startupcity+des+moines&ie=UTF-8&ei=CnDlUsWcNuilsQTht4CADw&ved=0CAkQ_AUoAQ) (317 6th Ave., 5th floor
Downtown Des Moines). 

Parking can be found in the following locations:  

* Street lot at 5th and Court 
* The EMC lot at 8th and Mulberry
* The lot at 5th and Locust 
* Street parking at any open meter
 

## Archives

<ul class="posts">
  {% for post in site.categories.meeting limit: 5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
