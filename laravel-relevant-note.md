Laravel 10 is noe released!
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
step 5: cd laravel-10-im-a-beginner
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

