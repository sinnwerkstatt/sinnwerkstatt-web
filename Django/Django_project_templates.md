# Django Project Templates

## Sinnwerstatt Requirements
Create a standard Django project template covering 80% of the cases we need. Should cover the values: Productivity and Quality (see [[Quality Guidelines]]).

### Front-end requirements:

#### Livereload.
* [Final Solution!!!](https://github.com/sinnwerkstatt/sinnwerkstatt-web/wiki/Django-livereload)
    * Consider http://livestyle.emmet.io/?
* [Cross Browser CSS Injection](http://css-tricks.com/cross-browser-css-injection/) - works for CSS. HTML changes are not livereloaded.
* http://livejs.com/
* http://stackoverflow.com/questions/19073878/how-to-livereload-django-templates
* [LivePage](https://github.com/MikeRogers0/LivePage) - for [Google Chrome](https://chrome.google.com/webstore/detail/livepage/pilnojpmdoofaelbinaeodfpjheijkbh) reloads website resources (such as CSS, HTML and JavaScript) as they change on the server. Disadvantage: the pull method sends a lot of server requests to check for changes.

#### Others
* Sass
* Minify
* ...
* ...
* Translation: a) add translation in the Django Admin b) Compile automatically changed *.po files into *.mo files
* Images - compress, create sprites: http://addyosmani.com/blog/image-optimization-tools/
* Grunt?
* [[Yeoman]]
* Front-end JavaScript templates: http://jlongster.github.io/nunjucks/ , http://paularmstrong.github.io/swig/ , 
* 404 and 500 pages.
* Client-Side rendering of Django-like template?
    * [Plate](https://github.com/chrisdickinson/plate)
    * [Swig](https://github.com/paularmstrong/swig)
    * or non-django templates: [doT.py](https://github.com/lucemia/doT/)

* requirements.txt
    * distribute?
    * MySQL-python?

### Open Questions
    * multiple settings and requirements files? (as in "Two Scopes of Django")
    * SECRET_KEY as environment variable? (as in "Two Scopes of Django")
    * fabfile settings.

### Implementation
* Internal: http://git.sinnwerkstatt.com/sinnwerkstatt/django-cms-project-template
* GitHub: after the internal implementation is ready.

#### Cookiecutter
* https://github.com/audreyr/cookiecutter
* Install: ```pip install cookiecutter```

## Templates
* https://github.com/strycore/djung
* [django-skel: A Skeleton for Django Projects](http://bixly.com/blog/django-skel-a-skeleton-for-django-projects/)
* https://github.com/audreyr/cookiecutter
    * https://github.com/pydanny/cookiecutter-djangopackage

## Andere
* http://humanstxt.org/
