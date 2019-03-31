# Git Like A Pro
**Disclaimer**: This workshop covers by far not all the nuances which Git offers. The intention of this workshop is to
give you an overview of the version control system Git and its models.

Please do the following things in order to be ready for the workshop:  
(If you run in any issues with the steps below, please reach out to me at sibebzh@gmail.com.)

* Install git on your machine (see [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git))
    * Configure your Git username and email using the following git commands in a bash shell. These
      details will then be associated with any commits that you create:
        * `git config --global user.name "yourfirstname yourlastname"`
        * `git config --global user.email "youremailadress"`
    * Configure the git editor you want to use according to [this](https://help.github.com/en/articles/associating-text-editors-with-git)
    * (If you're a Linux/macOS user, you can additionally install bash git completion according to [this](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion))
* Install Docker CE on your machine (see [Docker](https://docs.docker.com/install/overview))
    * (If you’re using Linux as OS, please install docker compose according to [this](https://docs.docker.com/compose/install))
* Start Docker on your machine
* Clone or download this repo
* Execute (to pull down the latest images and to start the containers) in the cloned/downloaded
repo: `docker-compose up -d`
* Navigate to http://localhost:3000/ in your browser. You should see the start page of your Gitea installation!
* Click the menu 'Explore' (upper left) and finish the database installation by clicking 'Install Gitea' at the bottom
* Create an account by clicking on the menu 'Register' (upper right)

That's it! Now you're ready for the workshop!

From now on each time you start the docker host on your machine, two new containers (gitea & mysql) will be created
and your self-hosted Git service (repository manager) will be up and running!

### Further helpful commands
* To view the container logs execute: `docker-compose logs`
* To upgrade your installation to the latest release:
    * Stop the running containers: `docker-compose down`
    * Pull the latest images: `docker-compose pull`
    * Start the new containers (the old ones will be removed automatically): `docker-compose up -d`
* If you then want to remove ALL old unused images from your machine type: `docker image prune -a`
(further docs [here](https://docs.docker.com/engine/reference/commandline/image_prune/))
* If you just want to remove some specific dangling images from your machine:
    * Show all downloaded docker images on your machine: `docker images`
    * Remove unused gitea image: `docker image rm <gitea IMAGE ID>`
    * Remove unused mysql image: `docker image rm <mysql IMAGE ID>`
* For further docs see [here](https://docs.gitea.io/en-us/install-with-docker/)

