# Database Migrations

We're using [Flask-Migrate](https://github.com/miguelgrinberg/Flask-Migrate) atop Alembic to automaticaally detect DB model chagnes, create migation scripts, and push them to our server.

The basic steps are:
1. Create database (or enable migrations if it exists)  
    ```$ flask db init	```
1. Generate migration script  
    ```$ flask db migrate	```
1. Review the generated migration script (in the ```migrations``` directory)
1. Apply the migration to the database  
    ```$ flask db upgrade	```
