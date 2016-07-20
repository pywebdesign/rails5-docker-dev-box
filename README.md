# rails5-docker-dev-box
Simple dev box with docker, the gems are installed locally in vendor/bundle 

## Setup

### Clone repo
git clone ...

### Rename folder with the name of the rails app you want to create

### Create rails app
```
  fig run web bundle install
  
  fig run web bundle exec rails new .
  #Answer yes to conflicting file. you may keep the .gitignore as is if you want
  
  . unlcok.sh
  
```

### Setup database
set up database.yml file: (change app_ with your app name like myappname_)

```
  default: &default
  adapter: postgresql
  encoding: unicode
  pool: 5
  host: db
  username: postgres

development:
  <<: *default
  database: app_development

test:
  <<: *default
  database: app_test

production:
  <<: *default
  database: app_production
```

```
  fig run web bundle exec rails db:create
  fig run web bundle exec rails db:migrate
```

### Set up gems
```
  fig run web bundle install
```

### Have fun
```
  fig up
  

  
