# Google URL Shortener API

Simple PHP library for Google URL Shortener API

## Getting Started

### Composer
```bash
composer require h2akim/googl:*
```

## How to Use

#### Create a new shorten URL
Parameters available:
* longUrl
* object _(optional)_ - return as object (if true)

```php
namespace H2akim\Googl;

$googl = new Googl('your-api-key');

$googl->create([
    'longUrl' => 'http://url.that.you.want.com'
]);
```

#### Retrieve original url from shorten URL
Parameters available:
* shortUrl
* projection - _ANALYTICS_CLICKS / ANALYTICS_TOP_STRINGS / FULL_
* object _(optional)_ - return as object (if true)

```php
namespace H2akim\Googl;

$googl = new Googl('your-api-key');

$googl->expand([
    'shortUrl' => 'http://goo.gl/short-url'
]);
```
