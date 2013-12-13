# Create a Static Web Server on Heroku

This assumes node, npm, and git on your system.

It also assumes you already have a heroku account and heroku toolbelt installed with heroku client + foreman.

## Steps

Create directory

    mkdir Static
    npm init
    npm install express --save

Edit files

    subl app.js
    mkdir public
    subl index.html

Create repository

    git init
    git status
    echo "node_modules" > .gitignore
    git add .
    git commit -m "my new static site"

Create proc file

    echo "web: node app.js" > Procfile
    git add . 
    git commit -m "proc file"

Create heroku app

    heroku create hs-static
    get push heroku master

Check out the full screencast.