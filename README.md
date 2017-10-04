# practice-docker-postgres10

# how to use 

I try to boot postgresql10 with using docker container.

## 立ち上げ(boot)

```
$ docker run --name pgsql10 -d -e POSTGRES_PASSWORD=password -p 15432:5432 postgres:10
```

## 接続(connect)

```
$ docker run -it --rm --link pgsql10:postgres postgres:10 psql -h postgres -U postgres
```
