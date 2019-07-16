# How we search  <!-- .slide: class="extly-slide-style" data-background="#ffa619" -->


## The Classic Search

- Simple search queries<!-- .element: class="small" -->
- Based on a SQL Engine<!-- .element: class="small" -->
- Results composed from separated queries<!-- .element: class="small" -->
- Ordered results by one criteria at a time<!-- .element: class="small" -->
- Integrated with the plugin system<!-- .element: class="small" -->
- Search on form POST (400-800ms)<!-- .element: class="small" -->


## The Smart Search

- Simple Full-text Search queries<!-- .element: class="small" -->
- Based on the SQL engine and indexed facts<!-- .element: class="small" -->
- Results composed from separated queries<!-- .element: class="small" -->
- Ordered results by unique criteria<!-- .element: class="small" -->
- Integrated with the plugin system<!-- .element: class="small" -->
- Search on form POST (400-800ms)<!-- .element: class="small" -->


## The Algolia Search

- Complex Full-text Search queries<!-- .element: class="small" -->
- Based on a NoSQL distributed search engine<!-- .element: class="small" -->
- Powered by managed indexes<!-- .element: class="small" -->
- Integrated with a rich set of widgets<!-- .element: class="small" -->
- Advanced configuration on Algolia's backend<!-- .element: class="small" -->
- Integrated via extensions (For instance, XT Search)<!-- .element: class="small" -->
- InstantSearch, Ajax queries by keystroke (50ms)<!-- .element: class="small" -->


## Algolia in CMS terms <!-- .slide: class="extly-slide-style plain console" -->

- An indexer process
- Indexing events
- Search Modules
  - Based on Algolia Widgets
  - Autocomplete
  - InstantSearch


## Algolia implementation for JED <!-- .slide: class="extly-slide-style plain console" -->

The Algolia Backend Configuration

- Indexes
- Searchable Attributes
- Results Attributes
- Facets
- Ranking System
- [JED Search Cases Docs](https://github.com/joomla/jed-issues/wiki/JED-Search-use-cases-and-definitions)


## Autocomplete Widget <!-- .slide: class="extly-slide-style plain console" -->

    const search= instantsearch(/* parameters */);

    const makeAutocomplete= instantsearch.connectors.connectAutocomplete(
      function renderFn(
          renderOpts: AutocompleteRenderingOptions,
          isFirstRendering: boolean) {
        // render the custom Autocomplete widget
      }
    );

    const  customAutocomplete = makeAutocomplete(instanceOpts: CustomAutocompleteWidgetOptions);
    search.addWidget(customAutocomplete);


## XT Search for Algolia <!-- .slide: class="extly-slide-style plain console" -->

A single solution for Joomla, PrestaShop, and WordPress

![SanJuan Turismo - Autocomplete](images/30-how/XTSearch-for-joomla.png)


## XT Search for Algolia

- A component for data indexation
- Modules
  - Autocomplete<!-- .element: class="small" -->
  - InstantSearch<!-- .element: class="small" -->
  - Browse By Facet<!-- .element: class="small" -->
- Ready for Joomla 3 / 4
- Ready for prestaShop 1.6 / 1.7
- WordPress 5 / WooCommerce (Coming Soon)

[extly.com/xt-search-for-joomla](https://www.extly.com/xt-search-for-joomla.html)