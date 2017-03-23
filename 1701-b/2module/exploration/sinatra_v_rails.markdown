## Sinatra versus Rails Exploration

### Setup:

First, clone down the Rails project:

```terminal
git clone https://github.com/turingschool/job-tracker.git rails_project
```

And then clone down the Sinatra project:

```terminal
git clone https://github.com/turingschool/bike-share.git sinatra_project
```
Now cd into each project, run `bundle` on each project, and you're ready to go. We will only be looking at the code base and not interacting with the app. If you wanted to run the server and interact with the app, you would need to create your database, migrate your migrations, etc.

### Exercise:

1. Take a look at this stripped down Sinatra app and this stripped down Rails app. How are they different and how are they similar? Identify 5 differences, and for each one describe 1-2 implications. What effect does that difference have for each framework? If you don't know exactly, draw on your knowledge and experience and make some educated guesses/inferences. Also, practice your research skills to look into the differences.

* For its views, the Rails app is using a .html.erb extension. I would probably infer from this that it is adding the ERB extension it is able to evaluate the ruby within, and then outputs a pure HTML file? 

* There is a bin directory which is short for binary, according to StackOverflow it is an application. Each of the files is a ruby file called a binstub. Binstubs are wrappers around gem executables, like rails or bundle, which ensures a gem executable is run inside the correct environment for your Rails app. They can be run from the command line without the need to start any ruby interpreter yourself.

* Rails uses Spring to keep the app running in the background.

* There is a concerns directory in the Rails app. One use of this directory is to create modules to DRY up your Models if they share similar method functionalities.


1. Consulting blogs and commentary you find online, identify 3 similarities between Rails and Sinatra.

* They are both gems
* They do the heavy lifting to spin up a web server
* They are both DSLs

1. Consulting blogs and commentary you find online, identify 3 things that distinguish Rails, advantages.

* Rails is more robust in functionaility. Sinatra is more basic, although Sinatra's simplicity could be advantage depending on what you're tryin' to do.

* From what I've read I wouldn't say one frame work is better than the other. Sinatra is better than Rails for simple Applications, and Rails obviously gives you a lot of tool for building large scale applications. Rails makes a lot of assumptions and gives you a lot of functionality that you may not even use.

1. In your Rails project, what does the `routes.rb` file inside of the `/config` directory do? What does this correlate to in our Sinatra app?

* Matches URLs to code. It's like our controller in Sinatra.

1. We teach Sinatra by adding some structures that Sinatra doesn’t need, but help you make the transition between Sinatra and Rails. What does a stripped down implementation of Sinatra look like, and what are the pieces we’ve added for educational purposes?

The MVC file structure is not necessary, but makes sense from an organizational standpoint. Although I believe you could have every file living in whatever structure you would like as opposed to Rails which I think imposes a more a strict convention for file structure due to the implicit functionality provided.
