---
layout: page
title: Book Notes
permalink: /books/
---

From time to time I spiral into what might be considered reading binges.
Usually these last for around a year or two.  I haven't been able to determine
what triggers them nor what causes me take a break for a while and reflect.
You'll know if I'm currently in the middle of one if after a few minutes of
talking I say the phrase, "Oh, That reminds me!  Are you familiar with
``<$AUTHOR>``?!  They did a ``<$NERDY_ADJECTIVE>`` study on
``<$TOPIC_TANGENTIALLY_RELATED_TO_OUR_DISCUSSION>``.  I'm aware that this can
be really annoying and I'm working on that.  In fact, I'm writing this page in
an attempt to avoid more such awkward moments.

<ul>
  {% assign books = site.books | sort: "rating" | reverse %}
  {% for book in books %}
    <li>
      <p>
      <a href="{{ book.url }}">{{ book.title }}</a> By {{ book.author }}<br />
      {% if book.subtitle %}
      <em>{{ book.subtitle }}</em><br />
      {% endif %}
      Rating: {{ book.rating }}/10<br />
      {% if book.takeaway %}
      Takeaway: {{ book.takeaway }}<br />
      {% endif %}
     </p>
    </li>
  {% endfor %}
</ul>
