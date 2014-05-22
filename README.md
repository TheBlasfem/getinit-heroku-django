getinit-heroku-django
=====================

A skeleton app Django ready to deploy in Heroku 

Install django-toolbelt, which includes all of the packages we need

    sudo pip install django-toolbelt

If fails, maybe you need dev dependencies

    sudo apt-get install python-dev python-psycopg2 libpq-dev

Set your heroku app

    heroku create

Create your postgresql db in Heroku Addons

Push your files to heroku

    git add .
    git commit -m "send to heroku"
    git push heroku master

Run one dyno
    heroku ps:scale web=1

And Finnaly, set your settings file to your heroku app and open it

    heroku config:set DJANGO_SETTINGS_MODULE=your_project.settings
    heroku open