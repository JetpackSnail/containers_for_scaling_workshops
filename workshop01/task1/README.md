# Workshop 01

## Build
```
docker build -t <USERNAME>/workshop01:1.0.0 .
```

## Run
```
docker container run -d -p 8080:3000 <USERNAME>/workshop01:1.0.0
```
Open [link](http://localhost:8080)

## Push
```
docker push <USERNAME>/workshop01:1.0.0
```
