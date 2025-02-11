---
lang-ref: home
layout: home
title: Solanaceae Source
description: A global taxonomic resource for the nightshade family
background:  "{{ site.data.images.datura.src }}"
imageLicense: "{{ site.data.images.datura.caption }}"
height: 60vh
cta:
  - text: Occurrence Data
    href: /occurrence/search
  - text: Taxonomy
    href: /taxonomy/browse
  - text: Phylogeny
    href: /phylogeny/explore
  - text: About
    href: /about
    isPrimary: true
permalink: /
composition:
  - type: heroImage # the block type
  - data: home.stats
    type: stats
  - type: latestPosts
    data: we_do_not_want_any_header # weird hack as the block layout looks for a data element and falls back to the page if none is present
parallax: true
---


