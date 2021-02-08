---
# frontmatter goes here
tags: things butter flying .net
---

Excerpt with multiple paragraphs

Here's another paragraph in the excerpt.
<!--more-->

Out-of-excerpt


___using a data.yml which provides alts per photo___
<div class="masonry-grid">
    {% for image in site.data.bf_photos %}
        <figure class="card">
            <img src="\assets\images\bf\{{ image.src }}.jpg" alt="{{ image.alt }}">
            <figcaption>{{ image.alt }}</figcaption>
        </figure>
    {% endfor %}
</div>

_or without data file_
> this method doesn't care about name or type of file
> 
> so we get one bonus!

<div class="masonry-grid">
    {% for image in site.static_files %}
        {% if image.path contains 'images/bf' %}
            <figure class="card">
                <img src="{{ image.path }}" alt="image"/>
                <figcaption>
                    same caption for all...
                </figcaption>
            </figure>
        {% endif %}
    {% endfor %}
</div>