---
layout: page
title: Home
id: home
permalink: /
---
[[Overview]]

<h2>Recent Posts</h2>
<ul>
  {% assign recent_notes = site.notes | sort: "origdate" | reverse %}
  {% for note in recent_notes limit: 5000 %}
    <li>
      {{ note.origdate | origdate: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>






<style>
  .wrapper {
    max-width: 46em;
  }
</style>
