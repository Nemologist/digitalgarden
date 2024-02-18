---
layout: page
title: Home
id: home
permalink: /
---
1
<h2>Recent Posts</h2>
<ul>
  {% assign recent_notes = site.notes | sort: "origdate" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.origdate | origdate: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
    <!--{% include note %}-->
  {% endfor %}
</ul>

<h3>Overview</h3>
[[Your first note]]

<!--
<h3>Overview1</h3>
{% include [[Your first note]] %}
-->



<style>
  .wrapper {
    max-width: 46em;
  }
</style>
