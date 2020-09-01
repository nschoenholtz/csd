---
title: Home
level: 8
xp: 45400
start: 34000.00
levelup: 48000.00
level_1: 0
level_2: 300
level_3: 900
level_4: 2,700
level_5: 6,500
level_6: 14,000
level_7: 23,000
level_8: 34,000
level_9: 48,000
level_10: 64,000
level_11: 85,000
level_12: 100,000
level_13: 120,000
level_14: 140,000
level_15: 165,000
level_16: 195,000
level_17: 225,000
level_18: 265,000
level_19: 305,000
level_20: 355,000
---

## Introduction

The sun never blinks upon the city of Aynuk, jewel of Jazirat and first of the great migrant cities of the True God. All great deeds begin here, where the wise and brave congregate to seek their fortune. All travels end here, where the ministry of the Lighthouse keep its terrible glow alive.

Brought by visions of lost knowledge to be recovered, treasures to be won, tragedies to prevent -- many airship crews set out, each on a dangerous voyage into the ever-changing wilderness of the splintered lands.

To the patron who sponsors your airship, you are just one more bet in a long ledger. But they must have the blessing of the True God to wear the orange of the plutocracy -- surely you will benefit from their piety?

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
