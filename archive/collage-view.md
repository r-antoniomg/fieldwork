---
title: 'collage'
layout: splash
permalink: 'collage-view'
tag: Collage
header:
  overlay_color: '#008CA3'
---

{% include practice-generated-tag-view.html %}

This is an auto-generated view of objects tagged as '{{ page.tag }}'.

{% assign related_fieldnotes_page = site.data.practice_fieldnotes_pages | where: "tag", page.tag | first %}

{% if related_fieldnotes_page %}
<div class="fw-generated-view-fieldnotes-link">
  <p> If you want to learn more about this topic as part of fieldwork practice, you can explore the curated
    <a href="{{ related_fieldnotes_page.url | relative_url }}">
      {{ related_fieldnotes_page.title }}
    </a> page.
  </p>
</div>
{% endif %}

## {{ page.tag }} gallery

## OLD INCLUDE % include practice-generated-view.html %

<p class="fw-generated-view-back-link">
  <a href="#" onclick="history.back(); return false;">
    ← Return to previous page
  </a>
</p>