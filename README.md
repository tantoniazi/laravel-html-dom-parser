# laravel-html-dom-parser
Laravel wrapper for the PHP Simple HTML DOM Parser package upgrade to php 8

## Instalation
Require this package with composer:
> composer require tantoniazi/laravel-html-dom-parser

You need to add the service provider in app.php
> Tantoniazi\LaravelHtmlDomParser\ServiceProvider::class,

If you want to use the facade, add this to your facades in app.php
> 'HTMLDomParser' => Tantoniazi\LaravelHtmlDomParser\Facade::class

## Usage
```php
$name = HTMLDomParser::str_get_html($html)->find('div.profile > span.name > span')[0]->plaintext;
```