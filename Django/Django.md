# Django

[Django](https://www.djangoproject.com/) - a high-level Web framework that encourages rapid development and clean, pragmatic design.

## Django project
* See [Django project](Django_project.md)

## Cheat Sheet
* [Mercurytide Cheat Sheets](http://www.mercurytide.co.uk/news/article/django-15-cheat-sheet/) (Django 1.5)

## Install Packages
* Find version: https://pypi.python.org/pypi/
* Django Packages: https://www.djangopackages.com/
* Video: https://www.djangopackages.com/packages/p/django-embed-video/

## CMS
* [Mezzanine](http://mezzanine.jupo.org/)

## Django CMS
Best Practices:
* Test web pages always with "Preview". When the page is ready see it with "Publish".
* [Django cms.key](http://www.slideshare.net/digi604/django-cmskey) - presentation about the show menu template tag and Django CMS.

### User
* [Add additional fields to the standard User](https://gist.github.com/ngeorgiev/6905083)

## Setup

See [Django project setup](https://github.com/sinnwerkstatt/sinnwerkstatt-web/wiki/Django-project#setup).

### PIP
* ``sudo pip install <package_name>`` installs the package globally
* ``pip install <package_name>`` installs the package in the current python context (often in the virtualenv)
* ``pip install -U -r requirements.txt`` Upgrade all packages

## Tutorials
* [Django documentation contents](https://docs.djangoproject.com/en/dev/contents/)
* [Django at a glance](https://docs.djangoproject.com/en/dev/intro/overview/)
* [Models and databases](https://docs.djangoproject.com/en/dev/topics/db/)
* [Handling HTTP requests](https://docs.djangoproject.com/en/dev/topics/http/)

## Style Guides
* [PEP 8 -- Style Guide for Python Code](http://www.python.org/dev/peps/pep-0008/)

## Images
* http://www.sandersnewmedia.com/why/2012/04/16/installing-pil-virtualenv-ubuntu-1204-precise-pangolin/ - fix image showing problem.

## IDEs

### PyCharm
See [[PyCharm]].

## Databases
* Install Databases
 ~/.environments/<PROJEKT>env/bin/pip install -r requirements.txt

## Requirements.txt
On change of the requirements.txt:
* pip install -r requirements.txt
* <ENV> manage.py '''syncdb'''
* <ENV> manage.py '''migrate'''

## Migrations
See [Django migrations](Django_migrations.md).

## Email
See [Django email](Django_email.md)

## Templates
* [Create your own main menu](https://gist.github.com/ngeorgiev/6688779)
* Placement of the sekizai_tags ```addtoblock```
    * should be inside a block to be rendered. If your template extends a file, then you should put it in a block.
    * all the contents of Django CMS plugin templates are rendered by default, so you can place ```addtoblock``` everywhere inside.


## Internationalization
* [How Django discovers translations](https://docs.djangoproject.com/en/1.5/topics/i18n/translation/#how-django-discovers-translations)
* Create or update message files (*.po files):
    * python manage.py makemessages -l de
* Compile (*.po into *.mo files):
    * python manage.py compilemessages -v 2 -l de
* Compile all:
    * bash compilemessages.sh


If you have problems with translating strings:

* read How Django discovers translation https://docs.djangoproject.com/en/1.5/topics/i18n/translation/#how-django-discovers-translations
* Define in your settings.py to make sure that strings are first read from the directory defined by you:
    * BASEPATH = realpath(join(dirname(_file), '..'))
    * LOCALE_PATHS = (
    *     join(BASE_PATH, 'locale'),
    * )
    * Stackoverflow: http://stackoverflow.com/questions/1832709/django-how-to-make-translation-work?rq=1

### Strings
* No ```_(u'A string')```. Use just ```_('A string')```. Reason: Python3 compatibility.

Additionally we should include

```python
from __future__ import unicode_literals
```

## Pagination
* [Step by step source code for adding Django pagination](https://gist.github.com/ngeorgiev/6979190).

### Translations in the Admin
* [django-rosetta](https://github.com/mbi/django-rosetta) - Rosetta is a Django application that eases the translation process of your Django projects.
* [Transifex](https://www.transifex.com/) - ununterbrochene Lokalisierung, die sich in Ihren Entwicklungsprozess integriert. (paid)

## AJAX
* http://www.dajaxproject.com/

## REST
* [Django REST Framework](http://django-rest-framework.org/)
* [Tastypie](http://tastypieapi.org/) - a webservice API framework for Django. It provides a convenient, yet powerful and highly customizable abstraction for creating REST-style interfaces.

## AngularJS
* [django-rest-framework and angularjs](https://www.youtube.com/watch?v=Q8FRBGTJ020)

## Best Practices
* [Django Best Practices](http://lincolnloop.com/django-best-practices/) - a guide to developing and deploying with the Django Web framework.
* [12 tips on Django Best Practices](http://de.slideshare.net/DZPM/12-tips-on-django-best-practices)

## Hosting
* https://code.djangoproject.com/wiki/DjangoFriendlyWebHosts
    * http://locum.ru/public/hosting

## Sites in Django
* [Disqus](http://marakana.com/s/post/1505/learn_how_disqus_does_it_when_it_is_not_django_python_video)
* [Pinterest](http://pinterest.com/)
* http://www.djangosites.org/

## Follow
* [pragmatic startup](https://pragmaticstartup.wordpress.com/)
