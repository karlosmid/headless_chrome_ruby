# headless_chrome_ruby

Docker configuration files for headless chrome selenium-webdriver testing using Ruby ecosystem

This is combination of [this](https://github.com/jrglee/docker-ruby-chrome) great docker image,  
and this [blog post from bradgessler.com] (http://bradgessler.com/articles/docker-bundler/) that explains how to make `bundle install` as fast as possible.

# How to install it

In `docker-composer.yml`, replace `{project_name}` with name of your ui automation project folder name.

Copy `Dockerfile` and `docker-composer.yml` to your ui automation project folder.

Start `docker terminal`, cd to ui automation project folder.

Run `docker-compose build --force-rm`

Run your tests: `docker-compose run web /bundle/bin/cucumber -f html -o chrome.html features/feature_name.feature`

`chrome.html` file is created in your development machine!
