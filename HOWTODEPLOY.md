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


