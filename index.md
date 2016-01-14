---
layout: page
title: Richard Decal
subtitle: Scientist | Traveller | Photographer | Writer
---

<div class="main-explain-area jumbotron">
  <p>I'm a series of space-time events known to go by Richard, Ricardo, Rich (a misnomer), Dick*, and (in some circles) Rich Dick*.</p>

<p>*lies</p>

<p>I'm a high tech low-life, an outdoorsy great indoorsman, a warmhearted, hotwired, heat-seeking cool customer; voice-activated, user-friendly, self-cleaning, and compostable. I'm attractive, proactive, psychoactive, and from time to time I'm radioactive. A high-concept, low profile, farfetched, close-range ballistic missionary. I'm a non-believer and an overachiever, laid-back but forward-thinking, a supercharged subversive, hands on but footloose, straight-up down to earth.</p>
</div>


<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>
	
	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}  
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>
  
    <div class="post-entry">
      {{ post.content | truncatewords: 50 | strip_html | xml_escape}}
	  <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
    </div>
  
   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}