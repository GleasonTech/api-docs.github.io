## Develop

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

Aviator is already optimised for adding, updating and removing documentation pages in CloudCannon.

### Usage

* Each section is a different collection, this helps organise your content.
* Set the order of the collections with the position field in collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position in front matter.

### Search

* Add `excluded_in_search: true` to any documentation page's front matter to exclude that page in the search results.
