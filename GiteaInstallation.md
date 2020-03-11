## Install Gitea on your machine

- Start the Docker host/daemon on your machine.
- Open a terminal and hit `docker run hello-world:latest` to check if your docker installation is working correctly.
- Git clone or download this repo.
- Open a terminal in the cloned/downloaded repo, navigate into the folder /gitea and execute `docker-compose up -d`  
  (this will pull down the latest Gitea docker image and spin up a container).
- Navigate to [localhost:3000](http://localhost:3000/) in your browser. You should now see the start page of your Gitea installation!
- Click on 'Register' (at the upper right) and finish the SQLite3 database installation by simply clicking the button 'Install Gitea' at the very bottom of the page.

From now on each time you start/restart the docker host/daemon on your machine, the Gitea container will be started automatically. Your self-hosted Git remote repository manager will be at your service!

### Further helpful docker commands

- To view the container logs execute: `docker-compose logs`
- To upgrade your Gitea installation to the latest release:
  - Stop the running container: `docker-compose down`
  - Pull the latest image: `docker-compose pull`
  - Create and start two new container (the old one will be removed automatically): `docker-compose up -d`
- If you want to remove ALL old unused images from your machine use: `docker image prune -a`
  (further docs [here](https://docs.docker.com/engine/reference/commandline/image_prune/))
- If you just want to remove some specific dangling images from your machine:
  - Show all downloaded docker images on your machine: `docker images`
  - Remove unused gitea image: `docker image rm <gitea IMAGE ID>`
  - Remove unused mysql image: `docker image rm <mysql IMAGE ID>`
- For further docs see [here](https://docs.gitea.io/en-us/install-with-docker/)