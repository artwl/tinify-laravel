# Tinify-laravel
Tinify API support with laravel

## Install

``` bash
$ composer require artwl/tinify-laravel
```

## Add Provider And Alias(Optional, Only need if laravel < 5.5)

Add this to your config/app.php,

under "providers":
```php
Artwl\LaravelTinify\LaravelTinifyServiceProvider::class,
```
under "aliases":

```php
'Tinify' => Artwl\LaravelTinify\Facades\Tinify::class
```

## Set Tinypng APIKEY

And set a env variable `TINIFY_APIKEY` in `.env` file with your tinypng api key.

## Examples

```php
$result = Tinify::fromFile('\path\to\file');

$result->toFile('\path\to\save');
```
