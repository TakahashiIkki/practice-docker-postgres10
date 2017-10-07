# practice-docker-postgres10.0_jp

# how to use 

I try to boot postgresql10 with using docker container.
I corresponded to Japanese.

## Dockerfileのビルド

```
docker build -t examples/postgres:10.0_jp --no-cache ./
```

## 立ち上げ(boot)

```
$ docker run --name pgsql10_jp -d -e POSTGRES_PASSWORD=password -p 15432:5432 examples/postgres:10.0_jp
```

## 接続(connect)

```
$ docker run -it --rm --link pgsql10_jp:postgres examples/postgres:10.0_jp psql -h postgres -U postgres
```
