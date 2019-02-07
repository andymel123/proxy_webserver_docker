# proxy_webserver_docker
Just a test docker environment for isolating a webserver container

I want to prevent (unknown) access from the (legacy) php backend to any third party services 

Run with
docker-compose -up
Access 'localhost' in browser
See the logs of prox (nginx proxy) and webs (apache webserver, legacy)

docker exec -it webs /bin/bash
ping www.google.com -> does not work

docker exec -it prox sh
ping www.google.com -> does work