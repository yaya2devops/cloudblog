---
title: "Explaining Packages To A-5Year-Old"
datePublished: Sun Mar 19 2023 20:22:05 GMT+0000 (Coordinated Universal Time)
cuid: clffugcsv000609lb1opo13xd
slug: explaining-packages-to-a-5year-old
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679257217849/52e0051b-2513-45b4-b10d-04a670440774.png
tags: npm, package, node, nkde

---

**Node.js** is a popular runtime environment for executing JavaScript code outside of a browser.

**npm** is the package manager for Node.js, used to install, manage, and share packages of code.

**Docsify** is a lightweight documentation generator that can turn your markdown files into a beautiful website.

## Installing Node.js

### Windows

1. Download the Windows Installer from the [official Node.js website](https://nodejs.org/en/download/).
    
2. Double-click the downloaded file to start the installation wizard and follow the prompts.
    
3. Open Command Prompt and run the following command to check if Node.js is installed:
    

```plaintext
node -v
```

If Node.js is installed, you will see its version number printed to the console.

### MacOs

1. Install Node.js using [Homebrew](https://brew.sh/) by running the following command in Terminal:
    

```plaintext
brew install node
```

1. Alternatively, you can download the Linux Binaries from the [official Node.js website](https://nodejs.org/en/download/).
    
2. Open Terminal and run the following command to check if Node.js is installed:
    

```plaintext
node -v
```

### Linux

1. Install Node.js using your distribution's package manager. For example, on Ubuntu, run the following command:
    

```plaintext
sudo apt-get install nodejs
```

1. Open Terminal and run the following command to check if Node.js is installed:
    

```plaintext
node -v
```

## Install NPM

npm is installed automatically with Node.js.

To check if npm is installed, open Terminal or Command Prompt and run the following command:

```plaintext
npm -v
```

## Installing Docsify

1. Open Terminal or Command Prompt and run the following command:
    

```plaintext
npm install -g docsify-cli
```

1. This command installs Docsify globally on your system, making it available from anywhere in the terminal.
    
2. To check if Docsify is installed, run the following command:
    

```plaintext
docsify -v
```

Congratulations!

You have successfully installed Node.js, npm, and Docsify on your system.

## Get Started with Docisfy

Start a New project:

```plaintext
docsify init your-project
```

Serve it locally:

```plaintext
docisfy serve your-project
```

I built [this](https://istic.computer-engineering.tech/#/) using Docsify.

You can now start to generate your websites.