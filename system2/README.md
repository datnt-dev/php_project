Step by steps
1. composer create-project --prefer-dist laravel/laravel name_app (e.g: system2)
2. database configuration. Open .env file to config
    e.g:
        DB_CONNECTION=pgsql
        DB_HOST=127.0.0.1
        DB_PORT=5432
        DB_DATABASE=laravel_2
        DB_USERNAME=admin
        DB_PASSWORD=1
3. intall bootstrap 4
    composer require laravel/ui
    php artisan ui bootstrap
    php artisan ui bootstrap --auth
    npm install && npm run dev
4. install Spatie package for ACL
    composer require spatie/laravel-permission
    composer require laravelcollective/html

*****
5. config/app.php: like that
    'providers' => [
        ....
        Spatie\Permission\PermissionServiceProvider::class,
        Collective\Html\HtmlServiceProvider::class,
    ],

    'aliases' => [
        ....
        'Form' => Collective\Html\FormFacade::class,
        'Html' => Collective\Html\HtmlFacade::class,
    ],
    