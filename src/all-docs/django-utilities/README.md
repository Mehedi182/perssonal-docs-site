# Django Utilities

### How to delete all the migrations in django 
* remove all migrations file 
```console
find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
find . -path "*/migrations/*.pyc"  -delete
```
* Reinstall Django
```console
pip install --upgrade --force-reinstall Django
```
* Go to psql terminal and select your db
```psql
DROP SCHEMA public CASCADE;
CREATE SCHEMA public;
GRANT ALL ON SCHEMA public TO postgres;
GRANT ALL ON SCHEMA public TO public;
```

### How to delete all table of a app in db
```console
delete from django_migrations where app = "your-app-name"
```

### How to delete/uninstall a app from django project
```console
# This will revert all the migrations for the app and clean the django_migrations table
python manage.py migrate <app_name> zero
Remove app (code, INSTALLED_APPS, urls.py, etc.)
Deploy (python manage.py migrate)
```