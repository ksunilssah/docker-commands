# Docker Commands

Get list of running container
`docker ps`

Get list of running and stoped container

`docker ps -a`

Stop running container

`docker stop contaier-name`

Get list of images

`docker images`

Downlaod image only

`docker pull imagename`

Remove images

`docker rmi image-name`

Remove container

`docker rm container-name`

To see the logs when container running in detach mode.

`docker container logs container-id or container-name`

List all the running containers

`docker container ls`

Delete container

`docker container rm container-id's`

See the process running under container

`docker container top  container-id or name`

Build images on local

`docker image build -t image-name:version .`

publish image in docker hub

`docker tag local-image:tagname new-repo:tagname`
and
`docker push new-repo:tagname`

Run image on port

`docker run -p 8080:8080 imagename`

Run images in detached mdoe

`docker run -d image-name`

Run nginx in docker container on port 8080

`docker container run --publish 80:80 nginx`

To stop the container on Mac press CTL + C or run stop command and pass container-id first 3 digits

`docker container stop container-id`

Run nginx in ditach mode or in background.

`docker container run --publish 80:80  --detach nginx`

Get container details

`docker inspect containernmae`

Containers logs

`docker logs containername`

Map volme in container

`docker run -p 8080:8080 -v /app/data:/image-default-data-path imagenmae`

Or

`docker run -p 8080:8080 -v "$(pwd)":/app -v /app/node_modules imageName`

##Docker compose

Run docker compose
`docker-compose up`

Stop docker compose
`docker-compose down`

Stop and remove all the data
`docker-compose down -v`

Run postgreySql image with volume mount for data persistence
`docker run --name postgresContainer -e POSTGRES_PASSWORD=1234 -p 5432:5432 -v /Users/sunil/Documents/Learning/git/database/postgreySql/db1:/var/lib/postgresql -d postgres:latest`

Stop running container
`docker stop container-name`

Start stopped container
`docker start container-name`
