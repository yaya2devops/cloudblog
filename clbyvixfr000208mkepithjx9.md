# Monitoring Made Easy with Prometheus




#  Site Reliability Engineering 

Site reliability engineering (SRE) is a discipline that combines software engineering and operations to ensure the reliability and scalability of a system. Google first applied it in 2003 to enhance the reliability of the company's systems and services.

At the time, Google's systems were rapidly expanding, and the company was facing increasing challenges in maintaining their dependability. To address this, Google formed a team of engineers in charge of both developing and operating the systems. Site reliability engineers (SREs) were the title given to these engineers.


Google's SRE team was primarily in charge of:
- Monitoring the systems 
- Automating tasks
- Responding to incidents

They also worked to **continuously improve** the systems' reliability and scalability by modifying the architecture and introducing new tools and technologies. 


SRE has gained widespread acclaim in the tech industry since its inception. Many businesses now have SRE teams in place to ensure the reliability of their systems and services. Other disciplines, such as site reliability architecture (SRA) and site reliability management, have been inspired by SRE (SRM).

I recommend this Google resource for more on SRE: [https://sre.google/](https://sre.google/)


## SRE, Essential Principles

The primary goal of SRE is to use engineering principles to improve the performance of a system's operations. This involves a variety of approaches and techniques, all of which are designed to ensure that the system is running efficiently and effectively. 

Some of the key principles and practices of SRE include the following:


- **Automation is key:** SRE teams use automation to perform tasks that are repetitive, error-prone, or time-consuming. This allows them to focus on more important tasks and helps to reduce the risk of human error.

- **Error budgets:** SRE teams allocate a certain percentage of their time to proactive tasks such as improving the system's reliability, and the rest of the time is reserved for reactive tasks such as responding to issues. This is known as an error budget, and it helps the team prioritize tasks and ensure that the system remains reliable over time.

- **Use of data:** SRE teams rely heavily on data to understand the performance of the system and identify patterns or trends that may indicate a problem. They use tools such as application performance monitoring (APM) tools, infrastructure monitoring tools, and log analysis tools to collect and analyze data.

- **Continuous improvement:** SRE teams are focused on continuously improving the reliability and scalability of the system. This can involve implementing changes to the system's architecture, introducing new tools and technologies, or redesigning processes to make them more efficient.

- **Reliability is a feature:** SRE teams view reliability as a critical feature of the system, and they prioritize it accordingly. They use a variety of **tools and techniques** to **monitor the system** and detect issues, and they take action to prevent outages and improve the overall reliability of the system.


**Prometheus**, the open source project from the Cloud Native Computing Foundation (CNCF), is widely recognized as one of the top monitoring systems available. With its powerful features and open-source nature, it is a popular choice among professionals looking to improve their monitoring practices. So, if you're ready to get started with Prometheus and take your monitoring efforts to the next level, let's get started!


# Get to Know Promethus

**P**rometheus is a time series database  monitoring system, Yes, once again, the result of an open-source-driven community. The development of Prometheus has been heavily influenced by the community, and it continues to be an actively developed and supported project.


**SoundCloud engineers** created Prometheus in 2012 as a way to monitor the performance of their systems and services. It gained popularity quickly and was adopted by other organizations. The CNCF approved it as a project in 2015, and it has since been actively developed and maintained by a large community of users and contributors.

Prometheus development is guided by a set of principles that prioritize simplicity, robustness, and usability. It is intended to be scalable and capable of handling large amounts of data as well as a high volume of queries. It also has a set of integrations with other tools and systems, making it simple to use in a variety of settings.

Let us explain what makes it a worthwhile consideration!

## Features For Your Note

Prometheus has several key features that make it an appealing choice, incl:

- **Flexible query language:** Prometheus has a powerful query language that allows users to define custom metrics and alerts based on their specific needs.

- **Time series database:** Prometheus stores metrics in a time series database, which allows users to view and analyze the data over time to understand trends and identify patterns or anomalies.

- **Scraping:** Prometheus can scrape metrics from target systems, which means it can periodically retrieve metrics from other systems and store them in its time series database.

- **Alerting:** Prometheus has built-in alerting capabilities that allow users to define alert rules based on metric thresholds or other conditions. When an alert is triggered, it can send notifications to the user or trigger an automatic response.

- **Integrations:** Prometheus has a rich set of integrations with other tools and systems, which makes it easy to use in a variety of environments. It is often used in conjunction with tools such as **Grafana** and **Kubernetes**.

- **Scalability:** Prometheus is designed to be scalable and can handle large amounts of data and a high volume of queries.


## Workflow Prior To The Jump
In order to effectively implement this tool and ensure a smooth workflow, I will provide a detailed explanation of the process. Then, we will move forward and complete each step in a step-by-step manner, carefully following the guidelines and paying close attention to detail in order to achieve the desired results!

1- Install Prometheus: You can install Prometheus on your own server or use a managed service such as Prometheus as a Service.

2- Configure Prometheus: After installing Prometheus, you will need to configure it to collect metrics from the target systems and applications that you want to monitor. You can do this using configuration files and command-line flags.

3- Set up targets: To collect metrics, Prometheus needs to know which systems and applications to scrape for data. You can set up targets using configuration files or the Prometheus web interface.

4- Set up alerts: Prometheus includes a powerful alerting system that allows you to set up rules and notifications for any kind of behavior or anomaly. You can set up alerts using configuration files or the Prometheus web interface.

5- Visualize and analyze data: Prometheus includes a flexible query language and a range of visualization tools that allow you to analyze and understand your metrics data. You can use these tools to create graphs, dashboards, and alerts.



# The Jump
The step-by-step instructions provided below will help you effectively get started with the Prometheus system. These steps will walk you through the process of installing and configuring Prometheus, ensuring that you can use the tool once it is up and running.

## Linux-Based OS
1- Download the latest release of Prometheus from the [official Prometheus website](https://prometheus.io/download/). You can either download a pre-built binary or build Prometheus from source.

2- Extract the downloaded archive and navigate to the directory containing the Prometheus executable.

```
tar xvfz prometheus-*.tar.gz
cd prometheus-*
```

3- Run the Prometheus binary:
```
./prometheus
```

## Windows-Based OS
The initial step is same, which is to install from the provided link.

2- Extract the downloaded archive and navigate to the directory using the command prompt:

```
cd C:\path\to\prometheus-*
```

3- Run the Prometheus binary:
```
prometheus.exe
 ```

## Create a configuration file for Prometheus. 

You can use the `prometheus.yml.example file` as a starting point and customize it to suit your needs. 

Let's create yours just right now! 

You will need to create a`  .yml`  file that specifies the configuration options for your Prometheus server. Here are guidelines for creating a configuration file for Prometheus:


1- Begin the file with ` global`  and ` scrape_configs`  blocks. The ` global`  block allows you to specify global configuration options that apply to all scrape jobs, while the ` scrape_configs`  block specifies individual scrape jobs and the targets they should scrape.


2- In the `global block`, you can specify options such as the external labels that should be applied to all metrics, the retention period for data, and the frequency at which the Prometheus server should scrape targets.

3- In the `scrape_configs` block, you can specify individual scrape jobs using the `- job_name` option. For each scrape job, you will need to specify the targets to scrape using the `static_configs` or `file_sd_configsv options. You can also specify additional options such as the scrape interval and the metrics path.

4- Save the file with a .yml extension and use the `--config.file` flag to specify the path to the configuration file when starting the Prometheus server.

Here is an example of a simple Prometheus configuration file:

```
global:
  external_labels:
    env: production
  retention: 90d
  scrape_interval: 15s

scrape_configs:
  - job_name: 'prometheus'
    static_configs:
      - targets: ['localhost:9090']

  - job_name: 'node_exporter'
    static_configs:
      - targets: ['localhost:9100']


```


This configuration file specifies two scrape jobs: one for the Prometheus server itself and one for the node exporter. It also specifies a global retention period of 90 days and a scrape interval of 15 seconds.

5- Start the Prometheus server using the following command:

```
 ./prometheus --config.file=<path to your config file> 

```

for Windows, instead of `./prometheus ` use `prometheus.exe` <br> 
Example:

```
prometheus.exe --config.file=prometheus.yml
```




That's it! GreatJob. You can verify that Prometheus is running by visiting http://localhost:9090 in your web browser. The Prometheus UI should now be accessible.

By default, Prometheus will listen on port 9090 for incoming metrics. You can use the `--web.listen-address` flag to specify a different port or IP address.

> To set up Prometheus as a service, you can use a process manager such as **Systemd** or **Upstart**.

| Prometheus as a service  |   Solution| 
|---|---|---|
| Windows  |  use the 'sc' utility ex;  `sc create Prometheus binPath= "C:\path\to\prometheus.exe"`|
| Linux  |   Use process manager such as **Systemd** or **Upstart** |

Start your monitoring Journey!
Some common use cases for Prometheus include monitoring the performance of servers, tracking the health of applications, and monitoring the usage of resources such as CPU, memory, and disk space. You can gain valuable insights into the performance and health of your systems and be better prepared to handle any issues that may arise.

At this level, you can proceed doing these steps:
- Set up alerts and create Alert rules.
-  Visualize and analyze data.
-  Monitor Third party Applications
- Collect Metrics 

By following the steps outlined in this blog, you should now have a fully functional Prometheus setup that is capable of collecting and visualizing metrics from your infrastructure.

# Synopsis

While **S**RE and **D**evOps have different focuses, they often overlap in practice and can be complementary to each other.  SRE teams may use DevOps practices such as continuous delivery and automation to improve the reliability of the system. Similarly, DevOps teams may adopt SRE principles such as error budgets and monitoring to ensure the reliability and performance of the system.

The moral, don't limit yourself to a specific job role; be curious and strive to learn as much as you can in order to provide value to your team and organization. and eventually the world.


I hope you've enjoyed learning about SRE, which I find personally very rewarding. It has been a pleasure to share my knowledge and experience with you today, and I hope you now have a better understanding of what SRE is and how it can be used in practice. With that, I believe we have covered great topics for today, so I will call our session to a close. Thank you for your time and consideration; I hope you will continue to investigate and learn more about SRE and DevOps in the future.




























