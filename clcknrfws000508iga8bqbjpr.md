# Quickstart Ruby On Rails


# Let's get the workflow

To start building a web application with Ruby on Rails, you will need to do the following:

Install Ruby and Rails: You will need to have the **Ruby** programming language and **the Rails** web development framework installed on your machine. You can install them using a package manager such as rbenv or rvm, or you can download and install them manually.


## Install Ruby

- For windows, download the [installer](https://rubyinstaller.org/)
> checkthis command in your terminal once finished

 ```
ruby -v
```


- for Linux refer [here](https://www.ruby-lang.org/en/documentation/installation/)


## Install Rails
To start building an app with Ruby on Rails, you will need to install Rails itself. You can do this by running the following command in your terminal:

```
gem install rails
```

This will install Rails and all of the dependencies needed to build a Rails app.

Once Rails is installed, you can create a new Rails app by running the following command:

```
rails new myapp
```
This will create a new directory called myapp with the basic structure of a Rails app.

To start the Rails development server, navigate to the `myapp` directory and run the following command:

```
cd myapp
rails server
```

This will start the Rails development server and you can view your app by visiting http://localhost:3000 in your web browser.

You can then start building your app by following the steps in the Ruby on Rails Tutorial. This tutorial will guide you through the process of building a complete Rails app from start to finish.



## Good job, what's next?

Ruby is the driving force behind websites like Twitter. There's a lot more to it than that. You can investigate the following:

- Set up the database: Rails uses a database to store application data. By default, it uses SQLite, but you can also use other databases such as MySQL or PostgreSQL. You will need to set up your database and configure your Rails application to use it.

- Define your models and controllers: In Rails, models represent the data in your application and controllers handle incoming requests and determine what to do with them. You will need to define your models and controllers and specify how they should interact with your database and views.

- Create your views: Views are the user-facing components of your application. They define the layout and content that will be displayed to users. You can create views using HTML, CSS, and the Rails template language.

- Test and debug your application: As you build your application, you will want to test it to ensure that it is functioning correctly. You can use tools such as the Rails console and the debugger to test and debug your application.

- Deploy your application: When your application is ready to be used by others, you will need to deploy it to a web server. There are many options for hosting Rails applications, including hosting providers such as Heroku or AWS.
