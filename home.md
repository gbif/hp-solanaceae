---
lang-ref: home
layout: home
title: Solanaceae Source
description: A global taxonomic resource for the nightshade family
background:  "{{ site.data.images.solanum.src }}"
imageLicense: "{{ site.data.images.solanum.caption }}"
# background: /assets/images/Solanum_rostratum_IMG_0547.jpg
# imageLicense: |
# *Solanum rostratum* Dunal (photo by S.Knapp licensed under CC-BY-NC)
height: 80vh
cta:
  - text: Occurrence Data
    href: /occurrence/search
  - text: Taxonomy
    href: /taxonomy/species-list
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


