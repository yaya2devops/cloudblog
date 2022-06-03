## Host Your Application Using Azure Blob Storage & CloudFlare | DNS Configuration

# Introduction
It's interesting how I came into CloudFlare by accident when hunting for a solution to the [Cloud Resume Challenge](https://y4hya4.github.io/Azure_Cloud_Resume_Challenge/)  because my student subscription didn't include Azure CDN support & appearing to be something I'm grateful I came across.

## Content Delivery Network 
A CDN is a computer network that stores copies of data at various network nodes. <br> A well-designed and properly implemented CDN improves data access by lowering latency and allowing for the rapid transfer of assets required for Internet content loading, such as HTML/JavaScript images and videos.
# CloudFlare
CloudFlare is a content delivery network (CDN) that consists of a large number of data centers and offers a variety of services to help websites load quicker and more securely. Cloudflare now handles five to ten percent of global internet traffic, making it one of the world's largest CDNs.

### Domain Name System
Instead of IP addresses, the Domain Name System allows you to access remote systems by inputting human-readable device hostnames. DNS creates a link between a domain name such as "https://www.yahya-abulhaj.dev" and its IP address.
### Nameservers
A nameserver is an Internet server that handles queries about the location of the domain name's various services. Name servers define your domain's current DNS provider in simple terms.
### CloudFlare Page Rule 
Clouflare page rules are something to keep in mind as you progress through the tutorial. In most circumstances, It enables you to override configurations made elsewhere on the Cloudflare dashboard.

---
# The Lab
### Configure Cloudflare With The Domain Provider
To reap the benefits of CloudFlare, you must update your nameserver. Follow the steps described in this [article](https://developers.cloudflare.com/dns/zone-setups/full-setup/setup/).<br> After that, you are no longer mandatory to use your cloud provider. Cloudflare will act as your primary DNS provider, configuring and managing your records. <br> A notable advantage is the speed with which new subdomains can be mapped to the domain that cloudflare maintains.


## Setup Azure Blob Storage Custom Domain
To get started, first create an Azure Storage in the Azure portal, then deploy your application to a container within this service.

![My Application Container.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940337556/a5Puqs2v_.png)


> Make sure your Static Web App is enabled if you're going to host static content like html pages.


![STATIC.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940360849/GFRxVgGJ9.png)

Second, go to **networking** then custom domain. Enter these settings in CloudFlare, then return and write down your domain.

![NETWORKING.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653943290606/fzhpKp1aM.png)



> Note that unless you change your record proxy status to DNS-ONLY, which is colored in grey, you won't be able to save the custom domain in the storage service. 

That's how you should end up with your final collection of records.


> ![Untitled (1600 × 400 px).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940520367/JkeoR672p.png)



### Still not working?
Remember the Page Rules; this will be our last and best option for mapping your content to a certain domain and getting it to function.
- Log into your Cloudflare Dashboard
- Go Rules => Page Rules => Create Page Rule

Enter the desired domain and strict SSL on this page. Your application will be properly configured and will operate flawlessly.




![pagerule.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940513212/O0WKONYXy.PNG)





# Bonus, CI/CD
### Overview

![Renew & Stay Certified (3).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1653941937138/mauBqmQpV.png)
Continuous integration and continuous delivery are two independent concepts that are commonly used together under the term CI/CD.

**Continuous integration:**<br> CI is a development technique that automates the building, testing, and merging of application code updates.

**Continuous delivery:**<br> The tested code from continuous integration is automatically distributed in numerous settings by a manual trigger in the following step of the process. It is an approach in which code updates are packaged and automatically deployed to production.

###  Pipeline
Now, I'd like to keep track of my changes. Rather than redeploying the app, I want the content uploaded to a cloud-based Git repository (best known GitHub or Gitlab) and when pushed, it should affect on my real-time application. We can accomplish this by configuring a pipeline to support the CI/CD process.
