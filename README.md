# Docker-Commands
### Docker

`sudo docker info`

`sudo docker version`

`sudo docker -v`

Login in [Dockerhub](https://hub.docker.com/)
<br>
`sudo docker login`

List images in your machine
<br>
`sudo docker images`

Download a new image by DockerHub <br>
`sudo docker pull`

Remove images (<b>-f</b> is force)<br>
`sudo docker rmi` <br>
`sudo docker rmi <image-id> -f`

List running containers <br>
`sudo docker ps`

Run a new container <br>
`sudo docker run`

Start Docker <br>
`sudo docker start`  <br>
`sudo docker start -it ubuntu`

Stop Docker <br>
`sudo docker stop` <br>
`sudo docker stop <contaier-id>`

Information about memory, CPU, DISK, ....  <br>
`sudo docker stats`

More informations about Docker  <br>
`sudo docker system df`

Recycle old containers  <br>
`sudo docker system prune`

### nginx

Publish ypour local website in docker

`sudo docker run --name JeanServer3 -P -d -v ~/Desktop/HTML:/usr/share/nginx/html:ro  nginx`

or

`sudo docker run --name JeanServer2 -P -d -v ~/Desktop/HTML:/usr/share/nginx/html nginx`


### Mysql
`sudo docker pull mysql`

`sudo docker run --name db -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 mysql`

`sudo docker exec -it db /bin/bash`

`mysql -uroot -p123456;`

`show databases;`

`create database test;`

`use test;`

`create table users (id INT NOT NULL AUTO_INCREMENT PRIMARY KEY, name TEXT);`

`show tables;`

`insert into users (name) values ('Jean');`

`select * from users;`

### Node - Hello World

node hello application

> const http = require('http');

> const port = 80;

> const server = http.createServer((req, res) => {

>  res.statusCode = 200;

>  res.setHeader('Content-Type', 'text/plain');

>  res.end('Hello World');

> });

> server.listen(port, () => {

>   console.log(`Server running at http://localhost:${port}/`);

> });

<br>

<b>DOCKERFILE</b>

> FROM node:10
> WORKDIR /usr/src/app
> COPY ./ .
> EXPOSE 80
> CMD [ "node","app.js" ]

docker cmd

> docker build -t teste_node_image

> docker run -p 3000:80 -it teste_node_image

<b>To Test</b>

in CMD

> curl -i localhost:3000

> 



