---
layout: page
title: Home
id: home
permalink: /
---

<h2>Recent Posts</h2>
<ul>
  {% assign recent_notes = site.notes | sort: "origdate" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.origdate | origdate: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<h3>Overview</h3>
[[Your first note]]

<h3>Overview</h3>
<div class="overview">
  {% include [[Your first note]] %}
</div>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
