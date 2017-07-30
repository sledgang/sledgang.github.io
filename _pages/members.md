---
layout: page
title: Members
permalink: /members/
---

> *All handles below are our member's [Discord](https://discordapp.com/) tags.*

{% for author in site.authors %}
---

## [`{{ author[1].name }}#{{ author[1].discord_discrim }}`](https://github.com/{{ author[1].github }})
{% endfor %}
