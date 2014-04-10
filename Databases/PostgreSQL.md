# PostgreSQL

## Linux Installation
* ```sudo apt-get install libpq-dev python-dev``` (libs to connect to PostgreSQL)
* ```sudo apt-get install postgresql``` (PostgreSQL)
* ```sudo apt-get install pgadmin3``` (Admin)
* ```sudo apt-get build-dep python-psycopg2``` (PostgreSQL dependencies)

### Console:
* ```sudo -u postgres psql```

### Create Database
* ```sudo -u postgres createdb mydb```

### GUI
* ``pgadmin3``

##OSX Installation
http://postgresapp.com/

When Postgres.app first starts up, it creates the $USER database, which is the default database for psql when none is specified. The default user is $USER, with no password.

PostgreSQL ships with a constellation of useful binaries, like pg_dump or pg_restore, that you will likely want to use. Go ahead and add the /bin directory that ships with Postgres.app to your PATH (preferably in .profile, .bashrc, .zshrc, or the like to make sure this gets set for every Terminal session):

```PATH="/Applications/Postgres.app/Contents/Versions/9.3/bin:$PATH"```

Once your path is correctly set up, you should be able to run psql without a host. (If not, check that the correct version is being loaded in the PATH by doing which psql)

Postgres.app creates a PostgreSQL user with your current username ($USER). It also creates a database with this name, which will be the default one psql connects to if you don't specify otherwise.

To create a new database, connect with psql and enter the following:
```CREATE DATABASE your_database_name;```

### Privileges
psql template1
template1=# CREATE USER tester WITH PASSWORD 'test_password';
template1=# GRANT ALL PRIVILEGES ON DATABASE "test_database" to tester;
template1=# \q

## Cheat Sheet
* http://blog.jasonmeridth.com/2012/10/02/postgresql-command-line-cheat-sheet.html

## Setup Server
* https://help.ubuntu.com/community/PostgreSQL#Basic_Server_Setup
