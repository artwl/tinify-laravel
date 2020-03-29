# Tinify-laravel
Tinify API support with laravel

[![Latest Version on Packagist](https://img.shields.io/packagist/v/artwl/tinify-laravel.svg?style=flat-square)](https://packagist.org/packages/artwl/tinify-laravel)

## Install

``` bash
$ composer require artwl/tinify-laravel
```

## Optional(Add Provider And Alias if laravel < 5.5)

Add this to your config/app.php

under "providers":
```php
Artwl\LaravelTinify\LaravelTinifyServiceProvider::class,
```
under "aliases":

```php
'Tinify' => Artwl\LaravelTinify\Facades\Tinify::class
```

## Set Tinypng APIKEY

Set a env variable `TINIFY_APIKEY` in `.env` file with your tinypng api key.

## Examples

```php
use Tinify;

$result = Tinify::fromFile('\path\to\file');
$result->toFile('\path\to\save');
```
