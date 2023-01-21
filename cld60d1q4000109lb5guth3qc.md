# The Technology Titan Go Language

Go is sure to be a major language in the world of programming for years to come. Created by Google in 2009, Go is a modern, open-source language that is designed for high performance, reliability, and ease of use

## Why GO Programming Language?

Go is considered a key player in the DevOps world. **Docker**, **Kubernetes**, **Prometheus**, **Hugo**, **Grafana** and **Terraform** are all built **on top of Go**.

Concurrency support built into Go makes it simple for developers to create highly performant and efficient systems, which is essential in the DevOps world where speed and reliability are critical.

In this article, I'll walk you through my troubleshooting process for installing Go lang and then running your first project.

Installation

* I downloaded the exe from the internet and installed it, if you wish to install it on Linux, install and extract the [binaries](https://golangdocs.com/install-go-linux).
    
* set env variable, in root, I added this line to `.bashrc`
    

```go
export GOPATH=C:/go-work
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307181891/7e88919c-fc6d-4b98-ad89-9fc87105b2a3.png align="center")

i did it using vim, u can do [nano](https://www.geeksforgeeks.org/nano-vs-vim-editor-whats-the-difference-between-nano-and-vim-editors/) if u wish.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307203752/70e87c1a-0c0f-4f83-b6b9-cda4bebf032e.png align="center")

On windows, u can also type 'edit environment variables' in the start and edit manually.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674339491254/441a4b06-f619-43b3-8bda-5b15a6dfc171.png align="center")

* I added this line to .bash\_profile (create one if you don't have)
    
    `source ~/.bashrc`
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307253235/3648b98f-adeb-43d1-9e02-590b7baebc95.png align="center")

These files are hidden, check them out using:

```bash
ls -a
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307289966/b5ff0ff9-450b-40f0-b9fe-bfe7a2f8411e.png align="center")

### Install checks

* Check if Go installed
    

```go
go version
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307326081/2d053139-b9b5-4e55-96f2-605af9689a9f.png align="center")

* check the env variable:
    

```bash
echo $GOPATH
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307283931/70f79f27-bb2d-4971-953c-5a77bb28f45a.png align="center")

to check all env available write

```go
go env
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307337406/c84e871b-89c0-42a8-8058-36dc8c38a7ae.png align="center")

### Hello world?

* write the code
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307392157/e755987c-7517-4f57-9bce-988feeef86db.png align="center")

* Let's execute the greatest
    

```go
go run filename.go
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674307405098/7bab1e0b-eda9-4af1-a0e4-598b68368595.png align="center")

You should be able to successfully set up your development environment and get started on your first project.

### Advanced Go use-cases

* Building web servers and APIs.
    
* Developing command-line tools and utilities.
    
* Creating concurrent and parallel programs.
    
* Building network services and distributed systems.
    
* Developing serverless functions.
    
* Building and deploying containerized applications.
    
* Developing desktop and mobile applications using GUI libraries.
    
* Building machine learning and data processing pipelines.
    
* Developing blockchain and cryptocurrency applications.
    

All in all, Go is a powerful, efficient, and simple programming language that is suitable for a wide range of applications. The language's simplicity and ease of use make it accessible to developers of all skill levels, and its performance and scalability make it suitable for building large, complex systems.

Go's popularity has been on the rise in recent years, and it has been adopted by many large companies such as Uber, Netflix, and Dropbox, as well as open-source projects such as Kubernetes and Docker.

If you are looking for a new language to try, or if you are interested in building systems, web applications, or network services, Go is definitely worth considering. It is a great choice for your next project and you will not regret giving it a try.

Bonus, check this [Get ChatGPT in Your terminal](https://github.com/gofireflyio/aiac), a go-based project that generates ready-to-use devops code such as terraform configurations, kubernetes manifest files, ansible, dockfiles, and much more with a single command.