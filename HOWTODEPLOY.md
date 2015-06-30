# How to Deploy

```
git clone git://github.com/redmine/redmine.git
cd redmine
git checkout 2.1-stable
cp config/database.yml.example config/database.yml
bundle install
bundle exec rake generate_secret_token
```

In my case, an error of rmagick occured when execute `$ bundle install`. I just installed imagemagick by homebew, then it works.

```
$ brew install imagemagick
```

```
heroku create your_redmine_app_name
git add -A
git commit -m "prepare for heroku"
git push heroku 2.1-stable:master
```

```
heroku run rake db:migrate
heroku run rake redmine:load_default_data
heroku restart
heroku open
```
