# heroku-greetings

## Deploy new application

**heroku create** - creates new remote repository and a reference to it called `heroku`

**git push heroku `master`** - merges commits from local branch `master` to the same named branch on heroku. Triggers application building on heroku.

## Link existing heroku application

**heroku git:remote -a `application-name`** - will add reference to remote heroku repository

## Procfile

A `Procfile` is a text file placed in the root of your application, that lists the process types in an application. Each process type is a declaration of a command that is executed when a dyno of that process type is started.

There are two main process (dyno) types:
* web - reponsible for handling user's web requests
* worker - responsible for executiong background work

Operations for each process type could be declared in the following format (one process type per line, with each line containing):
`process type: command`

The syntax is defined as:
* **process type** – an alphanumeric string, is a name for your command, such as web, worker, urgentworker, clock, etc.
* **command** – a command line to launch the process, such as `node server.js`.

