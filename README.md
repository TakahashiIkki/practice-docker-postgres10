# practice-docker-postgres10

# HOW to use
## 立ち上げ(boot)

```
$ docker run --name pgsql10 -d -e POSTGRES_PASSWORD=password -p 15432:5432 postgres:10
```

## 接続(connect)

```
$ docker run -it --rm --link pgsql10:postgres postgres:10 psql -h postgres -U postgres
```
