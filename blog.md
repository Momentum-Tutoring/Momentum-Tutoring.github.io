---
layout: page
title: Blog
---
<h1>Blog</h1>
<hr>

<div class="posts">
  {% for post in site.posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>

    {{ post.content }}
  </div>
  {% endfor %}
</div>








<!-- ############################################################################ -->
<!-- 
Original Code for posts and pagination. I couldn't get it to work in this markdown file
so there will just be no pagination for now. Just list of blogs.
-->


<!-- 
<div class="posts">
  {% for post in paginator.posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>

    {{ post.content }}
  </div>
  {% endfor %}
</div>


<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="/page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="/">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="/page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div> -->