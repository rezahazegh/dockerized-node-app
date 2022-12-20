# Dockerized Simple Node App
___

## Run app via docker compose (recommended):
Build image and run container

```docker-compose up -d```

Stop container and remove it

```docker-compose down```

## Run app directly by docker:

1- Build image

```docker build -t simple-node-app .```

2- Check if image build successfully. You should see ```simple-node-app``` in the list of images.

```docker image ls```

3- Run container

```docker run -p 3000:3000 --name test-instance -d simple-node-app```

4- Check if container is running 

```docker ps```

5- Stop container

```docker stop test-instance```
___
## .dockerignore
Everything that we add to .dockerignore won't copy to the image.

We added ```**/node_modules``` because ```node_modules``` will be created during building image. 