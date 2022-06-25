## Automate the CI/CD Pipeline using Harness.io
![](https://cdn.hashnode.com/res/hashnode/image/upload/v1655412104295/eCliRNBao.gif?w=1600&h=840&fit=crop&crop=entropy&auto=format,compress&gif-q=60&format=webm)
# Introduction
Many firms have implemented continuous integration and spent numerous hours automating scripts, but they are unable to keep up with continuous delivery, owing to the complexity of the process.
In addition to the fact that CI and CD are vastly dissimilar.

**Harness** employs a model to define your goals rather than scripting. You do not need to write a script for the pipeline, though you can use YAML within Harness. The real benefit here is that you simply select these steps, stages, as well as every component required for the configuration file via a user-friendly interface

As part of the process, Harness performs continuous verification and includes an artificial intelligence layer to guarantee that nothing went wrong in terms of quality, security and performance. 

> [What is a pipeline?](https://blog.yahya-abulhaj.dev/host-your-application-using-azure-blob-storage-and-cloudflare-or-dns-configuration#heading-bonus-cicd). 

# Harness Solutions
Harness.io is a tool that used to be part of the CD category and has since grown to include four main products. It is now a CI/CD platform that can be used to build and ship code while progressively innovating and adding new features.
- [Compare DevOps Tools with Harness](https://harness.io/learn/comparison-guide)

###  Continuous Delivery
 CD is Harness primary solution. As they have stated Harness CD is a Self-Service Continuous Delivery module that allows engineers to deploy on-demand without the use of scripts, plugins, version dependencies, toil, downtime, or frustration.

![harness.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655489756667/60voGLk7K.png)
### Continuous Integration
The first step towards automating your software delivery is continuous integration.
[Drone Ci](https://www.drone.io) is Harness' open source platform for automating software development and testing. Committing the code to a repository triggers the Drone CI.
### Cloud Cost Management
Control and cost management over your workload. <br>

![costs.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655489778246/JEq0AwglE.png)
These are some of its key features.
- **Cost Transparency** Valuable insights into the used, idle, and unallocated resources in your workloads and clusters.
- **Optimization** Lowering your overall cloud spend by identifying mishandled resources and eliminating waste.
- **Governance and Reporting** Keep track of your budget use with reports and alerts at key stages.

### Feature Flags
Feature flags are a way to test major updates before they are released. Because you can validate the functionality in the real world, development teams can add a new level of confidence when building a new feature.
- [Introducing Harness Feature Flags](https://harness.io/blog/product-updates/introducing-harness-feature-flags/)



---

# The Workflow

### What is an Artifact?
Artifact is an unintended consequence of the software development process. It could include the project source code, dependencies, binaries, or resources, and it could be expressed in a different ways based on the technology. An AMI, a Docker image, or a JAR file are all examples of Artifcats.

**When harnessing, the common workflow is as follows:**
- Use the **CI module** to create an artifact.
- Once artifact has been created, deploy it to the **CD task.**
- When running on a specific infrastructure, the developer can use **Feature Flags** to enable and disable specific functionality.
- Continuous cost management monitoring using **Harness Cloud Cost Management.**

---

## Final Note

As large corporations already have their own DevOps cycle in place.<br> Harness is an excellent option to consider for businesses just getting started in the DevOps space and aiming to increase their agility. <br>
Are you aware that Harness is a viable option for you?







