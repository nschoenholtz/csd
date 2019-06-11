---
title: Home
level: 5
xp: 6500
start: 6500
levelup: 14000.00
---

## Introduction

The sun never blinks upon the city of Aynuk, jewel of Jazirat and first of the great migrant cities of the True God. All great deeds begin here, where the wise and brave congregate to seek their fortune. All travels end here, where the ministry of the Lighthouse keep its terrible glow alive.

Brought by visions of lost knowledge to be recovered, treasures to be won, tragedies to prevent -- many airship crews set out, each on a dangerous voyage into the ever-changing wilderness of the splintered lands.

To the patron who sponsors your airship, you are just one more bet in a long ledger. But they must have the blessing of the True God to wear the orange of the plutocracy -- surely you will benefit from their piety?

### Schedule

* Tuesday, 11 June
* Tuesday, 18 June
* Tuesday, 25 June

### Party Level {{page.level}}
{{page.xp}} / {{page.levelup | round}}xp
<div class="progress">
    {% assign start = page.xp | minus: page.start %}
    {% assign end = page.levelup | minus: page.start %}
    <span style="width: {{start | divided_by: end | times: 100}}%"></span>
</div>

{% if site.sessions %}
### Latest Session
{% assign item = site.sessions.last %}
<a href="{{ item.url }}">{{ item.title }}</a>
{% if item.description %}<span class="description">{{ item.description }}</span>{% endif %}
{% endif %}

<a href="{{ '/assets/' | append: 'csd2.pdf' | relative_url }}">Latest Handout</a>
