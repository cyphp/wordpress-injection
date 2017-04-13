# wordpress-injection

## install

```bash
composer install cyphp/wordpress-injection
```

## compile

```bash
composer run build
```

## use

```php
require_once __DIR__.'/injection.phar';

use FS\Injection\I;

I::boot(__DIR__);

I::action('init', function() {
    I::__('Hello, world');
}, [
    'acceptedArgs' => 1,
    'dependencies' => ['woocommerce/woocommerce.php']
]);

```

