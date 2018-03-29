# Daveweb

This is the code for [davidrodriguez.io](http://davidrodriguez.io)

If you'd like to run this project yourself just create a `.env` file with the
the following:

```
# Used in development for hot-reload of code
PROJECT_PATH=/path/to/proj

DEBUG=True
SECRET_KEY='something_super_secret'

POSTGRES_DB=somedb
POSTGRES_PASSWORD="supertoughpass"

DB_ENGINE=django.db.backends.postgresql_psycopg2
DB_NAME=somedb
DB_USER=user
DB_PASS="supertoughpass"
DB_HOST=db
DB_PORT=5432
```

Then, run `docker-compose up`.


## Info

Currently the site is deployed using `docker-machine` and `docker-compose` but
it can also be deployed using `kubernetes` by creating a kubernetes secret from
the `.env` file and using `daveweb.yaml` to create the required deployments and
services.
