---
layout: default
---


<img src="/images/jmb.jpg" alt="Drawing" style="width: 200px;"/>



* Full list of [Publications](/pubs.html)
* Academic [CV](/cv/long-cv.pdf)



<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>






