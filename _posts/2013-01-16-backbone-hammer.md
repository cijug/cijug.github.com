---
layout: post
title: "Getting swipe to work in Backbone"
date: 2013-01-16 15:10
comments: true
categories: tech
---
Have a [backbone.js] app and need it to respond to touch
events? With [hammer.js], it's easy.

## index.html

{% highlight html linenos %}
<html>
  <head>
    <title>Swipe Backbone with Hammer.js</title>
		<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">		
		<style>
			#swiping {
				height: 100px;
				width: 300px;
				text-align: center;				
				background: blue;
				color: white;
			}			
		</style>
  </head>
  <body>				
		<div id="swiping"></div>
		
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js"></script>
    <script src="js/underscore.js"></script>
    <script src="js/backbone.js"></script>		
    <script src="js/hammer.js"></script>
    <script src="js/jquery.specialevent.hammer.js"></script>
    <script src="js/main.js"></script>
  </body>

</html>
{% endhighlight %}

In the html, we've included the required libraries and created
an empty swipe zone ("swiping"). We'll use this div to load
our view.

##main.js

{% highlight javascript linenos %}
AppView = Backbone.View.extend({
  el: '#swiping',					
    
  events: {
    'swipe': 'swipeMe'
  },
    
  render: function(){				
    this.$el.html('<h2>Swipe Me</h2>');
  },
    
  swipeMe: function(e){				
    alert('swiped ' + e.direction);
  }
    
});

var view = new AppView();
view.render();		
{% endhighlight %}

This looks like a pretty standard Backbone view. The important part is
on line 5. Here we're telling backbone to respond to hammer's swipe
event with the "swipeMe" function. 

The event's direction method tells you if they swiped forward
or backwards. 

Its not the best documented set-up, but this [gist] helped me. Once set-up, it's amazing how easy you can get backbone to respond to touch events.

[backbone.js]:http://backbonejs.org/
[hammer.js]:http://eightmedia.github.com/hammer.js/
[gist]:https://gist.github.com/4279025 
