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

<a href="http://www.aureusgroup.com/"><img src="http://www.aureusgroup.com/design/landing/agbox.jpg" alt="Aureus"></a>

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

We usually meet at [Businessolver](https://www.google.com/maps/place/Businessolver+Inc/@41.5851253,-93.7179891,17z/data=!3m1!4b1!4m2!3m1!1s0x0:0xc9221c27d26bc690), but in March we're meeting at <a href="/assets/PrincipalCampusMap.pdf">Principal Financial
Group (750 Park St downtown.)</a>  The meeting will be in the z-shaped building, in the southwest corner of the 1st floor.  The security entrance you’ll need to enter is also on the west side of the “Z” but on the north side.  You access that entrance from Park St.  Our security staff has asked attendees to park in lot L2, just north of the Z building. 

## Archives

<ul class="posts">
  {% for post in site.categories.meeting limit: 5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
