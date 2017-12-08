## Quick start

First run (install drupal core):

    $ mkdir drupal
    $ docker-compose run php composer create-project drupal-composer/drupal-project:8.x-dev . --stability dev --no-interaction

### Run environment

Start your development

    $ docker-compose up
    
Open `http://drupal.docker.localhost:8000/` in your browser

### Install

    $ docker-compose exec php su www-data -c "cd web && drush site-install standard --locale=de --db-url=mysql://drupal:drupal@mariadb:3306/drupal --account-pass=admin --site-name=ProjectName. -y "

### Install modules / themes / profiles

As example install devel module:

    $ docker-compose run php composer require drupal/devel:~1.0
