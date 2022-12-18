# KUBERNETES | The Containers Orchestration Engine

# What's KUBERNETES

Kubernetes is a container orchestration system that provides basic mechanisms for deployment, maintenance, and scaling of applications. Kubernetes also known as k8s was originally designed by Google and is now maintained by the Cloud Native Computing Foundation.

Ensure you reviewed my previous article on [Docker](https://blog.yahya-abulhaj.dev/containers-docker-or-what-exactly-is-that) to get knowledge neat.

Kubernetes has become popular in recent years due to its ability to manage complex deployments on top of scalable infrastructure. Many companies have started using Kubernetes to orchestrate their containerized workloads because it can help them save time and money on operations costs.

# K8S & DevOps

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671297443052/XOgdY_-uW.png)

Kubernetes is an important tool for DevOps teams that are looking to streamline the process of deploying and managing containerized applications at scale. By automating many of the tasks associated with these processes, Kubernetes can help reduce the amount of time and effort required to manage large-scale deployments. Speed, ladies and gentlemen. Additionally, Kubernetes provides a number of features that can help ensure high availability and performance levels for applications running in production environments. **Quality.**

Kubernetes is a powerful and essential tool for DevOps teams that need to deploy and manage applications at scale. It provides a consistent and reliable environment for running applications, and offers a range of tools and features that can help devops teams manage and monitor their applications effectively.

# Architecture

Kubernetes has a decentralized architecture that is made up of a number of components that work together to form a cluster. At a high level, the architecture of Kubernetes can be divided into two main parts: the control plane and the worker nodes.

The control plane is the central management component of the Kubernetes cluster. It is responsible for maintaining the desired state of the cluster and ensuring that the worker nodes are in sync with that state. The control plane consists of a number of components, including:

*   **The Kubernetes API server:** This is the central control plane for the Kubernetes cluster and is responsible for managing the state of the cluster and handling requests from clients.
    
*   **The etcd distributed key-value store:** This stores the configuration data for the cluster and is used by the API server to store and retrieve data about the cluster.
    
*   **The scheduler:** This component is responsible for scheduling pods (a group of one or more containers that are deployed together) onto the worker nodes.
    

Worker nodes are the machines (either physical or virtual) that run the applications and services in the cluster. Each worker node runs a number of components, including:

*   **The kubelet:** This is a process that runs on each node and is responsible for starting, stopping, and managing the containers on that node.
    
*   **The kube-proxy:** This is a network proxy that runs on each node and is responsible for networking and load balancing across the nodes in the cluster.
    
*   **Container runtime:** This is the software that is responsible for running the containers on the node. Kubernetes supports a number of different container runtimes, including Docker, containerd, and CRI-O.
    

In a typical Kubernetes deployment, there is a single control plane that manages a number of worker nodes. The control plane and the worker nodes communicate with each other through the Kubernetes API, which is exposed by the API server. Applications and services are deployed onto the worker nodes as pods, which are scheduled and managed by the control plane.

Overall, the architecture of Kubernetes is designed to be flexible and scalable, with a decentralized control plane that can manage a large number of worker nodes running a wide variety of applications and services.

# Critical Elements

There are many important concepts and features in Kubernetes, but some of the most crucial elements to understand are:

*   **Pods:** Pods are the basic building blocks of Kubernetes, and they represent a group of one or more containers that are deployed together. Pods are the smallest deployable units in Kubernetes and are used to host applications and services.
    
*   **Deployments:** Deployments are used to manage the lifecycle of pods, including scaling and rolling updates. Deployments allow you to declaratively specify the desired state of your applications, and Kubernetes will ensure that the pods are running as intended.
    
*   **Services:** Services are used to expose a set of pods to other parts of the cluster or to external clients. Services provide load balancing and service discovery for the pods they expose.
    
*   **Namespaces:** Namespaces are used to partition resources in a Kubernetes cluster and are often used to separate different environments (e.g. production, staging, development) or teams.
    
*   **RBAC: Role-based access control (RBAC)**: is used to control access to the Kubernetes API and resources within the cluster. RBAC allows you to specify who has access to what resources and what actions they can take.
    

## Ways to install Kubernetes

Installing Kubernetes can seem like a daunting task, especially if you are new to the platform. However, there are a number of ways to get started with Kubernetes, depending on your needs and the resources available to you. Here are a few options for installing Kubernetes:

1- **Use a managed Kubernetes service:** If you don't want to worry about setting up and maintaining your own Kubernetes cluster, you can use a managed Kubernetes service such as Google Kubernetes Engine (GKE), Amazon Elastic Container Service for Kubernetes (EKS), or Azure Kubernetes Service (AKS). These services provide a fully managed Kubernetes environment, allowing you to focus on building and deploying your applications.

2- **Use a local development environment:** If you want to get started with Kubernetes quickly and easily, you can use a local development environment such as minikube or Docker for Desktop. These tools allow you to run a single-node Kubernetes cluster on your local machine, making it easy to experiment with Kubernetes and develop applications without the need for additional resources.

3- **Install Kubernetes on your own infrastructure:** If you want to set up a production-grade Kubernetes cluster, you can install Kubernetes on your own infrastructure. There are a number of tools and resources available to help you do this, including the kubeadm tool and the Kubernetes documentation.

4- **Installing Kubernetes using a package manager:** Kubernetes can be installed using a package manager such as apt-get (for Debian-based systems) or yum (for Red Hat-based systems). This method is relatively straightforward and can be used to install Kubernetes on a single node or multiple nodes.

Regardless of which option you choose, the process of installing Kubernetes generally involves the following steps:

*   **Install the required dependencies:** Depending on the installation method you choose, you may need to install additional dependencies such as Docker, etcd, or a container runtime.
    
*   **Install the Kubernetes control plane components:** This includes the Kubernetes API server, the etcd distributed key-value store, and the scheduler.
    
*   **Install the worker node components:** This includes the kubelet, kube-proxy, and container runtime.
    
*   **Configure the cluster:** This involves setting up networking, security, and other cluster-wide configurations.
    

Installing Kubernetes can take some time and effort, but the process is well documented, and there are several resources available to help you get started. Once you have a Kubernetes cluster up and running, you can begin deploying and managing containerized applications with ease.

# Commands

Here are some essential Kubernetes commands that you may find useful:

```plaintext
kubectl get pods: Lists all the pods in the current namespace.
kubectl describe pod <pod-name>: Shows detailed information about a specific pod, including its status, containers, and events.
kubectl logs <pod-name>: Shows the logs for a specific pod.
kubectl exec -it <pod-name> -- bash: Opens a shell inside a specific pod.
kubectl create -f <filename>: Creates a new resource based on the configuration in the specified file.
kubectl cluster-info : Understand your cluster services
kubectl apply -f <filename>: Updates an existing resource based on the configuration in the specified file.
kubectl delete -f <filename>: Deletes a resource based on the configuration in the specified file.
kubectl get secrets : Reveal your secrets
kubectl get events  : Keeping track of events
kubectl scale deployment <deployment-name> --replicas=3: Scales a deployment to the specified number of replicas.
kubectl rollout restart deployment <deployment-name>: Restarts a deployment.
```

These are just a few examples of the many commands available in Kubernetes. For a full list of commands, you can refer to the KubernetesDocs or use the kubectl --help command.

# Creating a Kubernetes deployment

A Kubernetes deployment is a configuration file that defines a desired state for a group of pods and the policies to manage them. It is used to deploy and manage applications on a Kubernetes cluster.

To create a deployment in YAML, you will need to define the following elements:

1- **The API version of the deployment object**: This specifies the version of the Kubernetes API that the deployment object will use.

2- **The kind of the deployment object**: This specifies the type of object that the deployment object represents. In this case, it will be "Deployment."

3- **The metadata of the deployment object**: This includes the name of the deployment and any labels or annotations that you want to apply to it.

4- **The spec of the deployment object**: This specifies the desired state of the deployment, including the number of replicas, the container image to use, and any environment variables or command-line arguments.

Here is an example of a simple deployment YAML file that deploys a single pod with an NGINX container:

```plaintext
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 1
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:latest
```

To create a deployment using this YAML file, you can use the **kubectl apply** command:

`kubectl apply -f deployment.yaml`

> We will have our deep dive with YAML.

This will create a deployment with the specified configuration and deploy it to the cluster. You can use the `kubectl get deployments` command to view the status of the deployment and the `kubectl describe deployment` command to get more detailed information about the deployment.

It is also possible to update an existing deployment by modifying the YAML file and using the `kubectl apply` command again. This will update the deployment with the new configuration and rolling out the changes to the pods in the deployment.

This makes it easy to deploy and manage even large-scale applications on Kubernetes.

## Monitor the deployment

After creating a Kubernetes deployment in YAML, there are several things you can do to manage and monitor the deployment:

*   **View the pods in the deployment:** You can use the `kubectl get pods` command to view the pods in the deployment, including their status and the containers that they are running.
    
*   **View the logs of the pods:** You can use the `kubectl logs` command to view the logs of the pods in the deployment. This can be helpful for debugging and troubleshooting issues with the deployment.
    
*   **Scale the deployment:** You can use the `kubectl scale` command to scale the deployment up or down by increasing or decreasing the number of replicas. This can be useful for handling changes in demand or for performing maintenance tasks.
    
*   **Roll out updates to the deployment:** You can use the `kubectl apply` command to update the deployment with new configurations or changes to the container image. This will roll out the changes to the pods in the deployment in a controlled and configurable way.
    
*   **Monitor the performance of the deployment:** You can use tools like **Kubernetes Dashboard** or **Prometheus** to monitor the performance of the deployment, including the resource usage of the pods and the health of the containers. This can help you identify and troubleshoot issues with the deployment.
    

There are several actions you can take after creating a Kubernetes deployment in YAML to manage and monitor the deployment and ensure that it is running smoothly.

## Conclusion

In conclusion, Kubernetes is a powerful and flexible open-source platform that is widely used to deploy and manage containerized applications in a distributed environment. It offers a consistent and reliable environment for running applications and simplifies the process of deploying and managing applications in a distributed environment.

There are several ways to install Kubernetes, including using a Kubernetes distribution, installing it using a package manager, or installing it manually. The best method for you will depend on your specific needs and preferences.

Once Kubernetes is installed, you can use YAML files to create and manage deployments, specifying the desired state of the deployment and the policies to manage it. You can then use a variety of tools and commands to manage and monitor the deployment, including viewing the status of the deployment, viewing the logs of the pods, scaling the deployment, rolling out updates, and monitoring the performance of the deployment.

Overall, Kubernetes is a powerful and essential tool for deploying and managing applications in a distributed environment, and it is worth considering for any organization that needs to deploy and manage applications at scale. **Adopt DevOps.**

# Continue to innovate

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671297664725/XzlYM3nM7.png)

Managing multiple deployments on Kubernetes can still be a time-consuming task, especially as the number of deployments grows. It can be difficult to keep track of all the different components and resources needed for each deployment, as well as ensure that they are all properly configured and up-to-date. This is where Helm comes in. Helm is a tool that simplifies the process of deploying and managing applications on Kubernetes. This will be our next topic of discussion. keep an eye out.
