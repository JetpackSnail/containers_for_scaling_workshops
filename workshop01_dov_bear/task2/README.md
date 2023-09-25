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
  -v data:/var/lib/mysql \
  -p 3306:3306 \
  stackupiss/northwind-db:v1
```