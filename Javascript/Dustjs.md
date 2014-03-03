# Dustjs

[LinkedIn's dustjs](http://linkedin.github.io/dustjs/) - аsynchronous templates for the browser and node.js ([demo, by akdubya](http://akdubya.github.io/dustjs/)).

* [GitHub](https://github.com/linkedin/dustjs)
* [Tutorial](https://github.com/linkedin/dustjs/wiki/Dust-Tutorial) ({$idx})
* [Leaving JSPs in the dust](http://engineering.linkedin.com/frontend/leaving-jsps-dust-moving-linkedin-dustjs-client-side-templates)
* [Dustjs Helpers](https://github.com/linkedin/dustjs-helpers) (bower: dustjs-linkedin-helpers)

## Performance
* Development - with the "full" version.
* Production - compile your templates on the server (node.js + dust.js npm module or grunt). Use the "core" version on client. The core version doesn't have the template compiler and is to be used with pre-compiled templates.

## Render server-side

* [grunt-dust-html](https://github.com/ehynds/grunt-dust-html) - this task renders Dust templates against a context to produce HTML.
* [grunt-dust-render](https://github.com/dig3/grunt-dust-render) - Grunt plugin to render dust templates to html.
