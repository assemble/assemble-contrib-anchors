# assemble-middleware-anchors [![NPM version](https://badge.fury.io/js/assemble-middleware-anchors.png)](http://badge.fury.io/js/assemble-middleware-anchors)

> Assemble plugin for creating anchor tags from headings in generated html using Cheerio.js.

**Upgrade notice!**: as of v0.2.0, _this middlweare requires Assemble v0.5.0._

## Example
### Before

```html
<h1 id="glyphicons">Glyphicons</h1>
```
### After

```html
<h1 class="docs-heading">
  <a href="#heading-id-name" name="heading-id-name" class="anchor">
    <span class="anchor-target" id="heading-id-name"></span>
    <span class="glyphicon glyphicon-link"></span>
  </a>
  Glyphicons
</h1>
```
Currently the plugin adds [Bootstrap](http://getbootstrap.com/components/#glyphicons) glyphicon classes. If you want to use different classes, find a bug, or have a feature request, [please create an issue](https://github.com/assemble/assemble-contrib-anchors/issues/new)

[![image](https://f.cloud.github.com/assets/383994/1511486/c2414c4e-4aaf-11e3-9c16-30f2993ae2d7.png)](http://assemble.github.io/example-assemble-anchors/components.html#glyphicons)

Visit the [anchors example repo](https://github.com/assemble/example-assemble-anchors).

## Quickstart
In the command line, run:

```bash
npm install assemble-middleware-anchors --save
```

Next, register the plugin with Assemble:

```js
var options = {
  plugins: ['assemble-middleware-anchors', 'other/plugins/*']
};
```

## Options
#### template

Specify a custom template (Underscore/Lo-Dash) to use for anchor markup. This is the default template:

```js
module.exports = [
  '<a href="#<%= id %>" name="<%= id %>" class="anchor">',
  '  <span class="anchor-target" id="<%= id %>"></span>',
  '  <span class="glyphicon glyphicon-link"></span>',
  '</a>'
].join('\n');
```

To use a custom template just specify it in the options as follows:

```js
options: {
  plugins: ['assemble-middleware-anchors'],
  anchors: {
    template: './path/to/custom/template.js'
  }
}
```


Visit the [plugins docs](http://assemble.io/plugins/) for more info or for help getting started.

## Other Assemble plugins
Here are some related projects you might be interested in from the [Assemble](http://assemble.io) core team.

+ [assemble-plugin-blog](https://github.com/assemble/assemble-plugin-blog): Assemble plugin for generating blog pages for posts and archive list pages. 
+ [assemble-plugin-drafts](https://github.com/assemble/assemble-plugin-drafts): Assemble plugin (v0.5.0) for preventing drafts from being rendered. 
+ [assemble-plugin-pagination](https://github.com/assemble/assemble-plugin-pagination): WIP this plugin isn't ready for use! 
+ [assemble-plugin-rss](https://github.com/assemble/assemble-plugin-rss): NOT Published yet! This plugin isn't ready for prime time! Plugin for creating RSS feeds with Assemble, the static site generator for Node.js, Grunt.js and Yeoman.  
+ [generator-plugin](https://github.com/assemble/generator-plugin): Yeoman generator for Assemble plugins.  
+ [grunt-init-assemble-plugin](https://github.com/assemble/grunt-init-assemble-plugin): Generate a plugin for Assemble. 
+ [plugins](https://github.com/assemble/plugins): Collection of contrib plugins maintained by the Assemble core team. 
+ [assemble-contrib-lunr-examples](https://github.com/assemble/assemble-contrib-lunr-examples): Usages examples for assemble-contrib-lunr, a search plugin for Assemble. 
+ [assemble-contrib-markdown](https://github.com/assemble/assemble-contrib-markdown): HEADS UP! This isn't ready for prime time! Convert markdown files to HTML using marked.js. This plugin is an alternative to Assemble's markdown Handlebars helpers. Both are useful in different scenarios. 
+ [assemble-contrib-navigation](https://github.com/assemble/assemble-contrib-navigation): Assemble plugin for automatically generating Bootstrap-style side navigation.  
+ [assemble-contrib-permalinks](https://github.com/assemble/assemble-contrib-permalinks): Permalinks plugin for Assemble, the static site generator for Grunt.js and Yeoman. This plugin enables powerful and configurable URI replacement patterns, presets, uses Moment.js for parsing dates, and much more. 
+ [assemble-contrib-sitemap](https://github.com/assemble/assemble-contrib-sitemap): Sitemap generator plugin for Assemble 
+ [assemble-contrib-toc](https://github.com/assemble/assemble-contrib-toc): Create a table of contents in the generated HTML, using Cheerio.js 
+ [assemble-contrib-toc-example](https://github.com/assemble/assemble-contrib-toc-example): Example for generating a Table of Contents using Assemble. 
+ [assemble-contrib-wordcount](https://github.com/assemble/assemble-contrib-wordcount): Assemble plugin for displaying a word-count on blog posts or pages. 

Visit [assemble.io/assemble-middleware](http:/assemble.io/assemble-middleware/) for more information about [Assemble](http:/assemble.io/) middleware.


## Contributing
Find a bug? Have a feature request? Please [create an Issue](https://github.com/assemble/assemble-middleware-anchors/issues).

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality,
and run `docs` in the command line to build the docs with [Verb](https://github.com/assemble/verb).

Pull requests are also encouraged, and if you find this project useful please consider "starring" it to show your support! Thanks!

## Author

**Brian Woodward**

+ [github/doowb](https://github.com/doowb)
+ [twitter/doowb](http://twitter.com/doowb)


## License
Copyright (c) 2014 Brian Woodward, contributors.  
Released under the MIT license

***

_This file was generated by [grunt-verb](https://github.com/assemble/grunt-verb) on May 14, 2014._
