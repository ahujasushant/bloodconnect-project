# BloodConnect

## Getting Started

These instructions will get you a copy of the bloodconnect project in rails on your local machine for development and testing purposes.

### Prerequisites

What things you need to install the software and how to install them

#### Ruby
Ruby version for this project is ` 2.5.3`
rbenv is our recommened and preferred ruby version management software. If you don't have rbenv installed on your system. You can see the installation instructions [here.](https://github.com/rbenv/rbenv)
For installing the ruby version, type in the following command on your terminal ```rbenv install 2.5.3```.

One can check the installed ruby version by the following command ```ruby -v```.

The output should be something like this ```ruby 2.5.3p105```.

#### Postgres

Our preferred database managing software is Postgres. If not installed, one can look into their official documentation [here](https://www.postgresql.org/download) and follow the steps as given.

#### Git
Make sure you have git installed on your system, if you haven't, just refer this [How to install Git.](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### Cloning the Repository
For cloning the Github repository and goto the project follow the following commands
```
git clone git@github.com:rahuliitd98/bloodconnect-project.git
cd bloodconnect-project
```
Or one can fork it either.

#### Project Dependencies

To setup the project, follow the below commands in the project directory.
```
gem install bundler
bundle install
```
This will install all the required gems for the project on your system.

#### Creating postgres db role
To setup psql db role one can go to the psql console by the following command and create role respectively.

```
sudo -u postgres psql
postgres=#  CREATE ROLE blooodconnect with CREATEDB login password 'blooodconnect';
```

#### Create and Migrate db
For setting up the migrations on your system, run the following commands on your system:
```
bundle exec rails db:create
bundle exec rails db:migrate
```
If a project has a seed file in it, one needs to run the following command as well:
```
bundle exec rails db:seed
```

##### For running the test suite
```
bundle exec rspec spec/**/*.rb
```


##### For running the rubocop lint

The following command will fix all the rubocop offenses as per your .rubocop.yml file.
```
rubocop -a
```
If you just want to see the rubocop offenses, you normally type in `rubocop`.

NOTE: One can configure .rubocop.yml file in the project.

### Starting the rails applications
 ```
$ bundle exec rails s
``` 
Your application should be running on localhost:3000
