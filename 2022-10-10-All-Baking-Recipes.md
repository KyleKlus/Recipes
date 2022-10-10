---
title: All Recipes
created: Tu 22.05.2022, 17:06:11
author: Kyle Klus
categories: Kyles-Cookbook baking forall moc
layout: post_moc
backlink: /Kyles-Cookbook.html
tags: status/not_tree
---
{% assign recipes = site.categories.baking%}
{% assign recipes = recipes | where: "categories", "recipe" %}

{% assign cake = recipes | where: "categories", "cake" %}
{% if cake != blank %}

## Cake

{% for post in cake %}

- [{{post.title}}]({{post.url}})

{% endfor %}
{% endif %}

{% assign pastry = recipes | where: "categories", "pastry" %}
{% if pastry != blank %}

## Pastry

{% for post in pastry %}

- [{{post.title}}]({{post.url}})

{% endfor %}
{% endif %}

{% assign cookies = recipes | where: "categories", "cookies" %}
{% if cookies != blank %}

## Cookies

{% for post in cookies %}

- [{{post.title}}]({{post.url}})

{% endfor %}
{% endif %}

{% assign other = recipes | where: "categories", "other" %}
{% if other != blank %}

## Other nice things

{% for post in other %}

- [{{post.title}}]({{post.url}})

{% endfor %}
{% endif %}