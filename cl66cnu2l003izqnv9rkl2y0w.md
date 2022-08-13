# Git/GitHub Workflow in 80 seconds
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1659018589276/oxgGf-iav.gif?w=1600&h=840&fit=crop&crop=entropy&auto=format,compress&gif-q=60&format=webm">

> This article began with the intention of demonstrating that Git and GitHub are not the same thing.

## From Linux to today
Linux has revolutionized using only the command line, as evidenced by the fact that the user interface we have today as a default was only a feature available to administrators a decade ago and scarcely employed. 
<br> **Mastering the command line is one of the most powerful things you can do.**

## Set up your Git Terminal
> After installing [Git](https://git-scm.com/downloads)

### 1- Get Git to know you
Run the following commands.

- `git config --global user.name "FIRST_NAME LAST_NAME"`<br>
- `git config --global user.email "MY_NAME@example.com"`
 
### 2- Get Secured (Public Key)
This step varies from repo hoster to another, but it is mostly the same.
You must generate a public key from your local terminal and save it to your repository hoster.

Run the following commands.
- `ssh-keygen -t rsa -b 2048 -C "email@example.com"`
> Click Enter instantly => Type parraphrase Twice => Done!

Now copy the Pk using this command(windows):
- cat ~/.ssh/id_ed25519.pub | clip

**Perfect**, GO to your repo hoster and paste the SSH key, along with a descriptive name!
For further details, you can consult the excellent [GitLab documentation](https://docs.gitlab.com/ee/user/ssh.html).

**Note**
For an improved algorithm you can run the following commands then copy again.
- `ssh-keygen -o -f ~/.ssh/id_rsa`<br>
- ` ssh-keygen -o -t rsa -b 4096 -C "email@example.com"`

##  [82 Seconds Workflow](https://www.youtube.com/watch?v=qwO_X6h8rVM)😆
I've included a brief video describing the Git/GitHub workflow. <br>**Please read the information provided below to make the most of it.**


# Prerequisite
## Linux Commands
- `mkdir <FolderName>`: Stands for Make a Directory, create a new folder.<br>
- `cd <FolderName>`: Move to the below folder. <br>
-  `pwd`: Where am i? Print the working directory. <br>
- `ls`: What is in the current folder?. <br>
- `touch <filename>`: Create a new file.

> [more Linux Commands](https://cheatography.com/davechild/cheat-sheets/linux-command-line/)

## Git 

### What is Git
Git is the most popular version control system. It keeps track of the changes you create to files so you can go back in time if required. It also aids collaborative efforts by enabling various people's changes to be merged into a particular source code.
####  So  What is a Git Repository
 It's simply a location where you keep and store your git belongings locally. Allowing the creation of a history over time.
### Git commands
> [What's GitHub ?](https://blog.yahya-abulhaj.dev/notlocalhost-or-free-hosting-and-serverless-services#heading-hosting-a-website)

- `git init`: Initizalize your local git repository. <br>
- `git add <filename>` : add the files/changes to the git repository<br>
- `git add .` : Add **all of the files** and changes in the directory to the git repo <br>
- `git commit -m "Your amazing message here"` : Before pushing, commit changes.<br>
- `git remote add origin <URL from your repository's hosting service>`:  Connect your local git repository to a remote hosting repository such as github, gitlab, or any other.<br>
- `git push -u origin <ur branch name>`Go ahead and push your great stuff!

> [More Git Commands](https://education.github.com/git-cheat-sheet-education.pdf)


# Get Started Workflow

- Navigate to the desired directory using `cd`
- Once you've arrived, make a project folder with `mkdir`
- Transmit to the new project using `cd`
- Create the files you want once you are there by using `touch`
- `code .` to edit your work in VS Code, save it, and then return to the terminal
- Create your git repository using `git init`
- Add your current files to the git repository `git add .`
- It's time to commit your modifications by using the `git commit`
- Connect your git repository to the external repository `git remote`
- `Push` and observe the magic.




**B**ig things happen of a simple start. Get your workflow on, create your inspiration, and show it off.

> Bonus, each project should include a README file as a best practice.

