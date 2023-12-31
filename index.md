---
layout: home
title: விஜய்
---

{{ site.email }}

<!-- <a href="vaasippu/">#வாசிப்பு</a> -->

<div class="card-presentation">
    <a href="read/"><p class="card-presentation-title" style="background-color:beige">#வாசிப்பு</p></a>
    <a href="translate/"><p class="card-presentation-title" style="background-color:beige">#மொழிபெயர்ப்பு</p></a>
    <a href="article/"><p class="card-presentation-title" style="background-color:beige">#கட்டுரை</p></a>
    <a href="notes/"><p class="card-presentation-title" style="background-color:beige">#குறிப்பு</p></a>
    <a href="kurumpaa/"><p class="card-presentation-title" style="background-color:beige">#குறும்பா</p></a>
    <br><br>
</div>

<br>

<h2>எல்லா பதிவுகளும்</h2>
<p class="tabs">
    {% for post in site.posts %}
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span class="date">
            {{ post.date | date: "%-d" }}
            {% assign m = post.date | date: "%-m" | minus: 1 %}
            {{ site.data.ta.months[m] }}
            {{ post.date | date: "%Y" }}
        </span>
        {% for tag in post.tags %}
            <span class="tag">#{{ tag }}</span>
        {% endfor %}
        <br>
    {% endfor %}
</p>


<!-- ## List all Tags of site
<ul>
    {% for tag in site.tags %}
        {% assign t = tag | first %}
        {% assign posts = tag | last %}

        <li>{{ t }}</li>
    {% endfor %}
</ul> -->