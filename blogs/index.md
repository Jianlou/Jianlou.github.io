---
layout: front
title: Blogs
---

<div class="grid">
        <div class="unit w-2-3 center-on-mobiles align-left">
        	<h3><font color="blue">My blogs</font></h3>
			<div id="home">
			  <ul class="posts">
			    {% for post in site.posts %}
			      <li><span>[{{ post.date | date:"%d/%m/%Y"}}]</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a>
				{{ post.excerpt }}</li>
			    {% endfor %}
			  </ul>
			</div>
        </div>
        <div class="unit w-1-3 center-on-mobiles align-left">
        	<h3><font color="blue">Archive by category</font></h3>
        	{% for category in site.categories %}
			<font color="red"><span>{{ category | first }}({{ category | last | size }})</span></font>
			<ul class="posts">
			    {% for post in category.last %}
			        <font size="2"><li>[{{ post.date | date:"%d/%m/%Y"}}]&nbsp;<a href="{{ post.url }}">{{ post.title }}</a></li></font>
			    {% endfor %}
			</ul>
			{% endfor %}
        </div>
</div>


