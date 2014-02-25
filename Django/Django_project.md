# Django Project

# Setup

1. Install Virtualenv
```
sudo apt-get install virtualenv
cd ~/.environments
virtualenv <PROJECT_NAME>env
```

  1.1. Activate your project virtualenv
```
source <your_environment>/bin/activate
. ~/.environments/<your_environment>/bin/activate
```
  or use alternatively the virtualenv wrapper (is quicker)

  1.2. Virtualenv Wrapper

  The [virtuaenv wrapper](http://virtualenvwrapper.readthedocs.org) enables you to quickly cd and activate your project just by typing:
```
workon <PROJECT_NAME>
```
  1.2.1. Install it:
```
sudo pip install virtualenvwrapper
```
  Add to your .bashrc:
```
export WORKON_HOME=~/path/to/your/virtualenvironments
export PROJECT_HOME=~/path/to/your/workspace
source /usr/local/bin/virtualenvwrapper.sh
```
  Restart your bash

  1.2.2. Add a project to the wrapper:
```
cd <PROJECT_NAME>
# Create the virtualenv (or activate it)
mkvirtualenv <PROJECT_NAME>env
# Bind the virtualenv to the existing project
setvirtualenvproject $VIRTUAL_ENV $(pwd)
```
Now you can "workon" your project:
```
workon <PROJECT_NAME>
```

2. Install MySQL
```
sudo apt-get install mysql mysql-server libmysqlclient-dev
```

3. Clone project
```
cd <PROJECTS_FOLDER>
git clone git@server.sinnwerkstatt.com:<PROJECT_NAME>.git
# (ggf. muss vorher der Public-Key übertragen werden)
```

4. Install Dependencies

In your project directory with activated virtual env:
```
pip install -r requirements.txt
# (ggf. muss das Paket MySQL-python manuell nachinstalliert werden:
easy_install -U distribute
pip install MySQL-python
```

5. Create and import Database
```
mysql -u<DB-USER> -p
CREATE DATABASE <PROJECT_NAME>;
```

  5.1. Create empty DB
```
python manage.py syncdb
python manage.py migrate
```

  5.2. Import Live-Database
```
cat <DB-DUMP-DATEI> | mysql -u<DB-USER> -p <DB>
```

6. Create Django settings
```
cd <PROJECT_NAME_APP>
cp example-settings.py settings.py
# In settings.py Datenbank-Einstellungen vornehmen
```

7. Start local server
```
cd <PROJECTS_FOLDER>
~/.environments/<PROJECT_NAME>env/bin/python manage.py runserver
```

# Create a new Django project
Note: project name should contain only letters and numbers (no other symbols)
```
cd <PROJECTS_FOLDER>
django-admin.py startproject <PROJECT_NAME> --template=https://github.com/sinnwerkstatt/django-start-project-zero/archive/master.zip
cd <PROJECT_NAME>
git init # Create an empty git repository or reinitialize an existing one
git add *
git commit -m 'first commit'
git remote add origin <PROJECT_GIT_LINK>
git push -u origin master
```

## Options
* Generate SECRET_KEY and add it as a string to your settings.
```
python -c 'import random; print "".join([random.choice("abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)") for i in range(64)])'
```

# Commit
Git ingore:
* /media (uploads of the clients) - that's why some photos will be missing.

# requirements.txt

The `requirements.txt` file must not contain any of the following dependencies:
* distribute
* setuptools
* wsgiref

Dependencies being installed from a VCS must include an explicit revision description, such as the hash, or a tag (cf. http://www.pip-installer.org/en/latest/logic.html#vcs-support)

# Templates
* ```base.html``` - base template
* ```start.html``` - start page template
* ```page.html``` - CMS page template

## Template Tags
* ```cms_tags``` - http://docs.django-cms.org/en/develop/advanced/templatetags.html
