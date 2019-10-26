# Git Like A Pro

**Disclaimer**  
This conference workshop covers by far not all the nuances which Git offers. The intention of this workshop is to
give you a solid understanding of the concepts and the models of the version control system Git. After this workshop
you will feel comfortable enough to use and further experiment with Git.

## Prerequisites

For this workshop you should bring the following things along:

- A modern laptop (OS: Linux, macOS or Windows10)
- Admin privileges on your laptop!
- Please install all the things described in the Installation procedure below
- A portion of humor and explorer enthusiasm!

## Installation procedure

Please do the following things in order to be ready for the workshop:  
(If you run in any issues with the steps below or you want to give me feedback on how I could improve this guide, please reach out to me at sibebzh@gmail.com)

### Windows

- [Install the latest version of VS Code](https://code.visualstudio.com/Download) and add the [Terminal](https://marketplace.visualstudio.com/items?itemName=formulahendry.terminal) extension
- [Install the latest version of Git for Windows](https://gitforwindows.org)
  - Choose Visual Studio Code as Git's default editor during the installation procedure.  
    (fyi: The Git core.editor will be set in the git config --system properties)
  - Other than that, proceed with the default settings
  - After the installation open up a Git Bash and check with `git --version` if Git returns its version number
- [Install Docker CE](https://docs.docker.com/docker-for-windows/install/)

### macOS

- [Install the latest version of VS Code](https://code.visualstudio.com/Download) and add the [Terminal](https://marketplace.visualstudio.com/items?itemName=formulahendry.terminal) extension
- [Install the latest version of Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03#file-mac-md)
  - After the installation open up a [terminal window](https://www.macworld.co.uk/how-to/mac-software/how-use-terminal-on-mac-3608274/) and do the following things:
    - Check with `git --version` if Git returns its version number
    - Set VS Code as default Git editor by hitting `git config --global core.editor "code --wait"`
  - Optional:
    - If you are using [bash shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), you can install bash Git completion according to [this](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
    - If you are using [Z shell (Zsh)](https://en.wikipedia.org/wiki/Z_shell), you can add [Git completion to Zsh](https://medium.com/@oliverspryn/adding-git-completion-to-zsh-60f3b0e7ffbc)
- [Install Docker CE](https://docs.docker.com/docker-for-mac/install/)

### Linux

- [Install the latest version of VS Code](https://code.visualstudio.com/Download) and add the [Terminal](https://marketplace.visualstudio.com/items?itemName=formulahendry.terminal) extension
- [Install the latest version of Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03#installing-git-on-linux)
  - After the installation open up a [linux terminal](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/) and do the following things:
    - Check with `git --version` if Git returns its version number
    - Set VS Code as default Git editor by hitting `git config --global core.editor "code --wait"`
  Optional:
    - If you are using [bash shell](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), you can install bash Git completion according to [this](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
    - If you are using [Z shell (Zsh)](https://en.wikipedia.org/wiki/Z_shell), you can add [Git completion to Zsh](https://medium.com/@oliverspryn/adding-git-completion-to-zsh-60f3b0e7ffbc)
- [Install Docker CE](https://docs.docker.com/install/)
- [Install docker compose](https://docs.docker.com/compose/install)

### All

- Start the Docker host/daemon on your machine.
- Open a terminal and hit `docker run hello-world:latest` to check if your docker installation is working correctly.
- Git clone or download this repo.
- Open a terminal in the cloned/downloaded repo, navigate into the folder /gitea and execute `docker-compose up -d`  
  (this will pull down the latest Gitea docker image and spin up a container).
- Navigate to [localhost:3000](http://localhost:3000/) in your browser. You should now see the start page of your Gitea installation!
- Click on 'Register' (at the upper right) and finish the SQLite3 database installation by simply clicking the button 'Install Gitea' at the very bottom of the page.

That's it! Now you're armed and ready for the workshop!

From now on each time you start/restart the docker host/daemon on your machine, the Gitea container will be started automatically. Your self-hosted Git remote repository manager will be at your service!

## Further helpful docker commands

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
