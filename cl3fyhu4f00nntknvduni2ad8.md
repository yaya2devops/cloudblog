## Why HashiCorp Terraform?



---

# Infrastructure As Code (IaC)


![IaC files.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653311067910/kOfSuTBEs.png align="left")

As the name implies, IaC refers to **the management and provisioning of infrastructure using code rather than dealing with a graphical user interface and tapping here and there**. Although it does seem simple, a significant problem had to be resolved. <br>
For instance, setting up such a complex architecture the traditional approach can take days of configuration while using an IaC tool can save you a considerable amount of time and assist you in achieving the levels of agility required to construct a successful route.


---
## Cloud Providers IaC


![over.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653311294174/G97dVfo2r.png align="left")



It's important to note that each cloud provider have their own IaC tool.  <br>
These tools are useful when working with a specific cloud.<br> When a new service release is available here, for example, it may take some time before it is  accessible in an external product like Terraform.  <br>However, **Cloud Providers IaC tools can only be used within their own services.**



# Terraform
Terraform by HashiCorp is an infrastructure as code tool that allows you to provision cloud and on-premises resources in configuration files written with a coherent language called HashiCorp Configuration Language (HCL).

### Overview


![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653221233055/V_BUpB8lX.png align="left")


Say i'm working at a company "A" and my job is to carry out an Azure storage, an Amazon DynamoDB and Google Compute Enginer VM etc..<br>
Bouncing from a portal and its terminal to another is fine until Terraform comes to play.
HashiCorp's product can handle infrastructure across multiple cloud platforms.

### HashiCorp Configuration Language (HCL)
The language was designed in human-readable format and empowers declarative logic's use in more complex applications. It is JSON compatible, which means it can communicate with systems other than those in the HashiCorp products line. <br> HCL was created to have a more clearly visible and defined structure when compared with other well known configuration languages, like YAML.

```auth.tf
# Example for Authenticating with AWS
provider "aws" {
  region     = "us-west-2"
  access_key = "my-access-key"
  secret_key = "my-secret-key"
}
```

---
# Getting Started

### Install Terraform CLI
Terraform must be installed in order for your terminal to understand it. <br> 
Follow the steps outlined [here](https://learn.hashicorp.com/tutorials/terraform/install-cli).

### Lifecycle
The basic Terraform workflow consists of :
1. Write - Create infrastructure in the form of code
2. Init - Initialize a working directory:
``` terraform init ```
3. Plan - Before applying changes, preview them:
``` terraform plan ```
4. Apply - Create a replicable infrastructure:
``` terraform apply  ```
5. Destroy - Destroy infrastructure when no longer needed: 
```terraform destroy```

**What is a State file?** <br>
Terraform saves information about the infrastructure it creates in a terraform.tfstate file every time you run it.


### About Modules
The module is one of Terraform's Core concepts.
It is a collection of Terraform configuration files in a directory. A module can be as simple as a  single directory containing one or more .tf files.

``` .TF
.terraform/modules
├── DevModule
│   ├── main.tf
│   ├── output.tf
│   ├── terraform.tfstate
├── ProdModule
│   ├── yaya.tf
│   ├── output.tf
│   ├── terraform.tfstate

```
You can find a ready-to-use modules in the [Terraform Registry](https://registry.terraform.io)



---

# Proceed Further

### Hands-On
The best way to learn about terraform is to do it yourself.
With a hands-on approach, you'll quickly grasp the material and improve with each keystroke. <br>
[Terraform Best practices](https://www.terraform-best-practices.com) is a good option to consider along the way.

### Terraform Certification

![tfcert.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653221441459/e2GB5lxQ6.png align="left")


Another way to get started is to study and take the exam. I've found this method useful since deadlines push to your limits. <br>

[HashiCorp Certified: Terraform associate](https://www.hashicorp.com/certification/terraform-associate) is multiple choice exam that relies on a practical experience. <br>
In this case, Terraform open source [documentation](https://www.terraform.io/docs) is for everyone to learn and experiment this product with.


## Conclusion
Terraform is a constantly evolving, extremely useful IaC solution that can greatly improve the efficiency of our DevOps.
We've only covered the fundamentals to get you started in this article; there's a lot more to Terraform that certainly requires more attention.
