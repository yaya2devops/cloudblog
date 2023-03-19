---
title: "Explaining Packages To A-5Year-Old"
datePublished: Sun Mar 19 2023 20:22:05 GMT+0000 (Coordinated Universal Time)
cuid: clffugcsv000609lb1opo13xd
slug: explaining-packages-to-a-5year-old
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679257217849/52e0051b-2513-45b4-b10d-04a670440774.png
tags: npm, package, node, nkde

---


In this [video](https://youtu.be/ZfuSs_g1jTs) we primiarly disscued three main technologies.

**Node.js** is a popular runtime environment for executing JavaScript code outside of a browser.  
  
**npm** is the package manager for Node.js, used to install, manage, and share packages of code.  
  
**Docsify** is a lightweight documentation generator that can turn your markdown files into a beautiful website.

## Installing Node.js

### Windows

1. Download the Windows Installer from the [official Node.js website](https://nodejs.org/en/download/).
    
2. Double-click the downloaded file to start the installation wizard and follow the prompts.
    
3. Open Command Prompt and run the following command to check if Node.js is installed:

```
node -v
```

If Node.js is installed, you will see its version number printed to the console.


### MacOs

1. Install Node.js using [Homebrew](https://brew.sh/) by running the following command in Terminal:
```
brew install node
```

2. Alternatively, you can download the Linux Binaries from the [official Node.js website](https://nodejs.org/en/download/).

3. Open Terminal and run the following command to check if Node.js is installed:

```
node -v
```


### Linux

1. Install Node.js using your distribution's package manager. For example, on Ubuntu, run the following command:

```
sudo apt-get install nodejs
```

2. Open Terminal and run the following command to check if Node.js is installed:

```
node -v
```

## Install NPM

npm is installed automatically with Node.js. 

To check if npm is installed, open Terminal or Command Prompt and run the following command:

```
npm -v
```

## Installing Docsify


1. Open Terminal or Command Prompt and run the following command:

```
npm install -g docsify-cli
```

2. This command installs Docsify globally on your system, making it available from anywhere in the terminal.

3. To check if Docsify is installed, run the following command:

```
docsify -v
```

Congratulations! 

You have successfully installed Node.js, npm, and Docsify on your system. 

## Get Started with Docisfy


Start a New project:

```
docsify init your-project
```

Serve it locally:

```
docisfy serve your-project
```

I built [this](https://istic.computer-engineering.tech/#/) using Docsify.

You can now start to generate your websites.











