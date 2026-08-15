---
layout: single
title: "Hello world!"
date: 2026-07-27
type: fieldnote
permalink: /fieldnotes/hello-world/
tags:
 - Collage
 - Metadata
targets:
 - inquiry
 - making
 - reflection
related: false
---
> '**Fieldnotes** refer to qualitative notes recorded by scientists or researchers in the course of field research, during or after their observation of a specific organism or phenomenon they are studying.'
>
> Fieldnotes. (2026). In _Wikipedia_. [https://en.wikipedia.org/w/index.php?title=Fieldnotes&oldid=1354042789](https://en.wikipedia.org/w/index.php?title=Fieldnotes&oldid=1354042789)

This blog post is primarily meant for the purpose of testing across various fieldwork practice areas (inquiry, making, reflection).

## Inquiry

Guiding questions:
* how do posts in Jekyll (with Minimal Mistakes theme) display and how are they organized based on metadata from the front matter and/or separate `.yml` files and includes?
* what kind of metadata should be included in posts?
* how are they going to be grouped and how will navigation work?
* what customizations are needed to the out-of-the-box theme in order to display things in a way that I like?

### Tests

The pre-set values that can be used for single-image display are:

### size
- small
- medium
- large
- if none specified: keep original image dimensions

### alignment
- left
- center (default)
- right

Below is an example of a single image displayed without additional formatting options:
{% include practice-fieldnote-image.html id='fw-ob-00001' %}

Below is an example of a single image displayed with medium size formatting, and left alignment:
{% include practice-fieldnote-image.html id='fw-ob-00001' size='medium' align='left' %}

Below is an example of a single image displayed with small size formatting, and right alignment:
{% include practice-fieldnote-image.html id='fw-ob-00001' size='small' align='right' %}

### debugging
#### first debugging test
<p>Testing image id: fw-ob-00002</p>

{% assign test_image = site.data.practice_objects | where: 'id', 'fw-ob-00002' | first %}

<p>Found title: {{ test_image.title }}<br />
Found path: {{ test_image.image_path }}</p>

#### second debugging test
<ul>
{% for item in site.data.practice_objects %}
  <li>id = {{ item.id }}</li>
{% endfor %}
</ul>

#### third debugging test

{% include practice-fieldnote-image.html id='fw-ob-00003' %}

#### fourth debugging test

<ul>
{% for item in site.data.practice_objects %}
  <li>
    ID={{ item.id }}
    |
    TITLE={{ item.title }}
  </li>
{% endfor %}
</ul>

#### fifth debugging test

{% include practice-fieldnote-image.html id="fw-ob-00004" %}

{% include practice-fieldnote-image.html id="fw-ob-00004" size="small" %}

{% include practice-fieldnote-image.html id="fw-ob-00004" size="medium" align="left" %}

{% include practice-fieldnote-image.html id="fw-ob-00004" size="large" align="right" %}

## Making

This section highlights some images from the collection in gallery format.

Below is an example of three curated images.

{% include practice-fieldnote-gallery.html ids='fw-ob-00001,fw-ob-00003,fw-ob-00008' %}

Below is an example of six curated images.

{% include practice-fieldnote-gallery.html ids='fw-ob-00001,fw-ob-00002,fw-ob-00003,fw-ob-00004,fw-ob-00005,fw-ob-00006' %}

## Reflection

As scattered as this post is, this is work in progress and a record of my testing so far.