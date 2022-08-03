---
layout: default
permalink: "/search/"
comments: false
search_omit: true
---

<h1>Search</h1>
  <!-- Html Elements for Search -->
<div id="search-container">
    <section class="row">
        <div class="col-sm-12 mt-5 search">
            <input type="text" id="search-input" placeholder="search for something...">
        </div>
    </section>
    <section class="row">
        <div class="col-sm-12 mt-5">
            <div id="results-container" class="row"></div>
        </div>
    </section>
</div>

<!-- Script pointing to search-script.js -->
<script src="{{ site.baseurl }}/assets/js/search.js" type="text/javascript"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  searchResultTemplate: '<div class="col-md-3 mb-5"><div class="card"><a href="{url}"><img class="rounded mb-4" src="{{ site.baseurl }}/{image}" alt="{title}"> </a><div class="card-block"><h2 class="card-title h4 serif-font"><a href="{url}">{title}</a></h2><p class="card-text text-muted">{excerpt}</p></div></div></div>',
  noResultsText: "Ops! No results found!",
  json: '/blog/search.json'
})
</script>