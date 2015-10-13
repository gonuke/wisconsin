---
layout: layout
title: About
---

<section class="content">

The {{ site.name }}
===================

<ul class="listing">
<li> <span>Spring 2015</span> <a href="{{ site.url }}/upcoming.html">Upcoming Topics</a></li>
<li> <span>Pre-2015</span> <a href="{{ site.url }}/previous.html">Previous Topics</a></li>
</ul>

Next Meeting
-------------

{% assign upcoming = (site.posts | where: "category", "upcoming") %}
{% assign next_mtg = upcoming.last %}

* Date: {{ next_mtg.date | date: "%B %e, %Y" }}
* Time: {{ next_mtg.time }}
* Location:  {% if next_mtg.location_map %} <a href="{{ next_mtg.location_map }}"> {% endif %}{{ next_mtg.location }}{% if next_mtg.location_map %} </a> {% endif %}
* Topic: <a href="{{ site.url }}{{ next_mtg.url }}"> {{ next_mtg.title }} </a>
{% if next_mtg.author %} * Presenter: {{ next_mtg.author }} {% endif %}

What:
-----

A weekly meeting of researchers who are always learning new tips and tricks to
make their computational work flow more smoothly.  In these friendly sessions,
peers at all levels of experience share topics useful in our scientific
software development workflows.

This meeting would be a great venue for introducing new libraries, showing off
useful features of a scientific library or programming language you're using,
or bringing up a computational problem you're having.

Who:
----

Anyone interested in software development best practices is welcome to come to our meetings.

When:
-----

Every second Tuesday, from 1:30-2:30 PM.

Other chapters:
------------------

  * [U. California-Berkeley](http://thehackerwithin.github.io/berkeley) (USA)
  * [U. Melbourne](http://thehackerwithin.github.io/melbourne) (Australia)

<a href="http://twitter.com/share" class="twitter-share-button" data-count="none" data-via="{{ site.twitter }}">Tweet</a>
<a href="http://twitter.com/{{ site.twitter }}" class="twitter-follow-button" data-show-count="false">Follow @{{ site.twitter }}</a>
<script src="http://platform.twitter.com/widgets.js" type="text/javascript"></script>



</section>

[me_map]: http://map.wisc.edu/s/4olvug5e
[sterling_map]: http://map.wisc.edu/s/jzb4imln
