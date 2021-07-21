# Jenkins-lts

## Contenedor Jenkins

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Jenkins_logo_with_title.svg/1280px-Jenkins_logo_with_title.svg.png">

## docker-compose.yml ultima version estable

``` bash
version: '3'
services:
  jenkins:
    container_name: jenkins
    image: jenkins/jenkins:lts
    user: root
    restart: always
    ports:
      - "8080:8080"
      - "50000:50000"
    volumes:
      - $PWD/jenkins_home:/var/jenkins_home
      - /var/run/docker.sock:/var/run/docker.sock
    networks:
      - net
networks:
  net:

```

