# HELM |  The Essential Package Manager for Kubernetes



# A Brief Timeline
If you're working with Kubernetes, you know that it can be challenging to manage and deploy applications on your cluster. **Helm** is a package manager for Kubernetes that makes it easy to manage and deploy complex applications.

- But, i don't know Kubernetes? [Break](https://blog.yahya-abulhaj.dev/kubernetes-the-containers-orchestration-engine)

Helm was originally developed by Deis, a company that provided a platform for deploying and managing applications on Kubernetes. The first version of Helm was released in 2015, and it quickly gained popularity as a tool for managing applications on Kubernetes clusters.

In 2017, Helm was donated to the **Cloud Native Computing Foundation (CNCF)** and became an incubator project. Since then, Helm has continued to evolve and improve, with the release of Helm 2 in 2017 and Helm 3 in 2020.

Helm was designed to be a package manager for **Kubernetes**, similar to package managers like **apt** and **yum** in the Linux world. It allows you to install and manage applications on your Kubernetes cluster using a common set of commands, and it provides versioning and rollback capabilities to help you manage the lifecycle of your applications.

## Understanding Helm
Helm is an open-source tool that helps you manage and deploy applications on your Kubernetes cluster. It allows you to define, install, and upgrade complex Kubernetes applications, known as Helm charts. A Helm chart is a collection of files that describe how to deploy an application on Kubernetes. It includes all the necessary Kubernetes resources to run the application, such as Deployments, Services, and Ingresses. Helm charts are written in YAML and are organized into a directory structure that includes a Chart.yaml file and templates for each of the Kubernetes resources.

## Benefits of Using Helm
There are several advantages to using Helm, and I'll list a few of them below.

1- **Define your application as code:** By using Helm charts, you can define your application as code, making it easier to version control and collaborate with your team.

2- **Consistent deployments:** Helm makes it easy to deploy applications consistently across different environments, such as development, staging, and production.

3- **Streamlined updates:** With Helm, you can easily upgrade your applications by updating the chart's version and applying any necessary changes.

4- **Community support:** Helm is an active open-source project with a large community of contributors and users.

# Mechanism to get you started
To use Helm, you first need to install it on your local machine and on your Kubernetes cluster. Once installed, you can search for and install charts from the official Helm repository, or you can create and publish your own charts.

To create your own chart, you can use the `helm create` command, which will generate the basic directory structure and files for you. Then, you can edit the `Chart.yaml` file to specify the chart's name, version, and dependencies. In the templates directory, you can define the Kubernetes resources that make up your application.

Once your chart is complete, you can use the `helm package` command to create a package, or "tarball," of your chart that can be easily shared and deployed. You can then use the` helm install` command to deploy your chart to your Kubernetes cluster.

To upgrade an existing installation, you can use the `helm upgrade` command, which allows you to update the chart's version and apply any necessary changes to your Kubernetes resources.



## Installation

To install Helm, you will need to have access to a Kubernetes cluster and have the `kubectl` command-line tool installed on your local machine.

1- First, download the Helm binary from the official website: https://helm.sh/docs/intro/install/

2- Extract the Helm binary and move it to a directory in your PATH, such as `/usr/local/bin`/ 

```
tar xvfz helm-v3.4.1-linux-amd64.tar.gz
mv linux-amd64/helm /usr/local/bin/helm

```

3- Initialize Helm by installing Tiller, the server-side component of Helm, on your Kubernetes cluster:

`helm init`

4- Wait for Tiller to be deployed and ready by running the following command:
`kubectl --namespace kube-system wait deploy/tiller-deploy --for=condition=available
`

5- Verify that Helm is installed and working correctly by listing the available charts:

`helm search`

That's it! You have now installed Helm and are ready to start using it to manage and deploy applications on your Kubernetes cluster.



## Helm Chart, The Dive
Helm charts are a way to package and deploy applications to a Kubernetes cluster. They contain all the information needed to create and manage the desired application, including the configuration and dependencies for the application, as well as the Kubernetes resources required to run it.

Charts are written in a declarative language using  the great YAML, which allows you to specify the desired state of your application. This means that you can describe the desired state of your application in a chart, and Helm will take care of creating and updating the necessary Kubernetes resources to achieve that state.

Charts can be customized using values, which allow you to tailor the resources in the chart to your specific needs. For example, you might want to customize the number of replicas for a Deployment, or the port that a Service exposes. You can specify these values in a separate file or pass them in at the command line when you install or upgrade the chart.

Here is an example of a simple Helm chart for deploying a basic web application on Kubernetes:

``` YAML
# Chart.yaml

name: my-web-app
version: 0.1.0
description: A simple web application

# templates/deployment.yaml

apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-web-app
spec:
  replicas: 1
  selector:
    matchLabels:
      app: my-web-app
  template:
    metadata:
      labels:
        app: my-web-app
    spec:
      containers:
      - name: my-web-app
        image: nginx:latest
        ports:
        - containerPort: 80

# templates/service.yaml

apiVersion: v1
kind: Service
metadata:
  name: my-web-app
spec:
  type: LoadBalancer
  ports:
  - port: 80
    protocol: TCP
    targetPort: 80
  selector:
    app: my-web-app

```

This Helm chart defines a Deployment and a Service for a basic web application running on NGINX. The Deployment manages a single replica of the NGINX container, and the Service exposes it to the outside world via a LoadBalancer.

To use this chart, you can package it into a tarball and install it on your Kubernetes cluster using the `helm install` command:

```
helm package my-web-app
helm install my-web-app-0.1.0.tgz
```


You can then check the status of your Deployment and Service using the `kubectl` command-line tool:

```
kubectl get deployment my-web-app
kubectl get service my-web-app
```

To upgrade your application, you can simply package and install a new version of the chart using the `helm upgrade` command:

```
helm package my-web-app
helm upgrade my-web-app my-web-app-0.2.0.tgz


```

That's a basic example of how to use a Helm chart to deploy an application on Kubernetes. 

Winding this up, Helm charts are a convenient and standardized way to manage and deploy applications to Kubernetes. They allow you to define your application in a declarative way, and use **Helm to handle the details of creating and managing the necessary Kubernetes resources**.


For more information, you can refer to the amazing Helm documentation [here](https://helm.sh/docs/)



# To wrap up

On-DevOps, Helm can be used as a tool to automate the deployment and management of applications on a Kubernetes cluster. With Helm charts to define the desired state of an application, developers can version and manage the application in a reliable and reproducible way, and use Helm to automate the process of deploying and updating the application on the cluster. Moreover, this help organizations to speed up their software delivery process and improve the reliability of their applications.

In summary, Helm is a powerful tool for managing and deploying applications on Kubernetes. It makes it easy to define your application as code, and to deploy and upgrade it consistently across different environments. If you're not already using Helm, i highly recommend giving it a try!


