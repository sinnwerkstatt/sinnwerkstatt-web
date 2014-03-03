# Grunt

[Grunt](http://gruntjs.com/)

## Install

### Requirements
* [Install Node.js and npm](http://nodejs.org/) (download and follow the README)

### Install Grunt
* [Getting Started with Grunt](http://gruntjs.com/getting-started), [How to install grunt and how to built script with it](http://stackoverflow.com/a/15712530/2510374)
    * cd your_project
    * npm install -g grunt-cli
    * npm install grunt --save-dev

## Use in existing Grunt project
* **npm install**
    * read all the module dependencies from package.json and install them from npm software repository into the local folder node_modules.
* **bower install** (optionally)
    * read all dependencies from bower.json and install them from the bower repository into the folder bower_components.
* **grunt**
    * runs the default registered task in Gruntfile.js.


Installing Grunt and gruntplugins:
* npm install <module> --save-dev
    * installs the module locally and adds it to the devDependencies section of package.json, using a tilde version range

## Structure
* '''package.json''' - contains various metadata about an Node Packaged Modules. Project identification and description, project's dependencies, ...
    * dependencies field is used to list all the dependencies of your project that are available on npm
    * devDependencies are dependencies not required for normal operation, but required/recommended if you want to patch or modify the project. E.g. testing framework
    * [package.json - an interactive guide](http://package.json.nodejitsu.com/)
* '''Gruntfile.js''' - defines, loads and configures Grunt tasks.
    * read a good explanation of a [Sample Gruntfile](http://gruntjs.com/sample-gruntfile)

## Grunt plugins
* [grunt-newer](https://github.com/tschaub/grunt-newer) - configure Grunt tasks to run with only those files modified since the last successful run.

## Others
* [concatenate and minify your Javascript and CSS source files](http://www.anujgakhar.com/2013/02/28/writing-a-simple-grunt-task-using-gruntjs/)
* https://npmjs.org/package/grunt-frontend - minify CSS and JS
* [grunt-contrib-jade](https://npmjs.org/package/grunt-contrib-jade) - compiles [Jade](http://jade-lang.com/) html language
    * [Jade Readme Contents](https://github.com/visionmedia/jade#readme-contents)
    * npm install grunt-contrib-jade --save-dev
* [simplemon](https://github.com/mihaifm/simplemon) - Simple file monitor that executes commands whenever a file change occurs
    * simplemon -O jade html_templates jade_templates
* http://livereload.com/
    * https://github.com/gruntjs/grunt-contrib-livereload
    ** Dependency: npm install grunt-contrib-connect https://npmjs.org/package/grunt-contrib-connect

## Create a Grunt plugin
* Follow the steps in [Creating Grunt Plugins](http://gruntjs.com/creating-plugins).
* Debug the Grunt plugin in [your IDE](PyCharm)
* Read the [Grunt API](http://gruntjs.com/api/grunt)

## Workflow
* [Advanced Grunt tooling](http://chrisawren.com/posts/Advanced-Grunt-tooling)
* [More maintainable Gruntfiles](http://www.thomasboyt.com/2013/09/01/maintainable-grunt.html)

See [[Javascript]], [[Bower]]
