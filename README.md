# Tinify-laravel
Tinify API support with laravel

## Install

``` bash
$ composer require artwl/tinify-laravel
```

Add this to your config/app.php,

under "providers":
```php
        Artwl\LaravelTinify\LaravelTinifyServiceProvider::class,
```
under "aliases":

```php
        'Tinify' => Artwl\LaravelTinify\Facades\Tinify::class
```


And set a env variable `TINIFY_APIKEY` with your tinypng api key.

## Examples

```php
	$result = Tinify::fromFile('\path\to\file');


	$result = Tinify::fromBuffer($source_data);

	$result = Tinify::fromUrl($image_url);

	/** To save as File **/
	$result->toFile('\path\to\save');

	/** To get image as data **/
	$data = $result->toBuffer();
```
