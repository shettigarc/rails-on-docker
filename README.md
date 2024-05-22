# Rails on Docker

> **Update:** Check out the new course on setting up a [Rails local development environment with Docker using DevContainers](https://www.devteds.com/devcontainers-for-developers-multi-container-local-dev-setup/) 

> This is an old episode and source code. Instead, I suggest you check out the new way of working with [Docker for Rails](https://youtu.be/xfeQ6vDuidA) applications

[![Episode Video Link](https://i.ytimg.com/vi/xfeQ6vDuidA/hqdefault.jpg)](https://youtu.be/xfeQ6vDuidA)

## Old code & episode

Learn how to use docker / docker compose to create and run rails application.

[Episode video link](https://youtu.be/a-jcTib9ZPA)

## Tested on

* Mac OSX - 10.10.5
* Docker - 1.12.1
* Docker compose - 1.8.0

## Instructions/commands

```
mkdir ~/projects/noteapp
cd ~/projects/noteapp
# Create Gemfile
# Create Dockerfile
# Create docker-compose.yml
docker-compose run app rails new . --force --database=mysql --skip-bundle
docker-compose build
docker-compose up
# http://localhost:3001
docker-compose run --rm app rails g scaffold note title body:text
docker-compose run --rm app rake db:migrate
# http://localhost:3001/notes
```


