# tckr
Stock market news tickerizer

## How to run
Build images and spin up containers:
```bash
$ docker-compose up -d --build
```

Run migrations:
```bash
$ docker-compose exec web python manage.py migrate --noinput
```

Stop all containers and remove volumes:
```bash
$ docker-compose down -v
```

Connect Postgresql database:
```bash
$ docker-compose exec db psql --username=tckr --dbname=tckr_dev
```

## How to manage database
```bash
tckr_dev=# \l -- list databases
tckr_dev=# \c tckr_dev -- switch on tckr_dev database
tckr_dev=# \dt -- list of relations
tckr_dev=# \q -- quit
```

Check that the volume was created as well:
```bash
$ docker volume inspect tckr_postgres_data
```
