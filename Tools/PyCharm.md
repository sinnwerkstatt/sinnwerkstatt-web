# PyCharm

https://www.jetbrains.com/pycharm/ is a Python and Django IDE

* [Features](https://www.jetbrains.com/pycharm/features/index.html)
* [Reference Card / Shortcuts](https://www.jetbrains.com/pycharm/docs/PyCharm_ReferenceCard.pdf)
* [Roadmap](http://confluence.jetbrains.com/display/PYH/PyCharm+development+roadmap)

## Use
* [Speed Tricks by John Lindquist](https://www.youtube.com/watch?v=ATPqj94ctLs)
    * Alt + Space + Space - shows all intended files.
    * Cyclic Expand Word - see shortcut in the keymap settings
    * Ctrl + Alt + Home - go to Related Files, go back with Show Usages.
    * Open "Enter file name" and type "ve\js" - this searches all "js" files within a directory that contains the string "ve"
* [AceJump](http://johnlindquist.com/2012/08/14/ace_jump.html) -> Ctrl + , and chose a character for jump
* [Get out of my way](https://www.youtube.com/watch?v=GEwjDeof1ak) - hide unneeded UI elements.
    * View-> hide the toolbars
* [File Templates](https://www.youtube.com/watch?v=DvwwbMTK0N8), [Live Templates](https://www.youtube.com/watch?v=ZxaVNGSax80)

## Django Debugging
* Settings-> Python interpreters - add the virtualenv python.
* In the (new) Django Debug Configuration: [DJANGO_SETTINGS_MODULE](http://stackoverflow.com/a/14428951/2510374) = project.settings

## Settings

### Browsers
* Settings->Web Browsers
    * /usr/bin/chromium-browser

### Navigation
* [Show line numbers](http://stackoverflow.com/a/15781866/2510374)

### Spelling
* [Add dictionary](https://chukovskij.wordpress.com/2010/04/27/install-russian-spellchecker-dictionary-for-intellij-ide/)

## Virtualenv
* [Establishing Dev environment with PyCharm + Virtualenv for Django development](http://garmoncheg.blogspot.de/2012/01/establishing-dev-environment-with.html)
    * You need to select "Python Interpreter" in those preferences panel and press "Add New" > "Select other" in the top right corner. After that you need to point out to your "virtual-environment directory > bin > Python executable". PyCharm will scan for environment and connect it to where needed.

## Databases
* [Pycharm Setting up Mysql Database Driver](http://stackoverflow.com/questions/14302887/pycharm-setting-up-mysql-database-driver)
    * e.g. DB URL: jdbc:mysql://localhost/databasename
* [Database Tools and SQL Support in IntelliJ IDEA](https://www.youtube.com/watch?v=P3C0iO1yqhk)

#v Debugging

### Node.js
* Read [Running and Debugging Node.js](https://www.jetbrains.com/pycharm/webhelp/running-and-debugging-node-js.html)
* [Install the Node.js plugin](https://www.jetbrains.com/pycharm/webhelp/running-and-debugging-node-js.html), enable it and restart PyCharm

### Grunt
See [Remote Debugging a Grunt plugin in WebStorm](http://habrahabr.ru/post/170441/).
* In your Terminal:
    * cd <path to Gruntfile>
    * node --debug-brk=64005 $(which grunt) your_task_name
* In PyCharm:
    * Run → Edit configurations… → + → Node JS Remote Debug. Add Debug port: 64005
    * Add a breakpoint and run the Debug configuration.

See also [local debugging hints from StackOverflow](http://stackoverflow.com/questions/17043484/grunt-debugging-from-webstorm).
