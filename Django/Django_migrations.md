# Django Migrations

See [Django](Django.md).

* [Django database migration tool: south, explained](http://www.djangopro.com/2011/01/django-database-migration-tool-south-explained/)

## Initial migration
* ```python manage.py schemamigration app_name --initial```
* ```python manage.py migrate app_name```

## Normal migration
* Migrate on change of requirements.txt, e.g. new tables are added.
    * ```python manage.py syncdb```
    * ```python manage.py migrate```
* Migrate on model change:
    * ```python manage.py schemamigration app_name --auto```
    * ```python manage.py migrate app_name```

## Other migration commands
* Delete migration
    * ```python manage.py migrate app_name number_of_migration_to_roll_back_to_e_g_0001```
    * delete file
* Fake a migration (Update the South history, without making DB changes)
    * ```python manage.py migrate app_name number_of_migration_to_fake_e_g_0001 --fake```
* List current migrations
    * ```python manage.py migrate --list```
