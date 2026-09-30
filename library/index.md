---
layout: default
title: The Library
---

# Inside the library

Welcome.

___
# About Adaptations

## From magazines publications

The purpose is to adapt stories published in old magazines into Twine format. I'm beginning with French publications because it's my country of origin and they're relatively easy to find.

I deliberately use the paragraph number as the paragraph name, so you stay oriented as you would in the paper version.


## from video games

I'm adapting classic text adventure games from the 1980s into Twine. These were games where players had to type the correct syntax to progress and achieve their objectives.

For my adaptations, I enhance the original descriptions to create a richer, more immersive experience. Rather than requiring precise command syntax, I offer contextual choices based on what the player currently has in their inventory. This makes the gameplay more intuitive while preserving the spirit of the original games.

The game maps remain faithful to the originals, maintaining the same layout and structure that players remember from the classic versions.


___
# The content

{% assign magazines = site.pages | where_exp: "page", "page.url contains 'magazines'" %}
{% assign computers = site.pages | where_exp: "page", "page.url contains 'computers'" %}
{% assign tips = site.pages | where_exp: "page", "page.url contains 'tips'" %}

## Magazines

{% for page in magazines %}
  {% if page.url contains 'index' == false %}
    {% assign title = page.title | default: page.name | replace: '.md', '' %}
    - [{{ title }}]({{ page.url | replace: '.md', '.html' }})
  {% endif %}
{% endfor %}

## Computers

{% for page in computers %}
  {% if page.url contains 'index' == false %}
    {% assign title = page.title | default: page.name | replace: '.md', '' %}
    - [{{ title }}]({{ page.url | replace: '.md', '.html' }})
  {% endif %}
{% endfor %}

## Tips

{% for page in tips %}
  {% if page.url contains 'index' == false %}
    {% assign title = page.title | default: page.name | replace: '.md', '' %}
    - [{{ title }}]({{ page.url | replace: '.md', '.html' }})
  {% endif %}
{% endfor %}
