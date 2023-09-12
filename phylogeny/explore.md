---
layout: compose
lang: en
lang-ref: phylogeny-explorer
title: Phylogeny Explorer
description: |
  This experimental tool allows the user to view occurrence data from the GBIF network aligned to legume phylogeny. This ongoing research and development project builds on its predecessors, [PhyloJive](https://doi.org/10.1093/bioinformatics/btu024) and [PhyloLink](https://doi.org/10.1093/bioinformatics/bty792)
  <div class="feature-cta">
    <a href="#phylogenetic-exploration-of-gbif-data" class="button is-primary" style="text-decoration: none;">Learn more</a>
    <button class="button" onClick="openWidgetInFullscreen()">Fullscreen</button>
  </div>
background: https://inaturalist-open-data.s3.amazonaws.com/photos/250892331/original.jpg
imageLicense: https://www.gbif.org/occurrence/4014939127
height: 50vh
composition: 
  - type: heroImage
  - type: blank
    inlineData: 
      klass: iframe-box
      markdownContent: |
        <iframe id="phylotreeiframe" seamless frameborder="150" src="{{ site.phylo.tool }}/explore?explore={{ site.url | url_encode}}{{ site.phylo.treePath | url_encode}}&template={{ site.url | url_encode}}{{ site.phylo.template | url_encode}}" height = '790' width="1370" style="height: calc(100vh - 68px);" scrolling='yes' ></iframe> 
  - type: pageMarkdown
---

<script>
  var elem = document.getElementById("phylotreeiframe");
  function setIframeTree(name) {
    var treeOptions = {{ site.data.phylogony.trees | jsonify }};
    const queryString = window.location.search;
    const urlParams = new URLSearchParams(queryString);
    var tree = urlParams.get('tree');
    if (tree) {
      const treePath = treeOptions[name || tree] || "{{ site.phylo.treePath }}";
      const src = "{{ site.phylo.tool }}/explore?explore={{ site.url | url_encode}}" + encodeURIComponent(treePath) + "&template={{ site.url | url_encode}}{{ site.phylo.template | url_encode}}";
      elem.src = src;
    }
  }
  setIframeTree();

  function openWidgetInFullscreen() {
    if (elem.requestFullscreen) {
      elem.requestFullscreen();
    } else if (elem.webkitRequestFullscreen) { /* Safari */
      elem.webkitRequestFullscreen();
    } else if (elem.msRequestFullscreen) { /* IE11 */
      elem.msRequestFullscreen();
    }
  }
</script>

## Phylogenetic exploration of GBIF data

A description could go here