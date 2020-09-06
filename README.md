# Git Like A Pro For Beginners / Git Foundations

**Disclaimer**  
This workshop covers by far not all the nuances which Git offers. The intention of this workshop is to
give you a solid foundation of the concepts and the models of the version control system Git. After this workshop
you will feel comfortable enough to use and further experiment with Git.

## Learning Outcomes
After this workshop you will be ready and armed to:
### Git Foundations (1.5h - 2h)
- Install and configure Git on a machine
- Describe the fundamental concepts of Git
- Create you first commit and push it to a remote repository
### Git Like A Pro For Beginners (4h - 8h)
- To do all the things from the Foundations workshop
- Use the basic Git commands like init, add, commit and push with confidence
- Use the following new cool stuff which is not part of my freely available Test Automation University course:
  - Switch
  - Aliases
  - Workshop specific Git Remote Repository manager
- Apply the basic Git concepts at work and in private projects
- Compare different branching and merge strategies

## Prerequisites
For this workshop you should bring the following things along:

- A modern laptop (OS: Linux, macOS or Windows10 (Pro/Enterprise/Education version))
- Admin privileges on your laptop!
- Please install all the things described in the Installation procedure below
- A portion of humor and explorer enthusiasm!

### If you join the online version of this workshop
- Webcam: All participants keep their webcam on for the whole duration of the workshop, if the online tool supports it. This will enhance the quality of the communication and of the workshop as a whole. You won’t be sitting at your desk and just watching slides. You’ll be engaged activities for the majority of the time... almost as if we were in a real classroom.
- Microphone: Please make sure to have a proper microphone in place. Please mute yourself when you are not talking, others will thank you.

## Installation procedure
Please do the following things in order to be ready for the workshop:  
(If you run in any issues with the steps below or you want to give me feedback on how I could improve this guide, please reach out to me at sibebzh@gmail.com)

### Windows
- [Install the latest version of VS Code](https://code.visualstudio.com/Download).
- [Install the latest version of Git for Windows](https://gitforwindows.org)
  - Choose Visual Studio Code as Git's default editor during the installation procedure.  
    (fyi: The Git core.editor will be set in the git config --system properties)
  - Other than that, proceed with the default settings.
  - After the installation open up a Git Bash and check with `git --version` if Git returns its version number.

### macOS
- [Install the latest version of VS Code](https://code.visualstudio.com/Download).
- [Install the latest version of Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03#file-mac-md).
  - After the installation open up a [terminal window](https://www.macworld.co.uk/how-to/mac-software/how-use-terminal-on-mac-3608274/) and check with `git --version` if Git returns its version number.

### Linux
- [Install the latest version of VS Code](https://code.visualstudio.com/Download)
- [Install the latest version of Git](https://gist.github.com/derhuerst/1b15ff4652a867391f03#installing-git-on-linux)
  - After the installation open up a [linux terminal](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/) and check with `git --version` if Git returns its version number.

    

That's it! Now you're armed and ready for the workshop!

### Optional
If you are a macOS/Linux user, you can optionally set Bash/Zsh auto completion:  
  - If you are using [bash shell](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>), you can install bash Git completion according to [this](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)  
  - If you are using [Z shell (Zsh)](https://en.wikipedia.org/wiki/Z_shell), you can add [Git completion to Zsh](https://medium.com/@oliverspryn/adding-git-completion-to-zsh-60f3b0e7ffbc)
