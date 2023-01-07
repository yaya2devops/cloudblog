# Quickstart Ruby On Rails

# Introduction

Whether you are a beginner looking to learn your first programming language, or an experienced developer looking to add Ruby to your toolkit, this post will give you the knowledge you need to get started. So let's dive in and learn how to use Ruby!

Let's explain 2 critical points:

* Ruby is a programming language
    
* Ruby on Rails also RoR is a framework that simply provides you with more tools to excel with Ruby developement!
    

To start building a web application with Ruby on Rails, you will need to do the following:

Install Ruby and Rails: You will need to have the **Ruby** programming language and **the Rails** web development framework installed on your machine. You can install them using a package manager such as rbenv or rvm, or you can download and install them manually.

## Install Ruby

* For windows, download the [installer](https://rubyinstaller.org/) check this command in your terminal once finished, if returned the version, done.
    

```bash
ruby -v
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673019316766/fcdd6f63-d399-46e9-acc5-740f9ccf153e.png align="center")

* for Linux refer [here](https://www.ruby-lang.org/en/documentation/installation/)
    

## Install Rails

To start building an app with Ruby on Rails, you will need to install Rails itself. You can do this by running the following command in your terminal:

```bash
gem install rails
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673019334371/16601d05-e5e2-4182-8853-5322f6ef1aa1.png align="center")

This will install Rails and all of the dependencies needed to build a Rails app.

Once Rails is installed, you can create a new Rails app by running the following command:

```bash
rails new myapp
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673019354526/ff06bd70-5c23-4b00-9ce0-d4eac05de360.png align="center")

This will create a new directory called myapp with the basic structure of a Rails app and it looks something like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673020354862/447612eb-42d0-4581-8d17-fd303132cead.png align="center")

To start the Rails development server, navigate to the `myapp` directory and run the following command:

```bash
cd myapp
rails server
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673085803496/30e63c2b-2c27-402d-a0b9-c582e88f9583.png align="center")

This will start the Rails development server, and you can view your app by visiting http://localhost:3000 in your web browser.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673085814329/4ff1e967-ab6b-44f5-a3dc-2f59f0e398b8.png align="center")

You can then start building your app by following the steps in the Ruby on Rails tutorial; simply click on the logo in the middle and it will direct you to the tuto where it will guide you through the process of building a complete Rails app from start to finish.

## Good job, what's next?

Ruby is the driving force behind websites like Twitter. There's a lot more to it than that. You can investigate the following:

* Set up the database: Rails uses a database to store application data. By default, it uses SQLite, but you can also use other databases such as MySQL or PostgreSQL. You will need to set up your database and configure your Rails application to use it.
    

```bash
rails db:migrate
```

* Define your models and controllers: In Rails, models represent the data in your application and controllers handle incoming requests and determine what to do with them. You will need to define your models and controllers and specify how they should interact with your database and views.
    
* Create your views: Views are the user-facing components of your application. They define the layout and content that will be displayed to users. You can create views using HTML, CSS, and the Rails template language.
    
    You can achieve the above by writing this command:
    
    ```bash
    rails generate scaffold post title:string content:text
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673112784685/6676e160-1150-443e-9c39-31ec626a309c.png align="center")

* Test and debug your application: As you build your application, you will want to test it to ensure that it is functioning correctly. You can use tools such as the Rails console and the debugger to test and debug your application.
    
* Deploy your application: When your application is ready to be used by others, you will need to deploy it to a web server. There are many options for hosting Rails applications, including hosting providers such as Heroku or AWS.