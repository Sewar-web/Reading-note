# HEROKU DEPLOYMENT
***Step 1 - Create the project***

1. The first step is to create a simple structure for our project with some basic files. For this article, I’ll create a demo server with NodeJS.

2. In a new folder I’ll open a terminal and run the command npm init -y in order to create a new project. The dummy server will be written in Express, so we need to run the npm install express command to install this module.

3. Once this library is installed, we can create a new file for our project, named app.js. Inside it we’ll write the code for our simple server: 

4. We can start the application by running node app.js. Then we can try it out at the following URL http://localhost:3000. At this point you should see the message Hello World in the browser. 

5. Great apps come from developers using tools and languages they love. That’s why a great developer experience has always been at the very heart of what we do. We embrace the languages of the modern app economy: Node, Ruby, Java, Scala, PHP and more. Heroku makes the processes of deploying, configuring, scaling, tuning, and managing apps as simple and straightforward as possible, so that developers can focus on what’s most important: building great apps that delight and engage customers.

6. Data lies at the heart of any significant app — whether it’s customer data or data about the service it provides — an app and its data go hand in hand. Heroku’s rich ecosystem of managed data services includes Heroku Postgres, Heroku Redis and Apache Kafka on Heroku. Developers shouldn’t need to discover how to optimally provision a database through trial and error - but instead have immediate access to a scalable, highly available database with rollback - one that supports their apps and development style.

***Conclusion***
1. Heroku allows developers to quickly and almost painlessly deploy an application on a web server.

2. It also provides a lot of plugins that you can integrate into your application.

3. A PaaS solution will always allow you to move faster than the solution with a VPS where you have to configure everything from the ground up.

![image](data:image/png;base64,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)




**Creating a Heroku remote**
* Git remotes are versions of your repository that live on other servers. You deploy your app by pushing its code to a special Heroku-hosted remote that’s associated with your app.

* For a new Heroku app
The heroku create CLI command creates a new empty application on Heroku, along with an associated empty Git repository. If you run this command from your app’s root directory, the empty Heroku Git repository is automatically set as a remote for your local repository.

heroku create
```
Creating app... done, ⬢ thawing-inlet-61413
https://thawing-inlet-61413.herokuapp.com/ | https://git.heroku.com/thawing-inlet-61413.git
You can use the git remote command to confirm that a remote named heroku has been set for your app:
```

```git remote -v
heroku  https://git.heroku.com/thawing-inlet-61413.git (fetch)
heroku  https://git.heroku.com/thawing-inlet-61413.git (push)
```