---
layout: default
---

<section class="intro">
  <h1>Welcome</h1>
  <p class="bio">
    I'm Bert. Computer engineering student at the University of Ghana, into
    embedded systems and figuring out how to build things that actually work.
    This is where I write about what I'm learning, building, and thinking
    about, mostly unfiltered.
  </p>
  <p class="find-me">Find Me</p>
  <p class="social">
    <a href="https://www.linkedin.com/in/bertbnk/" target="_blank" aria-label="LinkedIn">
      <svg viewBox="0 0 448 512" fill="currentColor"><path d="M100.28 448H7.4V148.9h92.88zm-46.44-338.5C24.09 109.5 0 85.4 0 55.9 0 25.4 24.1 1 53.84 1c29.7 0 53.84 24.4 53.84 54.9 0 29.5-24.14 53.6-53.84 53.6zM447.9 448h-92.68V302.4c0-34.7-.7-79.2-48.29-79.2-48.29 0-55.69 37.7-55.69 76.7V448h-92.78V148.9h89.08v40.8h1.3c12.4-23.5 42.69-48.3 87.88-48.3 94 0 111.28 61.9 111.28 142.3V448z"/></svg>
    </a>
    <a href="https://github.com/bertqrt" target="_blank" aria-label="GitHub">
      <svg viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
    </a>
    <span class="email">bertrandoseiowusu22@gmail.com</span>
  </p>
</section>

<div class="feed">
  {% for post in site.posts %}
  <a class="entry" href="{{ post.url | relative_url }}">
    {% assign words = post.content | strip_html | number_of_words %}
    {% assign read_time = words | divided_by: 200 | at_least: 1 %}
    <p class="meta">{{ read_time }} min &middot; {{ post.date | date: "%b %-d, %Y" }}</p>
    <div class="entry-header">
      <h2>{{ post.title }}</h2>
      {% if post.image %}
      <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="entry-thumb" loading="lazy">
      {% endif %}
    </div>
    <p class="hook">{{ post.excerpt | strip_html }}</p>
  </a>
  {% endfor %}
</div>
