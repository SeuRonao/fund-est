---
title: Listas de Exercícios
toc: false
---
{% assign list = site.data.exercises | sort: "order" %}
{% for item in list %}
- [{{ item.title }}]({% link {{ item.url }} %}){% endfor %}
