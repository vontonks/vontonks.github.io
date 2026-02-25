---
layout: vonlayout
title: Home
---

<div class="hero">
  <h2>Senior Policy Advisor · Tech Journalist · Writer</h2>
  <p>I'm an award-winning journalist turned senior policy advisor, combining deep expertise in technology and the written word to advocate for Australia's IT industry.</p>
</div>

<div class="two-columns">
  <div class="column">
    <h3>For Employers</h3>
    <p>6+ years in tech journalism and policy. I've led strategic projects, delivered clear advice to stakeholders, and built a reputation for excellent, efficient work.</p>
    <ul>
      <li>Senior Policy Advisor at the Australian Computer Society</li>
      <li>Finalist, IT Journalism Awards (2020, 2021)</li>
      <li>Former Senior Journalist at Information Age</li>
    </ul>
    <p><a href="/experience" class="button">View Experience →</a></p>
  </div>
  
  <div class="column">
    <h3>For Publishers</h3>
    <p>Honours in Creative Writing from the University of Adelaide. Published fiction, poetry, and academic work across multiple outlets.</p>
    <ul>
      <li>Short fiction in Magic Oxygen Literary Prize Anthology</li>
      <li>Poetry in Between Dusk and Dawn anthology</li>
      <li>Co-editor, Against the Odds: Care Leavers at University</li>
    </ul>
    <p><a href="/publications" class="button">View Publications →</a></p>
  </div>
</div>

<div class="recent-writing">
  <h3>Recent Writing</h3>
  <ul>
    {% for post in site.posts limit:3 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date">{{ post.date | date: "%B %Y" }}</span></li>
    {% endfor %}
  </ul>
  <p><a href="/blog">See all posts →</a></p>
</div>
