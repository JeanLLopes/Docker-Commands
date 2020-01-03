# Docker-Commands

### nginx

Publish ypour local website in docker

`sudo docker run --name JeanServer3 -P -d -v ~/Desktop/HTML:/usr/share/nginx/html:ro  nginx`

or

`sudo docker run --name JeanServer2 -P -d -v ~/Desktop/HTML:/usr/share/nginx/html nginx`
