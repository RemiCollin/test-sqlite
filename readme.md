#Test APP for SQLITE decimal column bug

This is a simple test app to show the SQLITE decimal column bug :

Run : 

```
    composer update
    php artisan migrate
    php artisan db:test

```

The script simply insert a decimal value into a SQLITE decimal column, then query back the table :

```php

     DB::table('test')->insert(
            ['decimal' => 1.12]
        );
    $test = DB::table('test')->get();

    dd($test);

```

