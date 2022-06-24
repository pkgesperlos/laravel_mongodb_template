1. install mongodb
   "jenssegers/mongodb": "*",

2. set this in config/database
   'mongodb' => [
   'driver' => 'mongodb',
   'host' => env('DB_HOST', '127.0.0.1'),
   'port' => env('DB_PORT', 27017),
   'database' => env('DB_DATABASE', 'homestead'),
   'username' => env('DB_USERNAME', 'homestead'),
   'password' => env('DB_PASSWORD', 'secret'),
   'options' => [
   // here you can pass more settings to the Mongo Driver Manager
   // see https://www.php.net/manual/en/mongodb-driver-manager.construct.php under "Uri Options" for a list of complete parameters that you can use

                'database' => env('DB_AUTHENTICATION_DATABASE', 'admin'), // required with Mongo 3+
            ],
        ],


3. set this in env
   DB_CONNECTION=mongodb
   DB_HOST=127.0.0.1
   DB_PORT=27017
   DB_DATABASE=firstmdb
   DB_USERNAME=
   DB_PASSWORD=

4. set this in config/add providers
   Jenssegers\Mongodb\MongodbServiceProvider::class,

5. making model
   php artisan make:model Post -mc
   

