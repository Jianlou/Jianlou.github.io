---
layout: front
title: Blogs
---

<div class="grid">
        <div class="unit w-2-3 center-on-mobiles align-left">
        	<h2>My blogs</h2>
			<div id="home">
			  <ul class="posts">
			    {% for post in site.posts %}
			      <li><span>[{{ post.date | date:"%d/%m/%Y"}}]</span> &nbsp; <a href="{{ post.url }}"><font color="#8B4C39">{{ post.title }}</font></a>
				{{ post.excerpt }}</li>
			    {% endfor %}
			  </ul>
			</div>
        </div>
        <div class="unit w-1-3 center-on-mobiles align-left">
        	<h2>Archive by category</h2>
        	{% for category in site.categories %}
        	<div class="grid">
        		<div class="unit w-1-4 center-on-mobiles align-left">
        			<font color="red"><span>{{ category | first }}({{ category | last | size }}):</span></font>
        		</div>
        		<div class="unit w-3-4 center-on-mobiles align-left">
        			<ul class="posts">
			    	{% for post in category.last %}
			        	<font size="2"><li>[{{ post.date | date:"%d/%m/%Y"}}]&nbsp;<a href="{{ post.url }}">{{ post.title }}</a></li></font>
			   		{% endfor %}
					</ul>
        		</div>
        	</div>
			{% endfor %}
        </div>
</div>


