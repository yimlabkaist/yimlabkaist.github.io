---
layout: page 
permalink: /news/
title: news
order: 5
nav: true
social: false
---

---
layout: page
title: news
permalink: /news/
nav: true
nav_order: 5
---

<div class="news">
  
  {% if site.news != blank -%} 
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign news = site.news | reverse -%} 
    {% for item in news %}
      <tr>
        <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
        <td>
          {% if item.inline -%} 
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {%- else -%} 
            <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
          {%- endif %} 
        </td>
      </tr>
    {%- endfor %}
    </table>
  </div>
{%- else -%} 
  <p>No news so far...</p>
{%- endif %} 
</div>
