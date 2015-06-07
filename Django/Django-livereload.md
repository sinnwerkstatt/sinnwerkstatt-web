You can livereload Django templates, CSS and Javascript files in two steps.

# 1. Install and configure Grunt

* Install [Grunt](https://github.com/sinnwerkstatt/sinnwerkstatt-web/wiki/Grunt)
* Configure Grunt's [watch task with livereload](https://github.com/gruntjs/grunt-contrib-watch#optionslivereload)

```javascript
grunt.initConfig({
    // ...
    watch: {
        options: {
            livereload: true
        },
        livereload: {
            files: ['**/*.html', '**/*.css', '**/*.js']
        }
    }
    // ...
});

grunt.loadNpmTasks('grunt-contrib-watch'); 
	
grunt.registerTask('default', [
    // add all tasks you need including watch
    'watch' 
]);
```

* Run ```grunt```

# 2. Activate Livereload's browser extension

* Install [Livereload](http://livereload.com/) [browser extensions](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-): [Chrome](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei), [Firefox, Safari](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-)
* Open your project in the browser and activate the extension

# Done
That's it. Change your Django files and the opened website will be automatically refreshed.

# Info
Livereloading will only work when both Grunt is running and the browser extension is connected to the server started by Grunt.

# Python
You can also use [Python LiveReload](http://livereload.readthedocs.org/).
