---
title: Docker 에서 MongoDB 이용하기
date: 2018-03-08 14:59:24
categories:
    - dev
    - docker.log
tags:
    - docker
    - mongodb
thumbnail:
---

### Mongo 검색

Command 이용해서 검색하거나 

[Docker Hub](https://hub.docker.com/) 에서 `mongo` 를 검색합니다.

command 검색: 

```
docker search mongo
```

![](/images/dev/docker.log/docker-mongodb.png)


### 이미지 받기 및 실행

```
docker pull mongo
```
위 명령어 없이 `run` 명령어 사용하면 자동으로 다운받고 실행을 합니다.


```
docker run --name mongo -p 27017:27017 -d mongo
```
위 명령어를 사용하면 `mongod`가 기동이 됩니다.


### Docker Container 접속

```
docker exec -it mongo /bin/bash
```
위 명령어 실행하면 컨테이너 안으로 들어가서 해당 명령어를 실행합니다.


만일 `run` 하면서 바로 접속하고 싶으면 다음과 같이 해도 됩니다.
```
docker run -it --name mongo -p 27017:27017 -d mongo /bin/bash
```

