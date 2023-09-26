# Task 2

## Create Docker bridge network
```
docker network create -d bridge mynet
```

## Create Docker volume
```
docker volume create data
```

## Pull images
```
docker pull stackupiss/northwind-app:v1
docker pull stackupiss/northwind-db:v1
```

## Run myapp
```
docker run -d \
  --name myapp \
  --network mynet \
  -p 8080:3000 \
  -e DB_HOST='mydb' \
  -e DB_USER='root' \
  -e DB_PASSWORD='changeit' \
  stackupiss/northwind-app:v1
```

## Run mydb
```
docker run -d \
  --name mydb \
  --network mynet \
  --mount type=volume,src=data,dst=/var/lib/mysql \
  stackupiss/northwind-db:v1
```

## Run docker compose
```
docker-compose up -d
```