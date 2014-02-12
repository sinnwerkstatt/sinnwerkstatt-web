# Web Development Workflow

## Overview of Tools
* [Tooling in the web app development lifecycle](https://secure.flickr.com/photos/kejun/6988320204/)
* [Tooling & the Webapp Development Stack](https://gist.github.com/jonkemp/2713513)
    * [URL's from Paul Irish's talk: Tooling & The Webapp Development Stack](https://gist.github.com/jonkemp/2713513)
* [Frontend development – then, now and the future](https://speakerdeck.com/roka/frontend-development-then-now-and-the-future) ([presentation](http://lecture2go.uni-hamburg.de/veranstaltungen/-/v/15109;jsessionid=EC7B6F2B9C8B73EBADA202B35DA90F41))
* [A Modern Web Designer's Workflow by chriscoyier](https://speakerdeck.com/chriscoyier/a-modern-web-designers-workflow)

## Design Workflow
* [My (Simple) Workflow To Design And Develop A Portfolio Website](http://www.smashingmagazine.com/2013/06/25/workflow-design-develop-modern-portfolio-website/)

## Javascript Development Workflow of 2013
Video: [Javascript Development Workflow of 2013](http://www.youtube.com/watch?v=f7AU2Ozu8eo) by [Paul Irish](http://www.paulirish.com/) ([PDF](http://cdn.oreillystatic.com/en/assets/1/event/83/Javascript%20Development%20Workflow%20of%202013%20Presentation.pdf))
* [A Baseline for Front-End Developers](http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/)

### Shell
* Shell customizations: http://dotfiles.github.io/
* Faves: [z script](https://github.com/rupa/z) (for jumping), server alias
* Siehe [[Terminal]]

### Editor
* learn it well, most important
* Code linting is your first unit test.
* Realtime Feedback
    * live linting
    * live recompilation
    * live reload

### HTML
See [[Html]]

### CSS

#### Icons

* http://fortawesome.github.io/Font-Awesome/
* http://fontcustom.com/

### Images
* Sprites
    * [Spritemapper](http://yostudios.github.io/Spritemapper/)
    * [Glue](http://glue.readthedocs.org/en/latest/quickstart.html)
    * [SmartSprites](http://csssprites.org/) - with Eclipse plugin.
    * [grunt-spritesmith](https://npmjs.org/package/grunt-spritesmith)

### Javascript
* Modules / Dependency management
    * AMD modules
    * CommonJS modules
    * ECMAScript Harmony modules
    * Minispade require ([ember.js example](https://github.com/emberjs/ember.js/blob/80d37171709f213bd16ed5646e3d5c7aeef8c5ec/packages/ember-views/lib/views/states/default.js))
* Tricks:
    * Template precompilation - into functions in a build step and ship the compiled templates.
    * Custom build output based on build-time forks. ([require.js optimizier](http://requirejs.org/docs/optimization.html#hasjs))
    * More module magic from Alex Sexton ([MVC MODULE MAGIC](http://alexsexton.com/talks/backboneconf2012/#/))
* Package Management - cooming soon.
* In-Browser Devtools
    * sourceURL ([Source Mapping](http://www.thecssninja.com/javascript/source-mapping), [Source Mapping Compile Demo](http://www.thecssninja.com/demo/source_mapping/compile.html))
    * source maps - full live debugging on source files with Chrome Dev tools.
    * Navigating scripts
* Mobile
    * Test in Chrome
    * Emulate touches, override device metrics
    * Emulators & [Browserstack](http://www.browserstack.com/)
    * Real device & Adobe Shadow
    * Chrome on Android w/ DevTools

### Testing
* Jasmin, QUnit or Mocha
* Execute tests in a variety of settings:
    * In the Browser
    ** [ Secrets of the Browser Developer Tools](http://devtoolsecrets.com/)
    ** [Chrome DevTools - Authoring & development workflow](https://developers.google.com/chrome-developer-tools/docs/authoring-development-workflow)
    * In a headless browser on-demand via cmd line
    * In a headless browser post-push. Continuous Integration
    ** https://travis-ci.org/ - on every commit - test.
    * In multiple browsers via cmd line
    ** [bunyip](https://github.com/ryanseddon/bunyip) -f test/index.html
    * In multiple browsers ''in the cloud'' via cmd line (e.g. with BrowserStack)
    ** [bunyip](https://github.com/ryanseddon/bunyip) -f test/index.html -b ios
* http://opendevicelab.com/

### Build System # =Issues=
* [Example of Guidelines for contributing an Issue at GitHub](https://github.com/necolas/issue-guidelines/blob/master/CONTRIBUTING.md)
* Create a [Reduced Test Cases](http://css-tricks.com/reduced-test-cases/)

### Grunt
see [[Grunt]]
see [brunch.io](http://brunch.io)

### Bower
see [[Bower]]

### Others
* Resolve your dependency chain
* concatenate
* compile
* flatten your CSS @imports
* Minify
    * Online: http://refresh-sf.com/yui/
* Beautify Javascript:
    * Online: http://jsbeautifier.org/
* Remove debugging statements
* Compress images
    * Online: http://tinypng.org/
* Precompile templates
* Run tests in a variety of environments
* Revs asset paths for caching
* Affirm code quality
* [FireShell](http://getfireshell.com/) - front-end boilerplate and workflows.

## Front-End Development Workflow
* [Front-end Process - Flat Builds and Automation, Part 1: Introduction](http://www.gpmd.co.uk/blog/front-end-process-flat-builds-and-automation-part-1-introduction/)

### After Deployment
#### Client-Side Error Tracking


* [errorception](http://errorception.com/)

### Projects to check out
* [modjs](https://npmjs.org/package/modjs)
* [Grunt](http://gruntjs.com/)
    * http://merrickchristensen.com/articles/gruntjs-workflow.html
* [LiveReload](http://livereload.com/)
* Shadow
* CodeKit
* [Brunch](http://brunch.io/) - recompiler
* WebStorm - unit testing, ...

### Principles
* DRY - Don't Repeat Yourself
    * don't type ./build.sh everytime you save a file
    * don't ftp everytime up you update the site's release branch.
* Learn from other developers.
* Share what you've learned.

## IDEs
* [[PyCharm]]

## Others
* [JavaScript Tooling JSConf. April 2nd. Paul Irish. ](https://dl.dropboxusercontent.com/u/39519/talks/jsconf-tools/index.html)
* [Optimize Your Workflow: JavaScript Tools and Libraries](http://www.joezimjs.com/javascript/optimize-your-workflow-javascript-tools-and-libraries/)
* [Current Workflow: Developing, Linting, Testing and Distributing JavaScript](http://custardbelly.com/blog/2012/02/07/current-workflow-developing-linting-testing-and-distributing-javascript/)
* [Yeoman – Level-up Your Daily Workflow](http://drublic.de/blog/yeoman/)
    * [Yeoman with Addy Osmani](https://www.youtube.com/watch?v=Hl1sp9axHEY)

## Stay Up to Date
* http://uptodate.frontendrescue.org/#addy-osmani
* [Talks To Help You Become A Better Front-End Engineer In 2013](http://www.smashingmagazine.com/2012/12/22/talks-to-help-you-become-a-better-front-end-engineer-in-2013/)
