Laravel 10 is now released!
Feb 2023

Starts learning with laravel 10
laravel.com
get started

git bash
composer -v
php -v

current 8.1 supported by laravel 10

getcomposer.org
install composer - a dependency manager/package manager for php
npm - package manager for JavaScript, for Node

Creating a project
composer create-project laravel/laravel example-app
composer create-project laravel/laravel laravel-10-im-a-beginner

it will create a new directory, it will start downloading laravel 10
then we will have our laravel so yeah

how i verify that it is really completed?
check how many files i have, git bash ll, code . to open vs code
cd laravel-10-im-a-beginner
code . 
once you run, artisan development server
php artisan serve

step 1: composer -v
step 2: php -v
step 3: composer create-project laravel/laravel laravel-10-im-a-beginner
step 4: ll
step 5: cd learning-laravel-10
step 6: code .
step 7: php artisan serve

so now we can see our amazing laravel application home page is here
within a few minutes, we are up and running! <3

Intro to Routes
we are using php to run something called artisan

php artisan
a lot of artisan commands

resources > views > welcome.blade.php - ui
routes > web.php - routes

the power of laravel, which actually gives us more different way of doing the same thing
whatever we like we can do

example 1
Route::get('/', function () {
    return view('welcome');
});

another way of doing it
Route::view('/', 'welcome');

topic: understand composer json
create repository
git init
git add .
git commit -m "let's begin"
create a new repo in Github
git remote add origin git@github.com/mldp-dev/learning-laravel-10.git
git branch -M main
git push -u main origin

phpunit is a framework for php test
config file for phpunit

packagejson this is for npm dependancies
composer.json - require/requiredev for development
laravel framework - vendor laravel framwork

vendor equilvalent to node application
all the packages and dependencies

package.json extremely important

gitignore - not push in github
env - hold all the important file because it hold important configuration

topic: full authentication with laravel breeze

a powerful framework

laravel is build with different packages

if we want to have authentication system like having registration
then user login for good password, sending email for the password
how can we do that all of these things?
if we have laravel, we dont have to worry

laravel breeze - give us full authentication of our application
composer require laravel/breeze --dev
php artisan breeze:install
this package actually export every file in the respective directory for authentication

extenstion: commercial break hehe
VS Code Icons
Material Icon Theme

creating database, since were using laravel we dont have to go in mySQL
.env
add database name
automatically in laravel we can migrate it
mind-blowing laravel is creating database into the mySQL for me <3

laravel is smart enough

php artisan migrate
we can register and log in

topic: understand the migrations

php artisan migrate -h
Description:
  Run the database migrations

  database > migrations
  schema skeleton of our table

XAMPP is meant only for development purposes. It has certain configuration settings that make it easy to develop locally but that are insecure if you want to have your installation accessible to others.

Start the XAMPP Control Panel to check the server status.

http://localhost/phpmyadmin
migrations - keep the record and batches

if we want to rename/update table name to username
php artisan // check commands
php artisan make:migration update_user_table_name_to_username --table=users
    from UP
    Schema
        $table->renameColumn('name', 'username');

    reverse to DOWN / we can use it when we rollback (useful code)
        $table->renameColumn('username', 'name');

1. Schema::create
2. Schema::table

we just want to update

php artisan migrate
batch 1 first successful migration
batch 2 succeeding
reload phpmyadmin

it is really amazing? this is actually how migration works
undo migrations in vscode and db migrations delete entry and rename back to name

We created a user, by using register form
what actually happened when we filled this form and clicked the register button