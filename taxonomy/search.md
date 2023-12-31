---
layout: documentation
sideNavigation: sidenav.taxonomy
title: Taxon
permalink: /taxonomy/search
description: Search the checklist of Fabaceae
klass: fullwidth
lang-ref: species-search
---
You can download the latest version of the Solanceae Source list in .txt (with DarwinCore fields) from the [Catalogue of Life ChecklistBank](https://data.catalogueoflife.org/).

<!--react and gbif component-->
<script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>

<script src="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@{{site.col.version}}/umd/col-browser.min.js" ></script>

<div id="search"></div>

<script >
'use strict';
const e = React.createElement;
class Search extends React.Component {

    render() {

      return e(
        ColBrowser.Search,
        { 
          catalogueKey: '{{site.col.catalogueKey}}',
          pathToTree: '/taxonomy/browse',
          pathToSearch: '/taxonomy/search',
          pathToTaxon: '/taxonomy/taxon/',
          defaultTaxonKey: '{{site.col.defaultTaxonKey}}',
          citation: 'top' 
        }
      );
    }
  }

const domContainer = document.querySelector('#search');
ReactDOM.render(e(Search), domContainer);
</script>
