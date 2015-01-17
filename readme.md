## Laravel 5 clean install

Installing clean version from Offical website with composer:
composer create-project laravel/laravel laravel5 --prefer-dist

After installing, rename .env.example to .env and change credentials/settings.
Make common changes as on 4.2 version.
Tried to run my project, but in this new version, 
command php artisan serve is not valid (it was removed).
[https://github.com/laravel/framework/issues/6474](https://github.com/laravel/framework/issues/6474)

I couldn't access the first page, it was blank, no errors logged - not in Apache nor in Laravel logs.

Finally I tried a method found at [mattstauffer.co](http://mattstauffer.co/blog/upgrading-from-laravel-4-to-laravel-5)

php -S localhost:8000 -t public/

It still didn't work, I had to remove file storage/framework/compiled.php
Tried to access http://localhost:8000 - but was still blank page.
I checked routes, so I tried accessing home page:
http://localhost:8000/home
I was redirected to login page and from there I could finally go to Laravel 'home' page.
Yey.


## Laravel PHP Framework

[![Build Status](https://travis-ci.org/laravel/framework.svg)](https://travis-ci.org/laravel/framework)
[![Total Downloads](https://poser.pugx.org/laravel/framework/downloads.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Stable Version](https://poser.pugx.org/laravel/framework/v/stable.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Unstable Version](https://poser.pugx.org/laravel/framework/v/unstable.svg)](https://packagist.org/packages/laravel/framework)
[![License](https://poser.pugx.org/laravel/framework/license.svg)](https://packagist.org/packages/laravel/framework)

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, queueing, and caching.

Laravel is accessible, yet powerful, providing powerful tools needed for large, robust applications. A superb inversion of control container, expressive migration system, and tightly integrated unit testing support give you the tools you need to build any application with which you are tasked.

## Official Documentation

Documentation for the framework can be found on the [Laravel website](http://laravel.com/docs).

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](http://laravel.com/docs/contributions).

### License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
